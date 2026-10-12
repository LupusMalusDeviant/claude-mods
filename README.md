# Claude Code mods

Single Claude Code mods, each installable on its own. They are the standalone versions of mods from the [Mod Box](https://github.com/LupusMalusDeviant/mod-box), which bundles them (and more) with one window to switch, configure and profile them. Take the box if you want several; take a mod from here if you want just that one.

Needs Claude Code 2.1.287 or newer. Install one in a terminal Claude Code session:

| Mod | What it does | Origin | Install |
|---|---|---|---|
| [Cache Meter](plugins/cache-meter) | Band: time left on the warm cache, hit rate, context as weather, plan limits, compact and keep-warm buttons; stops one send to a cold cache and names its cost (Cache Tax runs inside). | own, embeds a fork (see its README) | `/plugin install cache-meter --marketplace LupusMalusDeviant/claude-mods` |
| [Subagent Saver](plugins/subagent-saver) | Search subagents (Explore) that were given no model of their own run on a cheaper one instead of the main model. An explicit model, forks, teammates and plugin agents stay untouched. With Claude Code's own CLAUDE_CODE_SUBAGENT_MODEL set (for all subagents), the mod stays out. | own | `/plugin install subagent-saver --marketplace LupusMalusDeviant/claude-mods` |
| [Read Guard](plugins/read-guard) | Holds a whole-file Read (no offset/limit) of a file above the limit, a lockfile, minified code or a source map, and the same via cat, type or Get-Content in the shell; tells Claude the size, a token estimate and a better way (Grep, offset/limit). A second try at the same file goes through. Claude Code itself stops only at about 25,000 tokens. | own | `/plugin install read-guard --marketplace LupusMalusDeviant/claude-mods` |
| [Secret Guard](plugins/secret-guard) | Stops before Claude writes API keys, tokens, private keys or a non-ignored .env into files, git add or commits. Exceptions for test keys and example files: /secret-allow. | own | `/plugin install secret-guard --marketplace LupusMalusDeviant/claude-mods` |
| [Package Guard](plugins/package-guard) | Before Claude installs or runs a package (npm, pnpm, yarn, bun, npx, pip, uv, poetry, pipx, cargo), asks the public registry about it. Holds the command when the package does not exist (a made-up name), is under 14 days old, or looks like a well-known package and is young or thin (typosquatting). Allow in the band or with /pkg-allow. | own | `/plugin install package-guard --marketplace LupusMalusDeviant/claude-mods` |
| [CI Watch](plugins/ci-watch) | After every git push, follows the GitHub Actions runs (via gh) until they finish; with an open pull request (also after gh pr create, or /ci pr <nr>) all its checks, other CI included, and whether it is ready to merge. On red it shows the failed step log. | own | `/plugin install ci-watch --marketplace LupusMalusDeviant/claude-mods` |
| [Sign Guard](plugins/sign-guard) | Spots Windows builds (cargo --release, dotnet publish, go build, pyinstaller, tauri, electron-builder, msbuild) and signs the new .exe/.msi/.msix with your own signing script. | own | `/plugin install sign-guard --marketplace LupusMalusDeviant/claude-mods` |
| [Handoff Note](plugins/handoff) | /handoff writes a handoff note to .claude/handoff.local.md; a new session offers to continue from it. | own | `/plugin install handoff --marketplace LupusMalusDeviant/claude-mods` |
| [Desktop Pet](plugins/pet) | A little cardboard box on the Windows desktop, always on top, that says in a speech bubble what Claude is doing: the file it reads or changes, the command that runs, what a guard held, and a short summary at the end of a turn. Drag it anywhere, right-click for quiet time. Built once with the C# compiler that ships with Windows and signed with the Sign Guard script when one is set. /pet shows it, /pet stop sends it off. | own | `/plugin install pet --marketplace LupusMalusDeviant/claude-mods` |
| [Blast Radius](plugins/blast-radius) | Holds risky shell commands (rm -rf, git reset --hard, git clean, force push, migrations) and shows what they would hit. | fork of [anthropics/claude-code-playground](https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/blast-radius) | `/plugin install blast-radius --marketplace LupusMalusDeviant/claude-mods` |

Forks say where they come from, in their README and at the top of every changed file. Everything here is generated from the Mod Box (`node tools/box.mjs export --out <this repo>`); please send changes there.

## License

Each plugin has its own LICENSE: MIT for the own mods, the original license for forks (Apache-2.0 for Blast Radius; the Cache Tax part of Cache Meter is MIT by Karan Bansal).
