# Agent Prompt & Skill Library

Installable [Agent Skills](https://agentskills.io) for HueForge image prompts and related image edits. Each skill lives in `skills/<name>/SKILL.md`. The open [`skills` CLI](https://github.com/vercel-labs/skills) (`npx skills`) discovers that layout and installs the skill into a coding agent.

## Skills

| Skill | Description |
| --- | --- |
| [`bambooify`](skills/bambooify/SKILL.md) | Transform a supplied image's subject into a structurally woven bamboo object while preserving its recognizable shape and colors. |
| [`hueforge-anime-portrait-series`](skills/hueforge-anime-portrait-series/SKILL.md) | Create a cohesive 3×3 grayscale anime character portrait grid optimized for HueForge printing. |
| [`hueforge-clean-flat-color-cel-shading`](skills/hueforge-clean-flat-color-cel-shading/SKILL.md) | Cleans up noise and gradients into flat, hard-edged color regions while preserving character identity and composition, for HueForge and color-limited 3D printing. |

Each HueForge skill keeps its English prompt in `SKILL.md` and its Chinese prompt in `Prompt-zh` ([portrait series](skills/hueforge-anime-portrait-series/Prompt-zh), [cel-shading](skills/hueforge-clean-flat-color-cel-shading/Prompt-zh)). The portrait series keeps its example images in [`examples/`](skills/hueforge-anime-portrait-series/examples). Bambooify keeps its edit templates and reference notes beside `SKILL.md`.

These folders replace the earlier `bambooify/`, `HueForge Anime Portrait Series/`, and `HueForge Clean Flat-Color Cel-Shading/` directories.

## Install

Requires Node.js 22.20 or later. The commands below use this repository on GitHub. From a local clone, use the repo path instead, for example `npx skills add . --list`.

List the skills in this repository without installing them:

```bash
npx skills add TnTvT/Agent-Prompt-Skill-Library --list
```

Install every skill to every agent, without confirmation prompts:

```bash
npx skills add TnTvT/Agent-Prompt-Skill-Library --all
```

Install one skill:

```bash
npx skills add TnTvT/Agent-Prompt-Skill-Library --skill hueforge-clean-flat-color-cel-shading
```

Target specific agents with `-a` or `--agent`. Documented agent ids include `cursor`, `claude-code`, and `codex`. The full list is in the CLI's [supported agents](https://github.com/vercel-labs/skills/blob/main/docs/agents.md) document.

```bash
npx skills add TnTvT/Agent-Prompt-Skill-Library --skill hueforge-anime-portrait-series -a cursor -a claude-code
```

Install every skill to one agent:

```bash
npx skills add TnTvT/Agent-Prompt-Skill-Library --skill '*' -a cursor
```

Install one skill to every agent:

```bash
npx skills add TnTvT/Agent-Prompt-Skill-Library --agent '*' --skill bambooify
```

`-g` installs into the user directory instead of the current project. `-y` skips confirmation prompts.
