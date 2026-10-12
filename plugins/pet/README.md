# Desktop Pet

A little cardboard box on the Windows desktop, always on top, that says in a speech bubble what Claude is doing: the file it reads or changes, the command that runs, what a guard held, and a short summary at the end of a turn. Drag it anywhere, right-click for quiet time. Built once with the C# compiler that ships with Windows and signed with the Sign Guard script when one is set. /pet shows it, /pet stop sends it off.

Part of the [Mod Box](https://github.com/LupusMalusDeviant/mod-box), which bundles it with other mods and one window to switch and configure them all. This is the same mod on its own.

## Install

In a terminal Claude Code session (2.1.287 or newer):

```
/plugin install pet --marketplace LupusMalusDeviant/claude-mods
```

## Commands

| Command | What it does |
|---|---|
| `/pet` | show the desktop pet |
| `/pet stop` | send it off |

## Options

Set them in `/config` (or when installing).

| Option | Default | What it does |
|---|---|---|
| `bubble` | `9` | How long news stays in the bubble. Questions and errors stay until the next news. |
| `summary` | `off` | off: the first sentences of the answer (no tokens). haiku: Haiku puts a longer answer in one sentence. |
| `language` | `en` | Language of the texts this mod shows and writes. |
| `signScript` | `` | PowerShell script called as <script> -Exe <file>. Empty: ~/.claude/skills/sign-binary/sign.ps1 |

## License

MIT, see [LICENSE](LICENSE).
