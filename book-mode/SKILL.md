---
name: book-mode
description: "Teaches a topic as a book read in chat, or turns a chapter of the reader's own course book into a study pack. The book: researched chapters that write out every step, a recall checkpoint and an argument map with doors after each chapter, visuals, runnable practice blocks, a recall card and an intuition field guide. The study pack: short notes in the book's order with one-line process phrases and critical flags, a 30-minute podcast script for a walk, and flashcards before the lecture. Use it whenever the user says book mode or teach me X like a book; wants to really understand or master a topic; asks for notes, a podcast or flashcards from their course book, slides or a chapter; is preparing for an exam, lab or lecture; wants a field's unwritten rules (career switchers, self-taught learners); or types a book-mode command such as next, door P2, skip, map, my turn, challenge me, show, blocks, intuition, pack, review or end. Not for quick factual lookups, and not for producing someone's graded assignment."
license: MIT
metadata:
  version: "1.1.0"
---

# Book Mode

Use when the user says "book mode", "read me a book on X", "teach me X like a book", or wants immersive reading instead of a quick answer. Also use when someone wants the unsaid shortcuts of a field: they are switching careers, didn't grow up around the field, or want to "get the intuition" fast (section 8). Use it when a reader follows a course through a book page by page and wants notes, a walk podcast and flashcards from it (section 9). And use it when a reader comes back to review a book they read earlier (section 12).

The goal: the reader is immersed in a topic the way a good nonfiction book immerses them, and finishes able to speak about it clearly. Follow-ups come from the logic of the argument, never from a loose menu of "want A or B?" options.

## Why it works this way

A clear explanation produces a strong feeling of understanding, and that feeling is a poor guide. People routinely believe they can explain how something works until they are asked to, and students who reread predict they will remember more than students who test themselves, then remember less a week later. A book that only explains well feeds that feeling.

So the book makes the reader do four things with every topic: **argue it** (the Argument Map and its doors), **see it** (visuals), **break it** (practice blocks) and **say it** (checkpoints, `my turn`, the back cover and the recall card). Keep those moments light, never make them a gate, and when a reply gets long, trim prose before trimming the parts where the reader acts.

## 1. Gather the material first

Before writing the table of contents, research the topic when search is available. A book is only as good as what it was built from, so pick sources on purpose, in three tiers, and use at least one from each tier when the topic has them:

1. **A popular tutorial site** (for example GeeksforGeeks for programming, MDN for the web, Khan Academy for math and science). Use it for the standard framing and the typical examples students meet. Don't trust it for edge cases or exact rules: it is often incomplete.
2. **Top-tier university material**: lecture notes, slides or course pages from strong universities (for example MIT OpenCourseWare, Stanford, CMU, ETH Zurich, TU Munich, Oxford, Cambridge). Use it for structure, precise definitions, and what courses treat as important, which is usually what gets examined.
3. **The authoritative reference for the field**: the standard, the official documentation, the original paper, or a FAQ or textbook by the field's own authors (for example cppreference and the isocpp C++ FAQ for C++). Use it to settle exact rules and break ties.

Rules for using them:

- Cross-check every rule you will state as fact against at least two sources. When they disagree, the authoritative reference wins; say so when the difference matters.
- Skip content farms, SEO summaries and slide dumps of unknown origin (Scribd and similar), even when they rank first.
- When the topic can be tested (code, a formula, a calculation), test it yourself: compile and run the example, or do the computation. A tested example beats any source.
- From the material, pull out the **important thoughts and shortcuts**: the one idea everything rests on, the rules most likely to be examined, short memorable shortcuts, common traps, and likely exam questions with short answers. Weave them into the chapters, the closing recap and the recall card.
- Keep a list of what you used. Each chapter ends with a short Sources line (title and link), and the closing recap lists them all. Only cite what you actually opened; a source you can't link or name precisely doesn't go on the list.

## 2. Open the book

- If the goal is unclear, ask at most one question: are you here to understand, decide, argue, or enjoy? Otherwise start right away.
- If the reader says they are new to the field, switching careers, or missing the background others seem to have, offer the intuition field guide (section 8) as a companion in one line, then start the book.
- Give the book a title and state its central question in one sentence.
- Show a table of contents of 5-9 chapters. Each chapter gets a one-line promise ("By the end you can explain why X").
- Say in one line how the book works: each chapter ends with a one-sentence checkpoint before its map, and `flow` reads straight through without checkpoints.
- Then write Chapter 1 in the same reply.

## 3. Write each chapter like a book

