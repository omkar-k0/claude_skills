# Changelog: skills v2

One line per change, with the reason. "Rigor Block" means the five-heading block (Plan-Gate, Scope-Fence, Adversarial Verification, Live-State Truth, Ruthless Editing) that v1 pasted into every skill.

## rigor-core (new)
- Added: single doctrine file covering confidence tags, the per-skill gate, act-with-enough-information, assessment-not-action, checkpoints only where needed, grounded progress, fresh-context verification, lead-with-outcome, judge-by-logged-data, and the no-reasoning-display rule. Reason: the Fable 5 guide says skills for older models are too prescriptive; one short doctrine replaces nine pasted copies.
- Added: the fixed four-sentence pointer block every other skill carries. Reason: each skill must still work when rigor-core is not loaded.

## humanizer
- Removed: Rigor Block. Replaced by the pointer. Reason: duplicated doctrine.
- Removed: "Merge note" about a previous humanizer.skill. Reason: one-off migration instruction, no longer true.
- Removed: the explicit reverse-test self-critique instruction. Reason: rigor-core routes high-stakes checks to a fresh-context verifier; "the output obeys the rules it enforces" keeps the intent in one line.
- Added: gate separating mechanical rules (R1, R2, R6, R7, R9, R10) from judgment rules (R3, R4, R5, R8). Reason: routine edits pass through, judgment edits are explained, meaning changes are flagged not made.
- Kept: R1 to R10 word for word, Diff-Pass output format, register note. Reason: his style preferences.
- Fixed: description now states it is the style authority other skills point to.

## citation-verifier
- Removed: Rigor Block. Replaced by the pointer.
- Removed: mandatory approval step on every inventory. Replaced by a scope question only above about 15 citations. Reason: checkpoints only where the work needs him.
- Added: gate defining VERIFIED as a live lookup in this session that matches author, year, title, and claim direction; memory never counts. Reason: this is the skill's confidence gate.
- Kept: five verdicts, 15-word quote limit, 25% rebuild rule, verify-do-not-rewrite boundary.

## career-pipeline
- Fixed: SAP removed as a career target in the description, SKILL.md, and verified-facts.md; target is applied AI and data Werkstudent and junior roles. Reason: stale.
- Fixed: German status replaced with the FOM Deutsch exam on 13 Nov 2026 at A1 to A2 and the A2 and B1 goals; the VHS Duisburg course line deleted. Reason: outdated.
- Added: three portfolio projects (Guidance Reconciliation Engine, ContractTracker, Werkbank) to verified-facts.md with their eval status, and the rule that result numbers need an eval table (ship-with-eval). Reason: in his notes, needed for claims.
- Kept: every existing [CONFIRM] field, open. Added two more where facts were uncertain.
- Removed: Rigor Block and the propose-structure-then-wait step for STAR and LinkedIn drafts. Reason: the model drafts well first-shot; a draft with [CONFIRM] markers is cheaper than a round trip.
- Added: gate on verified-facts.md lines without [CONFIRM]. Reason: this is the skill's confidence gate.
- Kept: one mode per session, send-ready output, gap-reported-as-gap, formal German conventions, live check for the 20-hour rule, conflict resolution with the facts file.

## deadline-backplanner
- Removed: Rigor Block. Replaced by the pointer.
- Removed: stale "July 18 first-aid/eye-test" example. Reason: outdated.
- Added: gate on the three required inputs (deadline, commitments, hours) and the deterministic collision test. Reason: confidence gate.
- Added: references/fixed-dates.md with the challenge window, German exam date, weekly budgets, tiers, and slip-risk patterns. Reason: the collision check needs his standing commitments, which were only in his notes.
- Added: tier rule (never cut Tier 1) to hard rules. Reason: from his notes.
- Kept: schedule-only boundary, 20% visible buffer, done-criteria, failure analysis, impossible-deadline-first rule.

