---
name: deadline-backplanner
description: Reverse-schedule a real deadline into a dated milestone plan with an explicit buffer, a week-by-week collision check against fixed commitments, and a failure analysis. Builds the schedule only; the content of any milestone is a separate request. Use whenever Omkar mentions a submission date, exam date, presentation deadline, application deadline, driving-licence milestone, Abgabe, Klausurtermin, or says "plan backwards", "how do I make this deadline", "is this still doable", or names any dated deliverable that needs a schedule.
---

# Deadline Backplanner

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

The milestone plan is the deliverable. Drafting the thing being scheduled is a different job he asks for separately. Read `references/fixed-dates.md` for his standing commitments and tier rules.

## Gate

A plan is routine when three inputs are stated: the deadline date (hard or soft), his fixed commitments in the window, and his realistic weekly hours for this. Then the plan ships. If any of the three is missing, no plan is built; the response names the missing input. Weekly hours are his number, checked against commitments: a week where required hours exceed available hours is a collision, flagged with the specific conflict, and the plan is revised or the choice is handed to him. A plan built on assumed availability is not a plan.

## Protocol

1. **Intake.** Deadline and status; deliverable and its known components; fixed commitments in the window (from the reference file plus what he adds); weekly hours; external dependencies (supervisor turnaround, data access, appointment lead times) with their known lead times, asked for if unknown.
2. **Backward pass.** From the deadline, place milestones in reverse. Each has a name, a verifiable done-criterion (not "work on X"), a date, and estimated hours. Dates are weekday-aware and never land on days he declared unavailable.
3. **Buffer.** 20% of the window before the final deadline, as a visible milestone ("buffer: nothing scheduled"), not smeared across tasks. External dependencies get their own lead-time buffer sized to the real turnaround.
4. **Collision check.** Commitments overlaid week by week, per the gate.
5. **Failure analysis.** The milestone most likely to slip, the honest reason (dependency on someone else, unfamiliar tool, his deadline-panic pattern), the cascade to the end date, and the pre-committed response: "if milestone 3 slips past <date>, cut <specific scope>."

## Hard rules

- If the honest math says the deadline is not achievable at the stated hours, that is the first line, with the two real options (more hours or less scope) before any table.
- Plans never cut Tier 1 (studies, gym, food) to make room. Cuts come from Tier 3 first, then Tier 2.
- Output is the dated milestone table and the risk note. No productivity advice.
