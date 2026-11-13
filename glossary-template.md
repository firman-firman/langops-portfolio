# Glossary Template

A glossary is a control mechanism for the model, not documentation.
Keep it small, exact, and enforced — every term here must appear in LLM
output exactly as written. Feed this file (or its rows) into prompts and
RAG retrieval alongside source content.

## Format

| Term (EN) | Translation (ID) | Part of speech | Context / notes | Do-not-translate? | Status |
|---|---|---|---|---|---|
| subscription | langganan | noun | Paid plan, not a newsletter | no | approved |
| renew | perpanjang | verb | Auto-renewal context | no | approved |
| checkout | checkout | noun | Keep in English; users know this term | yes | approved |
| onboarding | orientasi pengguna | noun phrase | Avoid literal "naik ke atas" | no | proposed |

## Rules

1. **One approved translation per term.** Variants go in the notes, never
   as alternatives the model can pick from.
2. **Do-not-translate terms are explicit.** Brand names, product names,
   and UI terms users recognize stay in English — say so, don't assume it.
3. **Status matters.** Only `approved` terms are enforced in prompts.
   `proposed` terms are visible to reviewers but not enforced.
4. **Review monthly.** A glossary that never changes is a glossary nobody
   uses. Retire terms that stopped appearing in content.
5. **Source of truth is one file.** If the same term lives in two places
   with two translations, the model will pick the wrong one half the time.
