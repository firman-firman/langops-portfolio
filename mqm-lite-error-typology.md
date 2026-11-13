# MQM-Lite Error Typology

A simplified Multidimensional Quality Metrics (MQM) typology for scoring
AI-translated output quickly and consistently. Full MQM has dozens of
issue types; this keeps the five that catch ~90% of real problems in
AI output, with severity weights so a score can be computed.

## Categories

| Category | What it catches | Examples |
|---|---|---|
| Accuracy | Wrong meaning | Mistranslation, omission, addition, hallucinated detail |
| Fluency | Broken target language | Grammar errors, spelling, unnatural phrasing |
| Terminology | Glossary violations | Approved term not used, inconsistent term, wrong term |
| Locale conventions | Wrong local formats | Dates, numbers, currency, units, address formats |
| Style / register | Wrong tone for the content | Overly formal for casual UI, or casual for legal text |

## Severity weights

| Severity | Weight | Meaning |
|---|---|---|
| Critical | 10 | Changes meaning dangerously, or makes content unusable |
| Major | 5 | Clearly wrong; a user would notice and be misled |
| Minor | 1 | Noticeable but doesn't change meaning |

## Scoring

```
Score per 1,000 words = 100 − (total penalty points / words × 1000)
Pass threshold: 95+ for user-facing content, 90+ for internal content
```

Worked example: a 500-word help article with 2 major terminology errors
(2 × 5 = 10) and 3 minor fluency errors (3 × 1 = 3). Total penalty 13.
Score = 100 − (13 / 500 × 1000) = 100 − 26 = **74 → FAIL**.

## Rules of use

1. **Score per segment, aggregate per document.** A single bad segment
   shouldn't hide in a good average — report the worst segment too.
2. **One error, one category.** If an error fits two categories, pick the
   one that describes the *effect* (a wrong term is Terminology, even if
   it also reads awkwardly).
3. **Calibrate with a second reviewer** on the first 20 segments. If two
   reviewers disagree on severity more than 20% of the time, the
   definitions need tightening, not the reviewers.
4. **Track error mix over time.** If Terminology dominates, fix the
   glossary/prompt. If Accuracy dominates, the model or the workflow is
   the problem — not the reviewer.
