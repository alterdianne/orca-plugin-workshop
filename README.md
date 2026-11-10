# Orca plugin workshop

An agent skill that helps college design students prepare to build and publish an Orca plugin with AI. Designed for students with little or no coding or terminal experience.

## Install

Install [Node.js](https://nodejs.org/) 22.20 or newer if `npx` is not available, and have Claude Code or Codex ready to use on your computer.

Run in your terminal:

```sh
npx skills add alterdianne/orca-plugin-workshop -g
```

Choose Claude Code or Codex when prompted. The `-g` option makes the skill available across projects.

## Start

Open your chosen agent and ask:

> Use the setup-orca-workshop skill to prepare my computer for the Orca plugin workshop.

The skill helps you:

- Install Orca and the tools you need.
- Create a GitHub account if needed and log in with GitHub CLI.
- Create your own plugin repository and local project folder.
- Connect Figma MCP if you plan to use Figma.
- Load and test a starter plugin in Orca.
- Save reopening instructions and brainstorm plugin ideas.

The workshop goal is a tested plugin published to the [Orca community directory](https://www.onorca.dev/plugins). Pre-work prepares your environment; it does not publish the starter.

## Files

- [Skill instructions](skills/setup-orca-workshop/SKILL.md)
- [Workshop publishing checklist](skills/setup-orca-workshop/references/publishing.md)

Community workshop resource; not affiliated with Orca or Stably.
