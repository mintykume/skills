# Book Mode

**A book you can argue with.** Book Mode is an Agent Skill that turns any topic into a book you read in chat, then makes you show that you understood it. If you follow a course through a book page by page, it also turns each chapter into a study pack: short notes, a podcast for your walk, and flashcards for before the lecture.

Version 1.1.0 · [Changelog](CHANGELOG.md) · [Sample session](examples/sample-session.md) · MIT license

## Why it exists

AI made explanations free, and that made the *feeling* of understanding cheap. That feeling is a poor guide:

- People rate how well they understand everyday mechanisms, like a zipper, then rate themselves lower after trying to explain them step by step (Rozenblit & Keil, 2002).
- Students who reread a passage four times predicted they would remember it better than students who read it once and recalled it three times. A week later they remembered 40% against 61% (Roediger & Karpicke, 2006).
- In a field experiment with about 1,000 high-school math students, a plain ChatGPT-style assistant raised practice scores by 48% but lowered exam scores without AI by 17%. A version with guardrails raised practice scores by 127% and caused no exam drop (Bastani et al., 2025).

The design decides whether AI helps or harms. So Book Mode makes you do four things with every topic: **argue it, see it, break it, say it.**

## How a session goes

1. You type `book mode: <topic>`.
2. It researches in three tiers (a popular tutorial site, university course material, the field's authoritative reference), cross-checks what it will state as fact, and runs any code or math itself.
3. It opens the book: a title, the central question, and 5–9 chapters, each with a one-line promise.
4. Each chapter is real prose. It opens with a concrete case, writes out every step, defines terms in plain words, and lists its sources.
5. A chapter ends with a **checkpoint**: one sentence, from memory, saying what it claimed. You get editor-style feedback, then the **Argument Map**: the claim, the premises it rests on, its hidden assumptions, the strongest objection, and **doors** that let you dig into any of them.
6. Along the way you can ask for visuals of anything that has a shape (`show`), runnable practice blocks (`blocks`), and an intuition field guide to the field's unwritten rules (`intuition`).
7. At the end: a one-page recap, a **recall card** to answer in a few days, and your own 3–5 sentence "back cover". Come back later with `review`.

See [examples/sample-session.md](examples/sample-session.md) for a real, abridged session.

## The course pack

For when your class goes through a book page by page and you need to keep up. Type `pack` and give it the chapter (your PDF, document or slides). It reads every page, lists every definition, criterion, formula and procedure, and checks the finished notes against that list, so nothing essential is skipped silently. You get:

- **Notes** in the book's order, with page references and the book's own notation. Each section opens with a one-line **process phrase** you can repeat from memory, such as *"Routh: build the table from the characteristic polynomial's coefficients; the number of sign changes in the first column is the number of roots in the right half-plane."* A few **CRITICAL** marks show what must be understood, each with its reason, and **Trap** lines show the usual mistakes. About one page of notes for every four to six pages of book. Anything left out is marked "skim in the book" with its pages.
- **A 30-minute podcast script** for your walk: a fictional professor on how the ideas came about, where they matter now, the game changers and leverage points, links to other fields (and where those links break), and what a sharp student would notice. It's written for the ear, so a read-aloud app reads it naturally.
- **10–15 flashcards** to answer just before the lecture, with page references, and a CSV you can import into a flashcard app.

Use them in this order: the notes beforehand, the podcast on the walk, the flashcards just before class. Type `notes`, `podcast` or `cards` to build only one part.

## Commands

| Type | What happens |
|---|---|
| `next` | Next chapter |
| `skip` | At a checkpoint, show the Argument Map now |
| `flow` / `checkpoints` | Turn checkpoints off or back on |
| `door P2` (or any node) | A side chapter on that premise, assumption or objection |
| `deeper` / `lighter` | Change depth for the rest of the book |
| `map` | Chapters read, doors opened, doors still open |
| `my turn` | You explain the claim; it edits your explanation |
| `challenge me` | Three questions: recall, apply, argue |
| `show` | The chapter as a visual sequence: states, sliders, system view |
| `blocks` | Runnable practice blocks: predict, run, break it, explain |
| `intuition` | The intuition field guide, as a document |
| `pack` | The course pack from your own book: notes, walk podcast, flashcards |
| `notes` / `podcast` / `cards` | Just one part of the course pack |
| `review` | Quiz yourself on a book's recall card |
| `end` | Close the book |

## Why each part is there

| Part | What it makes you do | What it draws on |
|---|---|---|
| Checkpoint, `my turn`, `challenge me`, recall card, `review` | Pull the idea out of memory, again after a gap | Retrieval practice and spacing (Roediger & Karpicke, 2006) |
| Argument Map and doors | See the logic, and where it could be wrong | Argument mapping. The evidence comes from learners who build maps themselves; here you check and extend one, and can draft its premises at the checkpoint |
| Predict → run → break it → explain | Commit to a guess before you see the result | Prediction and learning from errors |
| Visuals with states and sliders | Find the relationship yourself: set X, predict, watch Y | Learning from words plus pictures |
| Three-tier sources, cross-checks, running the code | Trust what you're reading | Accuracy; a well-designed AI tutor at Harvard used pre-written solutions for the same reason (Kestin et al., 2025) |
| Intuition field guide | Get the hunches insiders never explain | The "hidden curriculum": what courses assume you already have |
| Course terms in parentheses | Connect the book to your own course | For people who study in one language and read in another |
| Process phrases and CRITICAL marks | Hold a whole procedure in one sentence; spend attention where it matters | Compressing steps into a chunk you can recall; marks kept rare so they still mean something |
| Walk podcast | Hear the chapter again, a few hours later, connected to history, the present and other fields | A second, spaced pass that links new ideas to what you already know |
| Flashcards before the lecture | Try to answer before you're taught, even if you get it wrong | Pre-testing: a failed attempt makes the explanation that follows easier to remember |

## Install

- **Claude Code:** copy the `book-mode` folder into `~/.claude/skills/` (all projects) or into `.claude/skills/` inside a project.
- **Claude apps:** zip the `book-mode` folder and add it as a custom skill in your settings.
- **Other agents that read `SKILL.md` skills:** put the folder in their skills directory (for example `.github/skills/` for GitHub Copilot).

Then type `book mode: <topic>`.

## Limits

- **Not tested as a whole yet.** Each part draws on research; the combination hasn't been tested in a study. A small pilot is planned, and its results will go here whichever way they come out.
- **Still mostly reading if you skip every checkpoint.** The active parts never block you, so it's possible to read straight through and get the false sense of understanding the book is built against.
- **Sources can still be wrong.** The three-tier rule reduces errors; it doesn't remove them. Check the sources that matter to you.
- **Visuals depend on the app.** Where interactive visuals can't render, it falls back to sketches and tables.
- **Course notes are only as good as the pages it can read.** It reads formulas and figures from page images when they don't come through as text, but check the CRITICAL parts against your book.
- **The podcast is a script, not audio.** Play it with a read-aloud app.
- **It teaches assignments, it doesn't do them.** Practice blocks use the ideas of your graded work with different specifics, so the rebuild challenge is never the thing you hand in.

## Tests

[`evals/`](evals/) holds six test cases: opening a book with a checkpoint, the Argument Map in `flow` mode, the intuition field guide for a career switcher, practice blocks with a sibling challenge, `review` asking one question at a time, and a course pack built from a short excerpt of a stability chapter. With Claude Code, run them from this folder with `claude plugin eval . --allow-tools Write,Edit,Bash,WebSearch,WebFetch`. That runs each case with and without the skill, as real (billed) model runs.

Status: the cases are written; results will be published here after the first run.

## References

- Rozenblit, L., & Keil, F. (2002). The misunderstood limits of folk science: An illusion of explanatory depth. *Cognitive Science*, 26(5), 521–562.
- Roediger, H. L., III, & Karpicke, J. D. (2006). [Test-enhanced learning: Taking memory tests improves long-term retention](https://psychology.ecu.edu/wp-content/pv-uploads/sites/216/2019/03/Roediger-Karpicke-2006.pdf). *Psychological Science*, 17(3), 249–255.
- Bastani, H., et al. (2025). Generative AI without guardrails can harm learning: Evidence from high school mathematics. *PNAS*, 122. [Summary (Wharton)](https://knowledge.wharton.upenn.edu/article/without-guardrails-generative-ai-can-harm-education)
- Kestin, G., Miller, K., Klales, A., Milbourne, T., & Ponti, G. (2025). [AI tutoring outperforms in-class active learning](https://pmc.ncbi.nlm.nih.gov/articles/PMC12179260/). *Scientific Reports*, 15, 17458.

## License

MIT. See [LICENSE](LICENSE).