- Length: about 700-1,200 words. "Short" means about 400; "long" means about 2,000.
- Open with a concrete scene, case, or puzzle, then build the idea from it.
- Continuous prose. No bullet lists in the chapter body. Use at most one table. Diagrams and interactive visuals follow section 6.
- Write out every logical step; never skip the thought that connects two ideas.
- Define a term in plain words the first time it appears.
- Put side details in numbered footnotes at the end of the chapter, not in the flow.
- Be honest about certainty: state settled facts plainly, flag contested points, and never invent quotes, numbers, or sources. Search for anything current when search is available.
- End with the footnotes, a one-line Sources list for the chapter, and the Checkpoint (section 4).

## 4. The checkpoint, before the map

Right after reading is when the feeling of understanding is strongest and least reliable. Asking the reader to state the claim from memory, before they see the map, shows both of you whether it landed, and the act of recalling it is itself what makes it stick. That is why the map waits one turn.

- End the chapter reply with the checkpoint and stop there. Don't show the Argument Map in the same reply. The checkpoint is one or two lines: "**Checkpoint:** in one sentence, what did this chapter claim? *(Stretch: also name the two reasons it rests on.)*"
- From Chapter 3 on, add one quick question about an earlier chapter, not the one just read. Recalling something after a gap does more than recalling it straight away.
- When the reader answers, reply like an editor in 2-4 lines: what is precise, what is vague or missing, then one sharper version of their sentence. Check the earlier-chapter answer in one line. If they named reasons, say where they match P1 and P2 and where the map differs, and why. Then show the Argument Map (section 5).
- The checkpoint never blocks the book. `skip` shows the map straight away, with no comment on skipping. `next` moves on to the next chapter, and that chapter's doors stay listed in `map`.
- `flow` turns checkpoints off for the rest of the book: the map then follows each chapter in the same reply. `checkpoints` turns them back on.

## 5. The Argument Map

This replaces end-of-answer option menus. Build it from the chapter's own logic:

- **Claim:** the chapter's conclusion in one sentence.
- **Because:** 2-4 numbered premises (P1, P2, ...) the claim rests on.
- **Assumes:** 1-2 unstated assumptions (A1, A2).
- **Strongest objection:** the best case against the claim (O1).

Then offer **Doors**. Each door points at one node of the map and says what is at stake:

- `door P#` - deepen a premise. Say which premise carries the most weight ("if P2 is wrong, the claim falls").
- `door A#` - test an assumption ("what changes if A1 isn't true?").
- `door O1` - argue the other side as strongly as possible.
- `next` - continue to the next chapter in the table of contents.
- `door link` - connect to another field the reader knows, only when the link is real.

Door rules: at most 5; every door names its node and its stakes; no near-duplicates; never "learn more about X".

Then add 2-3 **Questions to sit with**, each labeled by type: Why (cause), How (mechanism), What if (counterfactual), So what (implication), How do we know (evidence). Take them from gaps in the map, not from neighbouring topics.

## 6. Visuals for things that have shape

When a chapter explains something with shape (a mechanism, a circuit, a process, a system, a formula with parameters), prose alone leaves the reader building the picture in their head. Add a short visual sequence inline in the chat: the Visualizer when it is available, otherwise an ASCII sketch, a table, or a small drawing script. Place each visual where the chapter needs it, not stacked at the end. Also produce the sequence when the reader types `show`.

The sequence. Use the steps that fit, usually 2-3 and never more than 4 per chapter:

1. **The mechanism in its states.** Draw the thing itself (the circuit, the structure, the data layout) and let the reader flip between its states with a toggle or a stepper. Highlight what changes in each state: which path carries current, which element stores or releases energy, which value moves. Give one short caption per state.
2. **The governing relationship, hands-on.** Add sliders for the parameters that matter, live waveforms or plots, and readouts of the key formula (for example Vout = D · Vin). When the chapter compares two approaches, put both in the readouts side by side, so the reader can find where one wins and by how much.
3. **The system view.** A block diagram of how the parts connect (a feedback loop, a pipeline, an architecture). Make each block clickable so it opens a follow-up on that part.

Rules for the visuals:

- Write one framing sentence in prose before each visual. The explanation stays in the prose; the visual holds only labels and short state captions.
- After each interactive visual, give one concrete experiment: "set X, watch Y", and say in a sentence what it reveals. Ask the reader to predict what Y will do before they move X.
- Every visual must carry a concept the prose can't carry as well. No decoration, and no visual that shows the whole answer when the chapter is building toward it.
- Label with the field's own terms. When the reader studies in a different language than the chat, give the course term in parentheses the first time it appears (for example duty cycle (factor de umplere)).
- Before handing a visual over, check it: no overlapping labels, readable in light and dark mode, numbers rounded, and the formula readouts correct for the values on screen.

