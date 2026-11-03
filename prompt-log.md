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

## 2026-11-02

**What I asked:** Help prepare my FIN-321 Stage 1 executive brief on FX hedging
(scenario 28, film-rights): confirm my scenario, check the arithmetic, create a
draft, and create capabilities/fx-hedging/README.md if the instructions require it.

**What you produced:** Confirmed the scenario inputs against scenarios.md; a
calculation note (baseline $4,232,160 at the indicative 1.1756; a 5% weaker
euro costs $211,608; the put costs $80,640); the brief's frontmatter and
template scaffold; a checklist; and capabilities/fx-hedging/README.md, which
the Stage 1 checklist requires. Claude did not draft the brief's text, because
AGENTS.md and the course rules say the brief is mine to write first.

**What was wrong and how it was caught:**
- The scenario was not in my first message. Claude asked for it, and I pasted
  my instructor's email, which Claude checked against scenarios.md.
- The Chrome extension was not connected, so Claude could not read the tab I
  pointed it to. The pasted email made reading the tab unnecessary.

## 2026-11-02 (same session, continued)

**What I asked:** For Claude to write the Stage 1 brief draft. Claude declined to
write it, so instead it interviewed me section by section and critiqued each of
my answers. Then I asked it to create the draft file.

**What you produced:** docs/briefs/2026-11-02-film-rights-hedge-brief.md: my
own answers pasted unchanged into the template, plus frontmatter, a References
list, a corrected ECB link (Croatian page to English page), and TODO comments
listing the fixes still to make. Claude also pulled the ECB EURUSD reference rate
for 2026-11-02 (1.1216) and checked every figure in my answers.

**What was wrong and how it was caught:**
- My ECB link pointed to the Croatian-language page; Claude caught it.
- Claude said a fairly priced put would make expected proceeds "roughly equal"
  to the forward's. I caught that this holds only for discounted risk-neutral
  values, not real-world expected proceeds.

## 2026-11-02 (same session, continued)

**What I asked:** Review my brief (a Word draft, then a Markdown version from my
Codex submission package), add the AI attribution, put it in the repo, push it,
and submit on Lamaku.

**What you produced:** Reviews of both versions (word count, arithmetic,
checklist). Copied the Markdown brief and the package's
capabilities/fx-hedging/README.md into the repo. The package README replaced
the shorter one Claude had made, and the brief replaced the earlier scaffold.
Added the llm_used field and the LLM Used line, crediting Codex (planning,
calculations, drafting) and Claude (input checks, ECB spot rate, arithmetic
verification, critique). Changed the ECB link from the Croatian page to the
English one.

**What was wrong and how it was caught:**
- The Markdown version had dropped all AI attribution, though the Word version
  credited Codex with drafting. Claude caught it in review and restored it.
- The ECB link had reverted to the Croatian page; Claude caught it in review.
