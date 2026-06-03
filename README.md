# Recipes for Agents — Submission vs. Camera-Ready Diff

This repository documents the changes made to the KDD '26 Blue Sky Ideas Track paper

> **Recipes for Agents: Understanding Skills and Their Open Questions**
> Hanwen Xing, Haomin Zhuang, Xuandong Zhao, Yue Huang, Zhenheng Tang, Xiangliang Zhang
> *Proceedings of the 32nd ACM SIGKDD Conference on Knowledge Discovery and Data Mining V.2 (KDD '26).*
> DOI: [10.1145/3770855.3818652](https://doi.org/10.1145/3770855.3818652)

between the **submission / accepted version** and the **camera-ready version**.

## How to read the diff

This repo has two commits:

1. **Submission version** — snapshot of `main.tex` as of 2026-05-17 (the last author edit before camera-ready preparation; the earliest version available in the Overleaf git history).
2. **Camera-ready version** — the final KDD '26 camera-ready `main.tex`.

The cleanest way to view the line-by-line changes is GitHub's commit comparison
(the **Camera-ready** commit shows the full diff against the **Submission** commit).
The same diff is also saved as a plain file: [`main.tex.diff`](main.tex.diff).

For a human-readable, categorized summary of what changed (and why), see
[**CONTENT-CHANGES.md**](CONTENT-CHANGES.md).

## TL;DR

The camera-ready changes fall into three buckets:

1. **Required ACM additions** (formatting/metadata, *not* paper content): CC-BY rights block, DOI/ISBN, ACM Reference Format, and CCS Concepts.
2. **Figure**: Figure 1 width adjusted (`1\linewidth` → `0.98\linewidth`).
3. **Prose tightening to fit the 5-page limit**: the mandatory rights block + CCS concepts consumed roughly half a page, pushing the body past the Blue Sky 5-page limit, so redundant/filler wording was trimmed. **All claims, citations, data, examples, analogies, and the ten open questions are preserved.**

## Files

| File | Description |
|---|---|
| `main.tex` | Camera-ready version (the submission version is in the first commit) |
| `main.tex.diff` | Raw unified diff (submission → camera-ready) |
| `CONTENT-CHANGES.md` | Categorized, human-readable change summary |
| `references.bib`, `ACM-Reference-Format.bst`, `figs/` | Support files (unchanged between the two versions) |
