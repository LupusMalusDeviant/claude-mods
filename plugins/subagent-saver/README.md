# Subagent Saver

Search subagents (Explore) that were given no model of their own run on a cheaper one instead of the main model. An explicit model, forks, teammates and plugin agents stay untouched.

Part of the [Mod Box](https://github.com/LupusMalusDeviant/mod-box), which bundles it with other mods and one window to switch and configure them all. This is the same mod on its own.

## Install

In a terminal Claude Code session (2.1.287 or newer):

```
/plugin install subagent-saver --marketplace LupusMalusDeviant/claude-mods
```

## Options

Set them in `/config` (or when installing).

| Option | Default | What it does |
|---|---|---|
| `model` | `sonnet` | Model for the listed subagent types. Sonnet searches nearly as well as Opus; Haiku is cheaper but may miss things, which then costs a second search on the main model. |
| `types` | `Explore` | Built-in subagent types to route, comma separated. |
| `language` | `en` | Language of the texts this mod shows and writes. |

## License

MIT, see [LICENSE](LICENSE).
