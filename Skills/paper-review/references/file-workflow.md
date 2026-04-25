# File Workflow

Use this workflow when the user asks to review a local paper, an extracted paper directory, a PDF, or pasted text and expects the result to be saved.

## Default Paths

Do not hard-code private local paths, usernames, personal names, or machine-specific directories in this public skill.

| Purpose | Default |
|---|---|
| Paper source | Explicit user-provided file path, attached text, or current workspace |
| Optional extracted-paper source directory | A user-approved directory such as `<PAPER_SOURCE_DIR>` |
| Review output directory | `./reviews/` in the current workspace, unless the user provides another directory |
| Skill directory | The directory containing this `paper-review` skill |

## Input Priority

1. Use an explicit file path from the user.
2. Use an attached or pasted paper text if provided.
3. If the user gives only a title, search the current workspace and any user-approved source directory for likely matching PDF, Markdown, TXT, or extracted content.
4. If multiple local matches are plausible, report the candidates and ask the user which one to review.
5. If only an abstract or excerpt is available, write a partial review and label unsupported sections clearly.

## Reading Guidance

- Prefer Markdown/TXT extracted from the PDF when available because it often preserves equations and section order better than ad hoc PDF text extraction.
- For PDFs, use the available PDF skill or local extraction tools when needed; inspect tables, equations, abstract, introduction, empirical strategy/model section, results, and conclusion.
- Keep track of what came from the paper versus your own evaluation.
- If equations are garbled after extraction, reconstruct only when the source is clear; otherwise mark `公式需核对原文`.

## Output Naming

Default filename:

```text
YYYY-MM-DD_<safe-title>_review.md
```

Rules:

- Use the current local date.
- Derive `<safe-title>` from the paper title when available; otherwise use the source filename stem.
- Replace Windows-illegal filename characters with `_`: `< > : " / \ | ? *`.
- Collapse repeated spaces and underscores.
- Truncate the title portion to about 80 characters if necessary.
- If a file already exists, append `_2`, `_3`, and so on.

## Saving Behavior

- Save the complete Markdown review to `./reviews/` in the current workspace unless the user gives another output directory.
- If the user gives an absolute output path, use it only for that task; do not copy that path into reusable skill documentation.
- After saving, return:
  - output file path
  - paper title
  - paper type
  - 3-5 most important takeaways
  - any evidence limitations, such as incomplete PDF extraction or missing tables

## Public-Skill Privacy Rules

- Do not include personal names, usernames, home directories, cloud-drive paths, or private organization folder names in committed skill files.
- Use placeholders such as `<PAPER_SOURCE_DIR>`, `<OUTPUT_DIR>`, and `./reviews/` in examples.
- Before publishing a skill, search for Windows/macOS/Linux home-directory patterns, personal names, email addresses, and local project names.

## Safety and Quality Checks

- Do not overwrite an existing review unless the user explicitly asks.
- Do not delete, move, or rename source paper files.
- Do not fabricate bibliographic metadata or empirical results.
- Before saying the review is complete, confirm the Markdown file exists and can be read as UTF-8.
