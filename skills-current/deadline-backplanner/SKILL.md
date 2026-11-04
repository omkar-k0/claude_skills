---
name: deadline-backplanner
description: Reverse-schedule a real deadline into a milestone plan with buffers and collision checks against existing commitments. Use whenever Omkar mentions a submission date, exam date, presentation deadline, application deadline, driving-license milestone, or says "plan backwards", "how do I make this deadline", or names any dated deliverable that needs a schedule.
---

# Deadline Backplanner

Builds the schedule only. Producing the content of any scheduled task is a separate request; that boundary is the point.

## Rigor Block (skill-specific, mandatory)

- **Plan-Gate:** The whole skill is a plan-gate: the milestone plan is the deliverable and it stops for approval before ANY task content gets generated. "Plan approved, now draft milestone 1" is a new instruction he must give.
- **Scope-Fence:** Schedule structure only. No drafting, no studying material, no writing of the deliverable itself inside this skill. If asked to do both in one breath, deliver the plan, then ask which milestone to execute.
- **Adversarial Verification:** After drafting, attack the plan: identify the milestone most likely to slip (honest reason: dependency on someone else, unfamiliar tool, historical pattern), and show what the cascade does to the end date. The plan ships with its own failure analysis.
- **Live-State Truth:** Requires the real deadline date and his real fixed commitments (exam dates, work hours, the July 18 first-aid/eye-test type appointments, travel). Today's actual date anchors the math. A plan built on assumed availability is refused.
- **Ruthless Editing:** Output is the dated milestone table and the risk note. No productivity advice, no "you've got this".

## Protocol

1. **Intake:** deadline date and hard-or-soft status; deliverable and its known components; fixed commitments in the window; realistic weekly hours for this (his number, then challenged if it collides with commitments); external dependencies (supervisor feedback loops, data access, appointment lead times).
2. **Backward pass:** from the deadline, place milestones in reverse. Every milestone: name, done-criterion (verifiable, not "work on X"), date, estimated hours.
3. **Buffer policy:** 20% buffer before the final deadline, placed as an explicit milestone ("buffer: nothing scheduled"), not smeared invisibly. External-dependency milestones get lead-time buffers sized to the dependency (supervisor feedback: use the actual known turnaround, ask if unknown).
4. **Collision check:** overlay commitments week by week. Any week where required hours exceed available hours is flagged with the specific conflict, and the plan is revised or the conflict is surfaced as his decision to make.
5. **Failure analysis (adversarial):** most-likely-to-slip milestone, why, cascade effect, and the pre-committed response ("if milestone 3 slips past <date>, cut <specific scope>").
6. **Stop.** Approval. Task execution is a new request.

## Hard rules

- No milestone without a verifiable done-criterion.
- If the honest math says the deadline is not achievable at stated hours, the output says so first, with the two real options (more hours or less scope), before any table is shown. A pretty plan for an impossible deadline is a lie.
- Dates come from the actual calendar (weekday-aware); milestones never land on days he declared unavailable.