## exam-study-pack
- Removed: Rigor Block. Replaced by the pointer.
- Removed: "Approval is an explicit yes" wording and the recompute-as-Adversarial label. Reason: too prescriptive; the topic map confirmation stays because item counts decide cost.
- Added: gate on "topic appears in the provided material, cited by location" and a [CONFIRM] rule when the professor's method is unknown. Reason: confidence gate.
- Kept: all five modes, professor-method-overrides-standard rule, the three reference files unchanged.

## idea-interrogator
- Added: the rigor-core pointer (it had no Rigor Block).
- Added: gate on verified versus UNVERIFIED claims and a LOW CONFIDENCE tag when two or more load-bearing answers are holes. Reason: confidence gate.
- Removed: inline humanizer rule restatement ("no em dashes, no filler..."). Reason: style is owned by humanizer.
- Removed: "(Scope-Fence)", "(Plan-Gate)" labels in step headings. Reason: v1 vocabulary.
- Kept: tone contract, one-question-at-a-time protocol, four-part verdict, DROP IT always live, pushback rule, skip-refusal rule.
- Fixed: domain-checklists.md heading "Career / job / SAP path ideas" renamed to "Career / job / Werkstudent ideas".

## oral-defense-simulator
- Removed: Rigor Block. Replaced by the pointer.
- Removed: formal approval of the attack map; he can redirect, otherwise it starts. Reason: checkpoint only where needed.
- Added: anchor gate: a question is asked only when it cites a location in the document. Reason: confidence gate.
- Kept: examiner character, escalation order, kill question, bluff-calling, fixed debrief, minimum six questions, no weak-rated-as-pass.

## panel-regression-rigor
- Removed: Rigor Block. Replaced by the pointer.
- Added: gate: a statistic is reported only if it exists in session output; post-hoc changes are logged and labelled exploratory. Reason: confidence gate; this was spread across three v1 bullets.
- Kept: Phase 1 spec with approval stop (a real scope decision), seven spec items, battery contract, adversarial re-estimation, FAIL-is-FAIL, causal-language rule. robustness-battery.md unchanged.

## vlog-production
- Removed: Rigor Block. Replaced by the pointer.
- Removed: draft-for-approval step on shot lists. Reason: the list is the deliverable; voiceover and captions stay separate requests.
- Added: gate: shots, spots, and beats rest on a lookup, a map result, or an inventoried clip; light times say "not looked up" rather than guess. Reason: confidence gate.
- Kept: three modes, MUST-HAVE core, no drone, inventory-only beat-maps, Deutschland-Ticket transit rule.

## life-os (new)
- Added: commands start, what now, log, Sunday review; bad-week mode with the data trigger and the fixed minimum day; detector; tier rules; restart preference; write scope limited to Daily/, Weekly/, Tracks/; text fallback without a vault tool.
- Added: gate deciding full day versus minimum day from logged numbers only. Reason: his rule "judge by logged data".
- Added: references/life-system.md with templates, budgets, patterns, and a [CONFIRM] slot for the private log field and for wake time.

## vault-keeper (new)
- Added: the eight vault rules as operations; gate on "source is something he said or logged in this session" else #gap; never delete, move to _to_delete/; _Log.md line per session; text fallback.
- Added: references/vault-rules.md with a [CONFIRM] for the vault tool and root path.

## ship-with-eval (new)
- Added: definition of done (labelled eval set, metrics table with share auto-handled and accuracy per confidence band, numbers in README); gate blocking any claim without a table at a named path; smallest-eval proposal; labels never generated by Claude.
- Added: references/projects.md with the three projects and their eval status.

## backtest-gatekeeper (new)
- Added: Phase 1 pre-registration (hypothesis, pass bar, baseline, scaling, validation design, sealed holdout, markets, trade count) and Phase 2 run log and reporting; gate on "every input logged before the result" with numbered iterations; holdout looked at once; demo accounts only.
- Added: references/research-rules.md with the house rules verbatim and [CONFIRM] markers for run-log path, market set, and holdout period.
