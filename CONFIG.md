# Configuration and event viewer

[简体中文](CONFIG.zh-CN.md) · [Back to the game](README.md)

This is a configuration snapshot for v0.2.3-playtest.4, shared for reading, analysis, and design discussion. It contains story spoilers. Game implementation source and the runnable Godot project are not included.

| Path | Contents |
| --- | --- |
| `config/events_vr/` | Base package: registry, JSON Schema, 40 events and 96 choices |
| `config/registry/items.json` | Definitions for 19 current items, including names, prices, and weight |
| `config/registry/legacy_items.json` | Legacy save compatibility items, not the current shop list |
| `config/shop_catalog.json` | Shop catalog |
| `config/balance.json` | Starting budget, daily costs, and other balance values |
| `config/registry/actions.json` | Action configuration |
| `config/registry/world.json` | World entities and state configuration |
| `config/registry/director.json` | Event director and delivery configuration |

## Use Event Graph Reviewer

My other project, [Event Graph Reviewer](https://github.com/AmethystineAlpaca/event-graph-reviewer), visualizes explicit event/choice prerequisites locally. It requires Python 3.9+, Node.js 20+, npm, and a browser. These tools are not required to play the game.

Run from a common parent directory:

```bash
git clone https://github.com/AmethystineAlpaca/z-shelter-public.git
git clone https://github.com/AmethystineAlpaca/event-graph-reviewer.git
cd event-graph-reviewer
./scripts/dev.sh ../z-shelter-public/config/events_vr
```

The first run installs the viewer's npm dependencies. Open the localhost URL printed in the terminal and keep it running; Ctrl+C stops it. Search by event ID or title and click nodes to inspect conditions, effects, and related nodes. Restart the command after editing local event JSON.

The viewer reads only events listed in the registry. It shows explicit story prerequisites; it does not simulate random delivery, delayed scheduling, world state, resource transactions, or game balance. Read item configuration directly as JSON; the viewer does not build a separate item graph.

The downloadable game cannot hot-load configuration from this repository. Editing these files does not change the installed game; integration requires validation and a new export from the private development project.

Share ideas, event IDs, or graph issues through Issues. Public readability does not grant an open-source or commercial license; see [RIGHTS.md](RIGHTS.md).
