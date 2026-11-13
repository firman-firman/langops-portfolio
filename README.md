# LangOps Portfolio — Firman Tahar

Language Manager at Meta (Bahasa Indonesia), building LangOps expertise:
designing **AI-native localization architecture** for organizations moving
into multilingual markets.

## What "LangOps" means here

Not translation itself — the **system around it**: how multilingual content
flows from source to market, how AI is applied deliberately (and where it
is kept out), how quality is measured, and how humans stay in the loop.
Language management is becoming language-agnostic; the value is in the
architecture, not in any single language pair.

## What's in this repo

- `prompt-library/` — reusable, production-shaped LLM prompts for
  localization work (translation QA first).
- `glossary-template.md` — a terminology template built for LLM grounding.
- `mqm-lite-error-typology.md` — a lightweight MQM error typology for
  scoring AI output quickly and consistently.
- `projects/` — end-to-end builds (first up: a small AI localization
  pipeline, EN → ID, with terminology enforcement and QA gates).
- `learning-log.md` — what I'm studying, week by week.

## Working principles

1. **Human-in-the-loop, always.** AI drafts; humans decide. The loop level
   (in / on / out of the loop) is chosen per workflow, not per hype cycle.
2. **Terminology first.** A glossary is not documentation — it is a
   control mechanism for the model.
3. **Measure quality, don't feel it.** MQM categories, severity weights,
   pass thresholds. If it can't be scored, it can't be improved.
4. **No black-box AI in production.** Every automated step has a named
   owner, a confidence signal, and a route to human review.
5. **Recordings over live attendance.** Learning fits around real work —
   async by default, live when it matters.

## Background

- Language Manager, Meta — Bahasa Indonesia (2 years)
- Path: in-house LangOps first, then independent consulting
- Currently: free resources + short courses + hands-on projects
  (see `learning-log.md`)
