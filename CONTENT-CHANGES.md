# Content Changes: Submission → Camera-Ready

Baseline: `main.tex` as of **2026-05-17** (pre-camera-ready, earliest version in Overleaf git history).
Target: KDD '26 camera-ready `main.tex`.

Changes are grouped into three categories. See [`main.tex.diff`](main.tex.diff) for exact line-level text.

---

## 1. Required ACM additions (formatting / metadata — not paper content)

These are mandated by ACM/KDD for the published version and do not alter the paper's argument.

- **Document class**: `\documentclass[sigconf,nonacm]{acmart}` → `\documentclass[sigconf]{acmart}` (publication mode).
- **Rights block added** (from the ACM Publication Release Confirmation):
  `\copyrightyear{2026}`, `\acmYear{2026}`, `\setcopyright{cc}`, `\setcctype{by}`,
  `\acmConference[KDD '26]{...}`, `\acmBooktitle{...}`,
  `\acmDOI{10.1145/3770855.3818652}`, `\acmISBN{979-8-4007-2259-2/2026/08}`.
- **ACM Reference Format enabled**: `printacmref=false` → `true`; removed `\setcopyright{none}` and the copyright-footnote suppression.
- **CCS Concepts added** (required by ACM for papers over 2 pages; concept IDs verified via the official ACM CCS tool):
  - Computing methodologies → **Intelligent agents** (significance 500, primary)
  - Computing methodologies → Natural language processing (300)
  - Computing methodologies → Knowledge representation and reasoning (300)

## 2. Figure

- **Figure 1 width**: `\includegraphics[width=1\linewidth]` → `[width=0.98\linewidth]`.

## 3. Prose tightening to meet the 5-page limit (content preserved)

**Why:** the mandatory rights block + CCS concepts consumed roughly half a page, pushing the body past the KDD Blue Sky 5-page limit (references excluded). Redundant/filler wording was trimmed to fit. **No claims, citations, numerical results, examples, analogies, or open questions were removed.**

Paragraph-level summary:

- **Q3 (behavioral spillover)**: two sentences merged into one; both citations (`brown2020language`, `sclar2024prompt`) kept; `Simply declaring … is unlikely to be sufficient` → `Declaring … is insufficient`.
- **Q5 (granularity)**: `fragile and brittle dependencies` → `brittle dependencies`; the recipe analogy (strawberry/blueberry cake) kept in full; `compose or reuse` kept.
- **Q6 (portability)**: kitchen-recipe analogy kept (quotation-mark typo fixed); literature-gap framing `Existing work studies model drift and prompt sensitivity in isolation, but …` kept; `Avoid-lists and tool dependencies require model-specific adaptation:` lead-in kept; trailing `across diverse settings` removed; minor word tightening.
- **Q7 (governance)**: `are currently unpaid hobbyists` → `are unpaid hobbyists`; `especially important` → `important`; `sustain valuable expertise` → `sustain expertise`. Both statistics and all citations kept.
- **Q8 (evaluation)**: `likely`, `same` removed; `provide useful precedent` → `offer precedent`; `tightly tied` → `tied`; `sustainable over time` → `sustainable`. All three benchmark citations kept; recipe analogy kept.
- **Q10 (training data)**: `and even more later` → `and growing`; `increasingly becoming` → `becoming`; `actually learn` → `learn`. All citations and the procedural-collapse argument kept.
- **Conclusion — A Call for Contribution**:
  - Opening and connective sentences tightened (removed `We believe that`, `on AI agents`, `however`, etc.).
  - Near-term horizon: the three concrete examples (clinical / synthesis / financial) and their `rather than …` parallelism kept; framing tightened.
  - Longer-term horizon: the three self-evolving behaviors kept; the defining appositive `where agents become both users and authors of procedural knowledge` kept; framing tightened.
  - Developer perspective: `straightforward` → `simple`; minor tightening; `shared knowledge commons` point kept.
  - User perspective: `not just one interaction but the reliability of the broader ecosystem` kept; minor tightening.
  - Final paragraph: tightened (`ultimately`, `engineering`, `By doing so, the field has an opportunity` removed); the core message and the bolded `procedural knowledge should be represented, shared, evaluated, and governed in agentic AI` kept.

## Net effect

- Body fits within the 5-page limit (references excluded), as required.
- All scientific content — the ten open questions, every citation, every statistic, the recipe/kitchen analogies, and the three contribution perspectives — is preserved.
