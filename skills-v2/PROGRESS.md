# Progress

Only work with a file or tool result behind it is listed.

## Phase 1: rigor-core (done 2026-11-04)
- Branch `skills-v2` created from `main` (git checkout output).
- `skills-current/` unzipped into the repo from the uploaded archive; `context/CONTEXT.md` placed in `context/` and listed in `.gitignore` (not committed).
- Fable 5 prompting guide fetched live and quoted in `NOTES.md`.
- `skills-v2/rigor-core/SKILL.md` written: 52 lines, frontmatter `name` and `description` only, covers all eight required behaviours plus confidence tags and the pointer block other skills will carry.
- `NOTES.md` holds the working notes and the mapping from the old Rigor Block headings to rigor-core.

## Phase 2: nine refactors (done 2026-11-04)
- Nine `skills-v2/<skill>/SKILL.md` rewritten: humanizer, citation-verifier, career-pipeline, deadline-backplanner, exam-study-pack, idea-interrogator, oral-defense-simulator, panel-regression-rigor, vlog-production. Longest is 41 lines (wc -l).
- Every skill carries the four-sentence rigor-core pointer and one named Gate section (grep "Rigor: see rigor-core" returns all; grep "## Gate" returns all).
- Descriptions between 547 and 648 characters (wc -c on the description line).
- humanizer R1 to R10 diffed against skills-current: identical.
- career-pipeline/references/verified-facts.md: SAP moved out of target, German line replaced with the 13 Nov 2026 exam at A1 to A2, VHS course line removed, three portfolio projects added with eval status, every existing [CONFIRM] kept.
- deadline-backplanner/references/fixed-dates.md added (challenge dates, German exam, weekly budgets, tiers, patterns).
- idea-interrogator/references/domain-checklists.md: "SAP path" heading renamed to "Werkstudent ideas"; rest unchanged.
- exam-study-pack and panel-regression-rigor references copied unchanged.
- grep for em dashes and reasoning-display phrases across skills-v2: only hit is rigor-core's own prohibition sentence.

## Phase 3: four new skills, EVAL.md, zips, PR (done 2026-11-04)
- Four new `skills-v2/<skill>/SKILL.md` written with references: life-os (37 lines + references/life-system.md), vault-keeper (29 + references/vault-rules.md), ship-with-eval (36 + references/projects.md), backtest-gatekeeper (37 + references/research-rules.md). Descriptions 615 to 648 characters.
- `CHANGELOG.md`: one line per removal, addition, or fix for all 14 skills.
- `QUESTIONS.md`: 25 items, each pointing at the file holding its `[CONFIRM]`.
- `EVAL.md`: 28 fresh-context Sonnet runs (two prompts per skill, one skill folder loaded, no access to other skills or CONTEXT.md), judged against each skill's own rules. 27 PASS. One run returned no output because the API refused the prompt's request for internal reasoning (reasoning_extraction); re-tested with a rephrased prompt, PASS. One gate sentence in life-os tightened after its adversarial run and re-tested (result recorded in EVAL.md).
- 14 upload-ready zips built by `zip -r` from each skill folder (`ls skills-v2/*.zip | wc -l` = 14), rebuilt after the life-os edit.
- `context/CONTEXT.md` never committed (`git ls-files context` is empty).
