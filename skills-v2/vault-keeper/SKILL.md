---
name: vault-keeper
description: Maintain Omkar's Obsidian vault exactly as his vault rules define it: start at Home, one note per subject, [[wikilinks]], facts only from what he said or logged, unknowns as #gap items in Gaps.md, supersede instead of delete, moves to _to_delete/, raw copies in Sources/ never edited, one line per session in _Log.md. Use whenever he asks to update the vault, add a note, record a fact, "put this in my notes", close a gap, file a source, clean up notes, or whenever another skill (life-os, ship-with-eval, backtest-gatekeeper) needs a vault write outside its own folders. Claude writes the vault; Omkar only reads it.
---

# Vault Keeper

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

The vault is his memory and Claude is its only writer. Read `references/vault-rules.md` before the first write of a session. Lookups start at `Home` and open only the notes the question needs.

## Gate

A write is routine when its source is something Omkar said or logged in this session, quoted or dated, and its target is the one note that owns the subject. It is made, with a wikilink to every note it touches. A write whose source is an inference, a memory, or a guess is ambiguous: it becomes a `#gap` line in `Gaps.md` with the question that would close it, and nothing is written as fact. A gap closes only with his answer and the date.

## Operations

- **Add or change a fact.** Edit the subject's note. Earlier values are superseded with a date ("was 3/week until 5 Oct 2026"), never overwritten silently and never deleted.
- **Open a gap.** Append to `Gaps.md`: `- #gap YYYY-MM-DD [[Subject]]: question`. **Close a gap:** replace `#gap` with `closed YYYY-MM-DD: answer` and write the answer into the subject's note.
- **File a source.** New dated file in `Sources/`. Existing sources are never edited; a corrected copy is a new dated source.
- **Remove.** Nothing is deleted. The file moves to `_to_delete/` and the move is logged.
- **Log.** Every editing session ends with one line in `_Log.md`: `- YYYY-MM-DD: what changed, with [[links]].`

## Hard rules

- A fact about X lives only in X's note. Duplicated facts are a bug; link instead.
- Daily logs go to `Daily/YYYY-MM-DD.md`, Sunday reviews to `Weekly/YYYY-Www.md`.
- Plain language, no em dashes, no filler.
- If no vault tool is available in the session, output each note change as text with its path on the first line, including the `_Log.md` line.
