---
name: exam-study-pack
description: Build FOM exam study materials with enforced rigor - worked calculation guides, MCQ banks with distractor audits, NotebookLM prompt packs, and one-page formula sheets, all scoped strictly to the professor's actual topic list. Use whenever Omkar mentions exam prep, study pack, QDA, MCQs, formula sheet, worked examples, NotebookLM prompts, Klausur, or preparing for any FOM module exam. Also use when he uploads a syllabus, lecture slides, or a professor topic list.
---

# Exam Study Pack

Produces four deliverable types from one gated intake. Never generates study content from memory of "what this subject usually covers".

## Rigor Block (skill-specific, mandatory)

- **Plan-Gate:** No content is generated until the topic map (Step 1) is approved. The plan lists: topics in scope, deliverables requested, estimated item counts. Approval is an explicit yes.
- **Scope-Fence:** Only professor-flagged topics enter the pack. "Nice to know" material is a violation. If a topic seems missing, ask; do not add it silently.
- **Adversarial Verification:** Every worked calculation is recomputed a second time through a different route (or with a check value) before delivery. Every MCQ distractor is attacked: "could a correct-thinking student arrive at this?" Distractors that are accidentally defensible get rewritten.
- **Live-State Truth:** Intake requires the actual syllabus, slide deck, or professor topic list as an uploaded file or pasted text. If none exists, stop and say what is needed. Professor-specific method conventions override textbook defaults (see references/method-conventions.md).
- **Ruthless Editing:** Deliverables contain the material only. No study advice, no motivational framing, no closing summary.

## Step 1: Topic map (gate)

Read the provided syllabus/topic list. Output a table: topic | professor-flagged? (cite where) | requested deliverables | item count. Stop for approval.

## Step 2: Generate approved deliverables

### Mode A: Worked calculation guides
Per topic: problem statement, step-by-step solution with every intermediate value shown, a self-check value at each stage ("your running sum should now be 247.5"), and the one trap students hit. Recompute independently before delivery (Adversarial). For any quartile/percentile work, read references/method-conventions.md first.

### Mode B: MCQ bank (OMR multi-answer format)
Read references/mcq-format.md. Multi-answer format: each question has 4-5 statements, any subset may be true. After generating, run the distractor audit on every item and fix failures before delivery. Deliver as question bank + separate answer key with one-line justifications.

### Mode C: NotebookLM prompt pack
Convert the approved topic map into ready-to-paste NotebookLM prompts (audio overview prompts, quiz prompts, targeted deep-dive prompts per weak topic). Output prompts only, in copy blocks.

### Mode D: Formula sheet
One page maximum. Each formula: name, formula, when-to-use condition, the one trap. Nothing that isn't in the provided materials.

### Mode E: Test selection (statistics modules)
When the exam involves choosing statistical tests, read references/hypothesis-test-tree.md and produce a decision-tree walkthrough grounded in the data properties named in the course materials, with the invalidating assumption stated for each test.

## Hard rules

- If the professor's method for a calculation differs from the standard method (documented in references/method-conventions.md), the professor's method is the only method shown in solutions; the standard method appears only as a flagged "exam trap" note.
- MCQ answer keys are generated in the same pass as questions, never reconstructed later.
- If asked to expand beyond the approved topic map mid-session, re-run the gate for the new topics.
