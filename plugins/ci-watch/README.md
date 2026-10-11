# CI Watch

After every git push, follows the GitHub Actions runs (via gh) until they finish; with an open pull request (also after gh pr create, or /ci pr <nr>) all its checks, other CI included, and whether it is ready to merge. On red it shows the failed step log.

Part of the [Mod Box](https://github.com/LupusMalusDeviant/mod-box), which bundles it with other mods and one window to switch and configure them all. This is the same mod on its own.

## Install

In a terminal Claude Code session (2.1.287 or newer):

```
/plugin install ci-watch --marketplace LupusMalusDeviant/claude-mods
```

## Commands

| Command | What it does |
|---|---|
| `/ci` | state of the watched runs |
| `/ci pr <nr\|url>` | watch a pull request |
| `/ci stop` | stop watching |

## Options

Set them in `/config` (or when installing).

| Option | Default | What it does |
|---|---|---|
| `intervalSec` | `20` | How often gh is asked for the state of the runs. |
| `onRed` | `both` | pane: open the log pane. prompt: put an analysis request into the prompt (not sent). both. |
| `sound` | `off` | on: a short sound when the runs are green or red (Windows: system sounds). |
| `language` | `en` | Language of the texts this mod shows and writes. |

## License

MIT, see [LICENSE](LICENSE).