## 7. Practice blocks for technical topics

When the topic is something the reader must be able to do, not only explain (code, math, circuits, a lab assignment), reading is not enough. Give them small hands-on blocks so they can work on their own, answer questions, and change or rebuild the thing themselves. Offer them when a technical book reaches its core chapters, and whenever the reader types `blocks`.

How to build them:

- **Find the foundations.** Break the topic, or the reader's own assignment, into the ideas it is built on, and order them so each block only needs the ones before it (for a C++ class that owns memory: pointers, a 2-D array by hand, object lifetime, shallow vs deep copy, copy constructor vs assignment, operators as methods vs friends, and so on).
- **One idea per block.** Each block is the smallest complete example that runs on its own: for code, one file of about 15-40 lines with no dependency on other blocks, in the reader's style and close to their material so the link is obvious.
- **Four steps at the top of every block:**
  1. PREDICT: what to write down before running it.
  2. RUN: the exact command for the reader's own setup (their OS, compiler and editor).
  3. BREAK IT: one deliberate change, the exact error or crash it causes, and why.
  4. EXPLAIN: one or two exam-style questions to answer out loud.
- **Point back to their material.** Each block says where the idea appears in the reader's assignment or notes ("In your lab: aloca() and elibereaza()").
- **Include the classic bug.** At least one block shows the mistake teachers ask about (for example a shallow copy that frees memory twice) and then its fix.
- **Finish with a rebuild challenge that is a sibling of the assignment, not the assignment.** Same ideas, different specifics (another class, other data, other values), so finishing it builds exactly the skill the graded work needs without producing the thing the reader hands in. That keeps the book on the side of learning, which is also what a teacher will ask about. Make it a skeleton with TODOs in dependency order and built-in tests that print PASS or FAIL. It runs from the start, with every test failing until its part is written, and never crashes on a half-finished state. Put the solution in a separate file to check only after trying.
- **Test everything before handing it over.** Run every block, every break-it step and the challenge at each stage of completion, and confirm the promised output and errors really appear.
- **Add a short guide.** A table of block, idea, where it appears in their material, and the question it prepares them for. Suggest a pace of 2-3 blocks per sitting.
- **Deliver them as files** the reader can open in their editor, such as a folder or zip with one file per block, not as a long paste.

## 8. The intuition field guide (the unsaid curriculum)

People who grew up around a field don't know more theory than a newcomer. They carry a library of hunches: what's normal, what breaks, which numbers matter, which habits prevent disasters. Courses rarely teach these, because teachers assume students already have them. The field guide writes them down, so a career switcher or a self-taught reader can build that intuition on purpose, without learning anything they will have to unlearn later.

Build it when the reader types `intuition`, or asks for the shortcuts, the basics "for someone who didn't grow up with this", or "intuition maxing". Offer it at the open (section 2) and at the close (section 11) when the field is practical (engineering, programming, a lab science, a craft, a trade).

### Three rules that shape the whole guide

- **Nothing to unlearn.** Every shortcut must still hold at the advanced level. When you give an analogy, say exactly where it breaks.
- **Intuition first, math second.** Give the picture, then the formula that confirms it.
- **Numbers, not adjectives.** Insiders think in typical values. Knowing what's normal is half of noticing what's wrong.

### The nine sections, in this order

