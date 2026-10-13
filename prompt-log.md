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

## 2026-10-12 (same session, continued)

**What I asked:** Grade my Phase 0 submission (open in Brave), then rename
RESUME to RESUME.md.

**What you produced:** A checklist review of the live repo against the Stage 0
deliverable list. Then RESUME renamed to RESUME.md, with its content unchanged.

**What was wrong and how it was caught:**
- Claude could only read Brave, not scroll it, so it couldn't see my submitted
  text and graded the repo on GitHub instead. It said so in its answer.
- The review caught that the resume file had no .md extension. The checklist
  requires RESUME.md at the root, and the file was renamed to fix it.
- The review also caught that README.md has no engagement index yet. It is
  still open: I write that part myself.

## 2026-10-12 (same session, continued)

**What I asked:** Fix the missing engagement index in README.md.

**What you produced:** An "Engagements" table (engagement, capability, brief,
decision) with one "None yet" row, added below my bio. The bio is unchanged.

**What was wrong and how it was caught:**
- The first check that the bio was unchanged failed because of how macOS `cmp`
  handles a byte count. It was rerun a different way and the bio matched byte
  for byte.
