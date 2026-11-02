# Changelog

## 1.1.0 (2026-11-02)

**Added**
- **The course pack** (section 9), for readers who follow a course through a book page by page. Type `pack`, or `notes`, `podcast` or `cards` for one part. It works from the reader's own document, never from general knowledge, and reads every page, using page images when formulas or figures don't extract.
  - **Notes** in the book's order with page references and the book's notation. Each section gets a one-line process phrase, rare CRITICAL marks with reasons, and Trap lines. About one page per four to six pages of book, with cut material marked "skim in the book". The notes are checked against an inventory of every definition, criterion, formula and procedure.
  - **A walk podcast script**: about 30 minutes (4,000–4,500 words), one fictional professor, written for the ear. It covers history, present-day uses, game changers, leverage points, analogies with their limits, and questions for the walk.
  - **10–15 flashcards** for before the lecture: recall questions, answers with page references, mixed order, a few cards on pages not yet covered, and an optional CSV.
- A test case that builds a course pack from a short excerpt of a stability chapter.

**Changed**
- The description now mentions the course pack and its triggers.
- Sections renumbered: 10 Navigation, 11 Close, 12 Review.

## 1.0.0 (2026-11-01)

First public release.

**Added**
- **Checkpoint before the map.** Each chapter ends with a one-sentence recall prompt, with an optional stretch to name the reasons. The Argument Map follows in the next reply, after editor feedback on the reader's answer.
- **Spaced recall inside the book.** From Chapter 3 on, the checkpoint adds one question about an earlier chapter.
- **`skip`, `flow` and `checkpoints`.** Checkpoints never block the book and can be turned off.
- **Recall card** at the close: 5–7 questions to answer from memory in 2–3 days and again in about a week, with the answers kept out of view.
- **`review`** (section 11): runs a recall card one question at a time and suggests the next review date.
- **"Why it works this way"**, a short section explaining the design to the model.
- Predict before moving a slider in interactive visuals.
- Only sources that were actually opened, or can be named precisely, go on a Sources list.
- **The rebuild challenge is a sibling of the reader's assignment**: same ideas, different specifics.
- A description that says when to use the skill, plus license and version metadata.

**Changed**
- Chapter replies are shorter: the map, doors and questions moved to the reply after the checkpoint (or the same reply in `flow`).
- Sections renumbered (4 Checkpoint, 5 Argument Map, 6 Visuals, 7 Practice blocks, 8 Intuition field guide, 9 Navigation, 10 Close, 11 Review).

**Removed**
- The "What this chapter claimed" paragraph, which duplicated the map's Claim line.

## Before 1.0 (unversioned)

Researched chapters with three source tiers, Argument Map and doors, navigation commands, visuals for things that have shape, practice blocks for technical topics, and the intuition field guide.
