# shanebrain-workflows

A personal fork of [warpdotdev/workflows](https://github.com/warpdotdev/workflows) — the public repository of [Warp](https://www.warp.dev) terminal workflows.

This fork exists so I (`thebardchat`) can:

- Add my own custom workflows (shanebrain-flavored shortcuts, scripts, and command recipes) on top of the upstream catalog.
- Pull in upstream updates from `warpdotdev/workflows` as they're released.
- Experiment with workflow tooling and AI-assisted authoring (see `CLAUDE.md`).
- Eventually contribute well-tested workflows back upstream via pull request.

> This is my **first** fork from another author's project, so I'm being deliberate about attribution and licensing. If you're the original author and notice anything that should be credited differently, please open an issue.

## What are Warp Workflows?

From the upstream README:

> Workflows make it easy to browse, search, execute and share commands (or a series of commands) — without needing to leave your terminal.

Warp users can browse them via the Command Palette (`Ctrl+Shift+R`) or at [commands.dev](https://commands.dev). Each workflow lives as a YAML file in `specs/`.

## Repository structure

This will mirror upstream after the fork is merged in:

```
specs/          # Workflow YAML definitions
src/            # Build / validation tooling (TypeScript + Rust)
CLAUDE.md       # Guidance for Claude Code working in this repo
README.md       # You are here
LICENSE         # See "Licensing & attribution" below
```

## Credits & attribution

All credit for the original project, tooling, and the existing workflow catalog goes to **Warp (warpdotdev)** and the wider community of contributors who have submitted workflows upstream.

- **Original project:** [warpdotdev/workflows](https://github.com/warpdotdev/workflows)
- **Original author / maintainer:** [Warp (warpdotdev)](https://github.com/warpdotdev) — the team behind the [Warp terminal](https://www.warp.dev)
- **Upstream contributors:** The full list of people who have authored or improved workflows is maintained by GitHub at [github.com/warpdotdev/workflows/graphs/contributors](https://github.com/warpdotdev/workflows/graphs/contributors). I am grateful to every one of them — this fork is built entirely on their work.
- **Web index:** [commands.dev](https://commands.dev), also by Warp.

Anything in `specs/` that originated upstream remains the work of its original author. New workflows added in this fork by `thebardchat` will be marked as such in their YAML `author` field.

## Licensing & attribution notice

The upstream `warpdotdev/workflows` repository is licensed under the **Apache License 2.0**. Because this project is a fork, that license and its `NOTICE`/attribution requirements continue to apply to all upstream-derived content.

## Status

🚧 **Pre-fork scaffolding.** Right now this repo only contains the README, CLAUDE.md, and a placeholder license. The actual workflow content from `warpdotdev/workflows` will be merged in next.
