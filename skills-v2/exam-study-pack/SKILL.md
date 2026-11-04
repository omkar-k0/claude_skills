---
name: exam-study-pack
description: Build FOM exam study materials from the professor's actual topic list only: worked calculation guides with self-check values, OMR multi-answer MCQ banks with a distractor audit, NotebookLM prompt packs, one-page formula sheets, and hypothesis-test selection walkthroughs. Use whenever Omkar mentions exam prep, study pack, Klausur, QDA, MCQs, formula sheet, worked examples, NotebookLM prompts, or preparing for any FOM module exam, and whenever he uploads a syllabus, lecture slides, or a professor topic list. Never generates content from memory of what a subject usually covers.
---

# Exam Study Pack

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

Five deliverable types from one intake: the professor's own material (syllabus, slides, topic list, announcement) as an upload or paste. Without it, stop and say what is needed.

## Gate

A topic enters the pack only when it appears in the provided material; the topic map cites where (slide number, page, line). That is the routine case. A topic he names that is not in the material is ambiguous: it is listed as "not in the professor's material" and left out until he confirms it is examinable. A calculation method documented in `references/method-conventions.md` overrides the textbook or software default; where no convention is recorded and the professor's examples differ from the standard, flag it as `[CONFIRM: professor's method]` instead of picking one.

## Flow

1. **Topic map.** Table: topic | where in the material | requested deliverables | item count. He confirms or trims before generation, because item counts decide the session's cost.
2. **Generate.**

**A. Worked calculation guides.** Per topic: problem, every intermediate value, a self-check value at each stage ("your running sum should now be 247.5"), the one trap students hit. Recompute each result by a second route before delivery. Quartiles and percentiles follow method-conventions.md.

**B. MCQ bank.** Read `references/mcq-format.md`. OMR multi-answer: four or five statements per item, any subset true. Run the distractor audit on every item and fix failures before delivery. Answer key generated in the same pass as the questions, with a one-line justification per statement.

**C. NotebookLM prompt pack.** Ready-to-paste prompts in copy blocks: audio overview, quiz, targeted deep-dives per weak topic. Prompts only.

**D. Formula sheet.** One page. Per formula: name, formula, when-to-use condition, the one trap. Nothing outside the provided material.

**E. Test selection.** For statistics modules, read `references/hypothesis-test-tree.md` and produce the decision-tree walkthrough grounded in the data properties named in the course material, with the invalidating assumption per test.

## Hard rules

- Where the professor's method differs from the standard method, only the professor's method appears in solutions; the standard result appears as a flagged exam trap.
- Topics added mid-session go through the topic map again.
- Deliverables contain the material only. No study advice, no closing summary.