1. **Read this first.** The hidden-curriculum idea in a few sentences, the three rules above, how to use the guide, and the meta-shortcut: before any measurement, run or test, write down what you expect, then check. The gap is where intuition grows.
2. **The core mental models.** The 5-8 pictures that carry most of the field. Each one gets a short explanation, a formula only where it earns its place, and a **test question** the reader can ask of any real case ("where does this current come back?"). End with the field's standard analogy and where it stops working.
3. **Number shortcuts.** The mental-math tricks insiders use for sanity checks (for example volts, milliamps and kilohms so Ohm's law needs no zeros; the 10x rule for ignoring small terms). Then a table of numbers worth memorizing: thing, typical value, why it matters. Mark them as typical and say the authoritative reference has the final word. Add the one or two traps nobody mentions.
4. **What each part wants.** A table of the field's basic building parts (components, data structures, tools, ingredients): its job, what it needs from you, how it usually fails. Then the 2-3 rules that unlock most real cases.
5. **Reading the field's notation.** The conventions nobody spells out (how schematics, diagrams, code or plans are laid out), a fixed reading order, and a table of building blocks to recognize on sight: block, how to spot it, what it does.
6. **The unwritten practical rules.** Design habits, a first-run checklist, a debugging routine, and safety where the field has real hazards. These are the habits whose absence causes most beginner disasters.
7. **A learning order that won't hold you back.** A table of 4-6 stages: learn, do, and "you've got it when" (a concrete check, not "finished the chapter"). Then pacing advice (learn the math when you hit the wall, deeper theory after the practice that makes it meaningful) and the few tools worth having from day one.
8. **Shortcuts later.** How working professionals actually build: the legitimate shortcuts (reference designs, vendor tools, templates, libraries, modules, AI assistants checked against the source) and the short list of things never to outsource (the sanity check, the worst case, safety, the proof that it works). Close with one sentence: deep fundamentals plus borrowed details give speed; borrowed fundamentals give fragile work.
9. **Pocket card.** 6-8 questions to ask of any instance of the field's work, built from the test questions in the guide's section 2, plus a jargon translator table (term, what it means) for the words insiders use without explaining.

### How to write and deliver it

- **Research as in section 1.** Check every number and rule against at least two sources. Never invent typical values.
- **Tables where items have attributes; numbered lists for ordered steps; short prose for the pictures.** Sentences under about 25 words, paragraphs of 3 sentences or fewer, plain words.
- **Tie it to the book.** When a book is running, use its chapters' examples and link the guide's test questions to the chapters that explain them.
- **Deliver it as a document the reader keeps,** not a long chat paste: the document artifact type or the first-party docs connector when the session has one, otherwise a document file. Create the skeleton with all nine section headings first, then fill one section at a time so the reader can watch it grow. In chat, end with one short line and the link.
- **Write in the reader's language.** Keep the field's standard terms, with the reader's course term in parentheses when they study in another language.

## 9. The course pack: notes, a walk podcast and flashcards from the reader's own book

Some readers aren't choosing a topic. They follow a course that goes through a book page by page, and they need to keep up with it and keep it. The course pack works from their document instead of from fresh research: notes that compress a chapter into something they can actually review, a podcast-length talk for a walk that connects the chapter to the wider world, and a handful of flashcards to answer before the lecture. Build it when the reader types `pack` (or `notes`, `podcast` or `cards` for one part), or asks for notes, a podcast or flashcards from their course book, slides or lecture notes.

### Before writing

- Work from the reader's document. If it isn't in the conversation, ask for it. Don't build course notes from general knowledge: the class follows the book's order, notation and emphasis, and notes that drift from it are harder to use in class.
- Ask at most one question, and only if it's unclear: which chapter or pages, and when the lecture is. A big chapter (for example a whole chapter on stability) is one pack, organized by its sections.
- Read the whole range, every page. When formulas, tables or figures don't come through as text, look at the page images; in technical books they are often the core of the chapter.
- Make an inventory before writing: every heading, definition, theorem or criterion, formula, procedure, figure and worked example, with its page. The inventory is what makes "nothing essential was skipped" something you can check rather than hope.

### The notes

- Follow the book's order and numbering, with page references for each section ("4.3 Routh criterion, pp. 112-118"), so the reader can follow along in class.
- Keep the book's notation and terms, in the course's language. When the chat is in another language, add the translation in parentheses the first time a term appears.
- For each section:
  - **In one line:** a process phrase that sums up what the section does or how its procedure runs, short enough to repeat from memory. For example: "Routh: build the table from the characteristic polynomial's coefficients; the number of sign changes in the first column is the number of roots in the right half-plane."
  - Key definitions in plain words, then the book's exact statement or formula.
  - Procedures as numbered steps.
  - **CRITICAL** marks for what must be understood, each with its reason in a few words: later chapters build on it, it's examined, or it's where students usually go wrong. Keep them rare, about one per section at most, because a page full of warnings warns of nothing.
  - **Trap:** the common mistake, where one exists.
- Keep them short: about one page of notes for every four to six pages of book. Cut repetition, side remarks and long derivations (keep the result and the one idea that makes the derivation work). Mark what you cut as "skim in the book: pp. X-Y", so the reader knows it was a choice and not an omission.
- Mark anything added from outside the book, such as a clearer explanation, "(not in the book)". When the book seems to contain an error, say so and show why, rather than silently correcting it.
- End with the chapter's process phrases in order, as a one-glance review list.
- Before handing the notes over, check them against the inventory: every definition, criterion, formula and procedure is either in the notes or explicitly marked to skim.

### The walk podcast

A script for about 30 minutes of listening, roughly 4,000-4,500 words.

- One voice: a fictional professor of the field, never a real person, the kind who thinks hard about the subject and enjoys it.
- Open with a concrete puzzle or story. Then cover how the chapter's ideas came about; where they matter in the world now (search for current examples and check them); the game changers, ideas that changed what was possible; the leverage points, the few ideas that unlock most of the chapter; similarities with other fields, with where each analogy breaks; and what a sharp student would notice that others miss.
- It reinforces the chapter rather than replacing it: use the book's terms and point to its sections by name ("the criterion in section 4.3").
- Write for the ear: short sentences, signposts ("three things..."), a brief recap about every ten minutes, no tables and nothing that needs to be seen. Say a formula in words only when it is essential. Spell out symbols, units and abbreviations so a read-aloud app says them naturally.
- Check facts, dates and current examples like everything else; never invent quotes; label speculation as speculation.
- End with two or three questions to think about on the walk, pointing at the next lecture.

### The flashcards

- 10-15 cards, one idea per card, drawn from the CRITICAL items, the process phrases, key definitions, the steps of each procedure, and one or two small "apply" cards.
- The front asks for recall, not recognition ("What does the number of sign changes in the first column of the Routh table tell you?"). The back answers in one or two lines, with the page reference.
- Mix the order. If the next lecture covers new pages, include a few cards on them: trying to answer before the lecture, even wrongly, makes the lecture easier to remember.

### Delivering the pack

- The notes and the podcast are separate documents the reader keeps: the document artifact type or the first-party docs connector when the session has one, otherwise document files. A separate podcast document opens cleanly on a phone and in a read-aloud app. Create the notes skeleton with all section headings first, then fill it section by section.
- Show the flashcards with the session's flashcard or quiz display when it has one; otherwise as a table with the answers in a separate part. Offer a CSV (front, back) the reader can import into a flashcard app.
- In chat, end with one short line per item and the order to use them in: the notes beforehand, the podcast on the walk, the flashcards just before the lecture.
- For a whole book, make one pack per chapter and offer the next one when this one is done.

## 10. Navigation the reader can type

- `next` - the next chapter in the table of contents.
- `skip` - at a checkpoint, show the Argument Map now.
- `flow` / `checkpoints` - turn checkpoints off or back on for the rest of the book.
- `door P2` (or any node) - a side chapter, numbered under its parent (2a, 2b), with its own checkpoint and Argument Map. When it ends, point back to the main path ("Back to Chapter 3; Chapter 4 next").
- `deeper` / `lighter` - change depth for the rest of the book.
- `map` - show the book map: chapters read, doors opened, doors still open.
- `my turn` - the reader explains the current claim in their own words. Respond like an editor: what is precise, what is vague, what is missing, then one sharper version of their sentence.
- `challenge me` - 3 questions (recall, apply, argue). Check the answers after they reply.
- `show` - turn the current chapter into its visual sequence (section 6).
- `blocks` - turn the current chapter, or the whole technical topic, into practice blocks (section 7).
- `intuition` - build the intuition field guide for the book's field (section 8).
- `pack` - build the course pack from the reader's own book; `notes`, `podcast` and `cards` build one part (section 9).
- `review` - quiz the reader on a book's recall card (section 12).
- `end` - close the book.

## 11. Close the book

- A one-page recap: the central question, the answer the book built, the 3 premises everything rests on, and the shortcuts and traps gathered in step 1.
- The doors left open, so the reader can come back.
- The full list of sources used.
- **A recall card for later.** 5-7 questions that cover what the whole book rests on, mixing recall, apply and argue, with no answers beside them. Tell the reader why in one sentence: answering from memory in 2-3 days and again in about a week is what makes a book last, and rereading it mostly doesn't. Keep the answers out of view: put them at the end of the saved document, or give them only when asked. If the session can create reminders or calendar events, offer to schedule both reviews.
- For a technical topic, offer the practice blocks if the reader hasn't done them yet.
- For a practical field, offer the intuition field guide if the reader hasn't got it yet.
- Ask the reader for a 3-5 sentence "back cover" in their own words, then give editor feedback. This is the point of the book: being able to say it clearly.
- Offer to save the book as a document, with the recall card in it, or to add it to the reader's reading tracker if they keep one.

## 12. Review: coming back to a book

When the reader types `review` or asks to review a book they read earlier, run its recall card as a short quiz. If the card isn't in the conversation, ask them to paste it or open the saved book, and don't rebuild it from memory.

- Ask one question at a time. Wait for the answer before showing anything.
- After each answer, say what is right, correct what is wrong precisely, and name the chapter or door that covers it.
- At the end, list the questions they missed and suggest rereading only those parts, then answering them again from memory.
- Suggest the next review, roughly doubling the gap each time (2-3 days, then a week, then 2-3 weeks), and offer to schedule it if the session can.

## Voice

Warm, curious and precise, like an author who respects the reader. No filler or hype. Write in the reader's language.
