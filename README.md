# claude-plugins

Personal productivity plugins for Claude. Most are Notion-based, **guided and approval-gated**: Claude proposes, you approve, and Notion holds the state.

## Plugins

| Plugin | One-line purpose | Guide |
|---|---|---|
| **research-notion** | Brief → Plan → Execute research, saved in Kutatások; query, extend, distil to zettels | [guide](guides/research-notion.md) |
| **storyline-notion** | Presentation storyline and slide guide | [guide](guides/storyline-notion.md) |
| **visualisation-notion** | Design-system digest and visual concepts with Claude Design prompts | [guide](guides/visualisation-notion.md) |
| **strategist-notion** | Fact-based strategy with evidence, options, roadmap and visuals | [guide](guides/strategist-notion.md) |
| **concept-notion** | Develop ideas from Seed to Ready in a concept library | [guide](guides/concept-notion.md) |
| **authoring-notion** | Write in your voice, review documents, strategic overviews | [guide](guides/authoring-notion.md) |
| **educator-notion** | Personal tutor with learner model, hint-ladder coaching | [guide](guides/educator-notion.md) |
| **learn-notion** | Learning paths, quizzes, flashcards and spaced repetition | [guide](guides/learn-notion.md) |
| **pdf-publisher** | Branded, print-ready PDFs from folders or Notion (local engine) | [guide](guides/pdf-publisher.md) |
| **pdf-to-notion** | Convert PDFs into structured Notion pages (local engine) | [guide](guides/pdf-to-notion.md) |

## Repository contents

The plugins are stored as packaged archives in `plug-ins/`:

| File | Plugin |
|---|---|
| `plug-ins/research-notion.plugin` | research-notion |
| `plug-ins/storyline-notion.plugin` | storyline-notion |
| `plug-ins/visualisation-notion.plugin` | visualisation-notion |
| `plug-ins/strategist-notion.plugin` | strategist-notion |
| `plug-ins/concept-notion.plugin` | concept-notion |
| `plug-ins/authoring-notion.plugin` | authoring-notion |
| `plug-ins/educator-notion.plugin` | educator-notion |
| `plug-ins/Learn notion-0.1.0-v1.zip` | learn-notion |
| `plug-ins/pdf-publisher.plugin` | pdf-publisher |
| `plug-ins/pdf-to-notion.zip` | pdf-to-notion |

`guides/` holds a newcomer how-to for each plugin.

## How the plugins work

Every plugin has a `.claude-plugin/plugin.json` manifest and a `skills/` folder. Each skill is a `SKILL.md` plus a `references/` folder of templates and conventions.

- **Entry skill and phase skills.** One entry skill (for example `research` or `strategist`) picks the flow and hands off to the phase skills.
- **Gates.** Most plugins run **Brief → Plan → Make**. Claude stops at each gate until you explicitly approve. Edits are not approval.
- **Notion is the state.** Pages are re-fetched before each phase, so you can edit them in Notion at any time.
- **No hard-coded locations.** You choose where output goes, and Claude confirms it.
- **No deletes.** The Notion connector can't delete pages, so retired pages get a `[removed] ` title prefix.
- **No invented facts.** Gaps appear as `[NEEDS: …]`.

## Requirements

- The Notion connector enabled in Claude. `research-notion` and `learn-notion` ship an `.mcp.json` pointing to `https://mcp.notion.com/mcp`.
- `pdf-publisher` and `pdf-to-notion` also need Python 3.10+ and their engine's `requirements.txt`. See their guides.

## Installing

Install each archive through your Claude app's plugin installation flow (Cowork / Claude desktop). Then invoke a plugin by describing the task ("start a new research…") or via its entry skill. `pdf-to-notion` also has a `/pdf-to-notion` command.

## Notes

- All plugins are at version 0.1.0.
- `pdf-to-notion` uses PyMuPDF (AGPL / commercial). Check the licence before distributing.
- Notion-side behaviour was developed against connector documentation and simulated responses. Run the first preview or pilot step before trusting a large batch.
