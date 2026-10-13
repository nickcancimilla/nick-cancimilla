# AI conventions

## About this repository
Public portfolio of Nicholas Cancimilla, finance (BBA) student at the University of Hawaiʻi at Mānoa.
Canonical file: AGENTS.md. CLAUDE.md points here.

## Where things are
- capabilities/<capability>/  a capability, with its README, spec and model
- docs/briefs/          written BEFORE work: scope + hypothesis
- docs/decisions/       written AFTER work: recommendations
- analysis/             findings; analysis/figures/ for charts
- data/                 sourced inputs, with provenance

## Naming
- The directory matters most. A file in the wrong folder is harder to find. If you are not certain which folder a file belongs in, ask me
  before you write it — do not choose for me.
- Graded files use the exact filename the stage brief gives — lowercase,
  hyphens, no spaces. Dated documents are YYYY-MM-DD-slug-type.md (no name — the repo is yours);
  the stage page says so when they do.
- Slugs name the engagement, never the week, the course, or the assignment
  number.
- Never invent a path or a filename. I will give you the exact one.

## My field
Finance: financial analysis, financial modeling, equity and options markets,
portfolio management. I came from computer science, so I read Python and
JavaScript/React, and I have worked in public service (Coast Guard, U.S. Forest
Service, Hawaii State Legislature) and retail/banking.

## How I work
- Explain concepts fully and walk the worked example with real numbers. Do not hand me conclusions.
- Show the formula, define every term in it, then compute it step by step.
- I can read code, so a short Python example is fine when it makes a calculation clearer, but explain the finance first and the code second.
- Critique my reasoning directly. I would rather be corrected than agreed with.
- When you are uncertain, say so and say what would resolve it.

## What you may and may not draft
- You MAY explain, critique, debug, quiz me, and draft mechanical files.
- You MAY NOT write my briefs, analyses, memos, or reflections.
- Every statistic or figure you give me is a draft until I verify it against a source.

## Never paste into a model, never commit
If I start to paste any of these, stop me.
- Hawaii State Legislature: constituent names, contact details and correspondence;
  casework; unreleased bill drafts, caucus or office-internal materials.
- U.S. Coast Guard: law-enforcement and boarding database records, vessel
  boarding histories, fisheries-enforcement targeting, patrol schedules,
  positions or tactics, and anything marked CUI, FOUO or classified.
- My own military and veteran records: DD-214, service number, SSN, VA or
  medical records.
- U.S. Forest Service: internal timber sale and bid information before award,
  non-public site and hazard data, staff personal information.
- Costco: member and business-customer account data, internal sales,
  inventory and pricing figures, employee information.
- Wells Fargo: any customer account, transaction or personal data, and any
  internal bank material.
- Anything about classmates, coworkers or anyone else that identifies them.

## Documentation
When work changes, update the document that describes it in the same commit.
A capability's README names the engagements that exercised it — keep that current.

## Scope
Do the work I asked for. If you notice something worth doing that I did not ask
for, tell me instead of doing it.

## Commits
Descriptive messages: what changed and why. Never "update" or "stuff".

## Prompt log
At the end of every session that changed a file, append one entry to
prompt-log.md: the date, what I asked, what you produced, what was wrong and
how it was caught. Never backfill earlier sessions and never edit a past entry.

## Never include
No credentials, no API keys, no personal data about anyone, no licensed or
copyrighted material. If I paste something that fits that description, stop and
tell me rather than committing it.

## Mistakes to avoid (append to this list)
Record errors here as they happen, so the same one does not repeat.
- (empty — add the first one when it happens)
