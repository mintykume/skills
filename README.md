# skills

Agent Skills by lucidbloom: small, tested instruction sets that make AI assistants teach and decide better. Each folder is a self-contained skill with its own README, examples and test cases.

| Skill | What it does | Version |
|---|---|---|
| [book-mode](book-mode/) | Turns any topic into a book read in chat, then makes you argue it, see it, break it and say it back. Also turns a chapter of your course book into notes, a walk podcast and flashcards. | 1.1.0 |
| [project-navigator](https://github.com/mintykume/project-navigator) *(own repo)* | Helps decide what to work on next: whether an idea is worth pursuing, whether it already exists, and the smallest useful next experiment. | see repo |

## Install a skill

- **Claude Code:** copy the skill's folder into `~/.claude/skills/` (all projects) or `.claude/skills/` inside a project.
- **Claude apps:** zip the skill's folder and add it as a custom skill in your settings.
- **Other agents that read `SKILL.md` skills:** put the folder in their skills directory (for example `.github/skills/` for GitHub Copilot).

## How skills here are held to a standard

Every skill ships with a README that says what problem it solves and where it falls short, an example session, a changelog, and test cases in `evals/`. Skills with scripts or their own test suites, like Project Navigator, live in their own repositories.

## License

MIT. See [LICENSE](LICENSE).
