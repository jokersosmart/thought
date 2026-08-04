# Repository Guidelines

## Project Structure & Module Organization

This repository is a Markdown knowledge base for an AI and thinking-skills course. The numbered files `01_*.md` through `45_*.md` are lesson transcripts arranged in course order. `思考習慣清單_v3.md` defines the 76 thinking habits. `思考決策資料庫/` contains reusable decision reports derived from the transcripts, with its entry point at `思考決策資料庫/README.md`. There are currently no application source directories, automated tests, build scripts, or binary assets.

Keep lesson files at the repository root and preserve their numeric prefixes. Filenames should use the pattern `NN_<大眾會有共鳴的問題>.md`, for example `06_為什麼團隊導入新工具總是失敗.md`. Add supporting notes only when their purpose and relationship to the course are clear; use a descriptive filename and Markdown extension.

## Build, Test, and Development Commands

No build or test toolchain is configured. For local review, use a Markdown-capable editor or previewer. Useful read-only checks include:

```powershell
Get-ChildItem -Filter *.md
rg "來源：|^#" *.md
```

These commands list Markdown content and find headings/source markers. If a future toolchain is introduced, document its canonical commands here.

## Coding Style & Naming Conventions

Use UTF-8 Markdown with ATX headings (`#`, `##`, etc.), short paragraphs, and bullet lists for checklists. Keep the existing Chinese terminology and punctuation consistent. Lesson filenames use a two-digit order followed by a concise, broadly relatable problem statement, for example `06_為什麼團隊導入新工具總是失敗.md`. Use descriptive headings and avoid renumbering existing lessons unless the course order has intentionally changed.

Preserve transcript timestamps in square brackets, such as `[00:07]`, and keep source links near the relevant lesson introduction. Do not silently rewrite quoted material; identify substantive edits in the change description.

## Testing Guidelines

There is no automated test suite. Before submitting changes, verify Markdown rendering, heading hierarchy, links, timestamps, and filename order manually. For a new or edited lesson, check that the source attribution and transcript structure remain intact.

## Commit & Pull Request Guidelines

Git history is not available in this directory, so no established commit convention can be inferred. Use concise imperative messages scoped to the change, such as `Add lesson 46 transcript` or `Correct section index links`.

Pull requests should explain which lessons or reference sections changed, link the source material when applicable, and note any intentional reordering or transcript corrections. Include screenshots only when a rendered Markdown layout change needs visual review.

## Content and Review Principles

Prefer small, focused edits. Keep the consolidated index synchronized when lesson titles, anchors, or course ordering change. Avoid adding generated files, secrets, or unrelated personal notes to the repository.

When a transcript changes materially, review its matching `思考決策資料庫/*_決策報告.md`. Keep explicit, inferred, and unverified habits distinct, and record unresolved source conflicts in `思考決策資料庫/待驗證事項.md`.
