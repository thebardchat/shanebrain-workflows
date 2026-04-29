# CLAUDE.md

Guidance for Claude Code (and Claude Code on the web) when working in this repository.

## What this repo is

`thebardchat/shanebrain-workflows` is a personal fork of [`warpdotdev/workflows`](https://github.com/warpdotdev/workflows), the public catalog of [Warp terminal](https://www.warp.dev) workflows.

A "workflow" here is a YAML file in `specs/` that describes a parameterized shell command (or a series of commands) that Warp users can browse, search, and execute from the Command Palette. Each spec includes a name, command template, description, tags, and argument definitions with defaults.

Treat this repo as **a curated content repo**, not an application. Most edits will be:

1. Adding a new YAML workflow under `specs/`.
2. Tweaking an existing workflow's command, args, or tags.
3. Occasionally touching the validation tooling under `src/` (TypeScript) or the Rust validator.

## What this fork is for

Beyond mirroring upstream, this fork is used to:

- Develop **shanebrain-specific workflows** — personal shortcuts, dev environment recipes, and AI/Claude-related command snippets.
- Stage workflows before deciding whether to upstream them via PR to `warpdotdev/workflows`.
- Experiment with AI-assisted workflow authoring (Claude generating, refining, and validating YAML specs).

## Working conventions

When asked to add or modify a workflow:

- Place new specs under `specs/<category>/<name>.yaml`, matching the upstream convention. If unsure of the category, search existing specs for similar commands first.
- Always include: `name`, `command`, `description`, `tags`, and `arguments` (with `description` and sensible `default_value` where applicable).
- Set `author: thebardchat` and `author_url: https://github.com/thebardchat` on any **new** workflow originally written here. Do **not** change the author on workflows pulled in from upstream.
- Keep upstream-authored files untouched unless the user explicitly asks for an edit — preserving original attribution matters.
- After changes, run the upstream validator (typically `cargo run` or `npm run build` / `npm test` per the upstream tooling) before reporting done.

## Attribution rules (important)

This is a fork of someone else's open-source work. Be careful to preserve credit:

- Never remove or rewrite upstream `LICENSE` or `NOTICE` files.
- Never change the `author` field on a workflow that came from upstream.
- When the user adds a workflow that's clearly inspired by an upstream one, note the inspiration in the workflow's `description` or as a comment.
- The upstream is **Apache-2.0**. New content added in this fork should also be Apache-2.0 unless the user explicitly says otherwise.

## Branching

The user develops on feature branches like `claude/<topic>-<slug>`. Don't push to `main` directly. When in doubt, ask which branch to use.

## Contributor info (for upstream PRs)

When opening a pull request upstream to `warpdotdev/workflows`, fill in their PR template using:

- **Discord username:** `ShaneBrainLegacy` (Shane's primary Discord handle; he has two others but this is the canonical one for upstream credit)
- **Description of changes:** auto-generate from the actual diff — list new spec paths, then existing-spec edits, then any tooling/doc changes, in that order. One bullet per file.

Don't ask the user to re-confirm the Discord handle every time; just include it. If he ever wants it changed or omitted, he'll say so.

## Tone for the user

The user is new to forking other people's projects and cares about giving proper credit. When you propose changes, briefly call out anything that might affect attribution, license compatibility, or upstream-merge friendliness, so they can decide before you act.

## Out of scope

- Don't refactor upstream tooling for stylistic reasons.
- Don't auto-rewrite existing specs in bulk.
- Don't generate workflows for destructive shell commands (`rm -rf /`, force-pushes to shared branches, etc.) without an explicit, clearly-scoped request.
