# Prompt log

## 2026-10-12

**What I asked:** Set up this portfolio repo: create the folder skeleton with
one-line placeholder READMEs, tailor AGENTS.md from the course baseline and my
resume, add a one-line CLAUDE.md pointer, start this log, put my resume into
RESUME.md as Markdown, leave my README.md bio untouched, and add a .gitignore.

**What you produced:** capabilities/, docs/briefs/, docs/decisions/, data/ and
analysis/figures/, each with a one-line README.md; AGENTS.md; CLAUDE.md;
.gitignore; this file. Claude also renamed RESUME to RESUME.md and formatted it
as Markdown, but I told it partway through not to change README or the resume,
so the rename and formatting were undone. RESUME and README.md are as I wrote
them. Nothing was committed.

**What was wrong and how it was caught:**
- My resume was missing from the prompt (the text ended at the divider). Claude
  noticed and used the RESUME file already in the repo instead.
- The web-fetch tool returned a paraphrase of the baseline's Naming section, not
  the exact text. Claude caught this and downloaded the page source to copy the
  section word for word.
- The first Markdown pass of RESUME.md changed the all-caps section headings to
  title case. A text diff against the original caught it. That change was
  undone anyway when the resume was reverted.
