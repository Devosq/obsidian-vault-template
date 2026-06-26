# Required Obsidian Plugins

The templates in `Templates/` use Templater syntax (`<% tp... %>`) and Dataview
queries (```` ```dataview ````). **They will not work without these community
plugins installed and enabled.**

## Essential (templates break without these)

| Plugin | Why | Used in |
|--------|-----|---------|
| **Templater** (`templater-obsidian`) | Resolves `<% tp.date.now() %>`, `<% tp.file.title %>` | every template |
| **Dataview** | Resolves the ```` ```dataview ```` query blocks | `Asiakas.md`, `Päivittäinen.md` |

## Recommended (referenced by the workflow)

| Plugin | Why |
|--------|-----|
| **Calendar** (`calendar`) | Daily-note navigation for `Päivittäinen.md` |
| **Tasks** (`obsidian-tasks-plugin`) | Checkbox/task queries |
| **Kanban** (`obsidian-kanban`) | Board views over projects |

## Setup

1. **Settings → Community plugins → Browse** → install the plugins above.
2. Enable them.
3. **Settings → Templater → Template folder location** → set to `Templates`.
4. (Optional) Templater → enable "Trigger Templater on new file creation" so new
   notes auto-apply the matching template.
5. Copy `structure/` folders into your vault for the taxonomy.

`.obsidian-community-plugins.json` in this repo lists the essential plugin IDs —
you can drop its contents into your vault's `.obsidian/community-plugins.json`
(merge with anything already there) to install them in one step, then enable.

## How Claude Code uses this vault
- Writes session summaries into `Päiväkirja/YYYY-MM-DD.md` after milestones.
- Reads `Strategia/` for business context.
- See the `claude-md-template` repo (Memory + Diary section) for the wiring.
