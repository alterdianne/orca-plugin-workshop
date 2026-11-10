# Orca plugin workshop

An agent skill that helps college design students prepare to build and publish an Orca plugin with AI. Designed for students with little or no coding or terminal experience.

At the workshop, you'll use AI to build a small plugin for Orca, an app for working with coding agents such as Claude Code and Codex. Plugins add experiences inside Orca, such as a notes panel, an organization tool, or a visual theme. Preparation introduces the app, sets up your tools, and tests a starter example; you'll build your own plugin during the workshop.

## Start with your agent

Open Claude Code or Codex on your computer, in an environment with permission to work with local files and run setup commands. Paste this message:

> Get the skill from https://github.com/alterdianne/orca-plugin-workshop and use it to prepare my computer for the workshop.

You don't need to run terminal commands yourself or create a GitHub account before starting. Your agent will help you. A chat-only session without access to your computer can explain the steps but cannot complete local installation.

The skill helps you:

- Install Orca and the tools you need, then explore its projects, workspaces, and terminals.
- Create a GitHub account if needed and log in with GitHub CLI.
- Create your own plugin repository and local project folder.
- Verify your existing Figma MCP connection or set it up if missing, then test access to a reference frame. This is a required preparation step.
- Load and test a starter plugin in Orca.
- Save reopening instructions and brainstorm plugin ideas.

Try Orca before choosing what to build. Come to the workshop with an idea or a shortlist of plugins you'd like to make; you can refine your choice during the workshop. Ask your agent questions and explore ideas together.

Your agent reports computer setup, Figma access, and your plugin idea separately. A required setup or Figma check that remains unverified is unfinished preparation, with a next action to resolve it.

The workshop goal is a tested plugin published to the [Orca community directory](https://www.onorca.dev/plugins). Pre-work prepares your environment; it does not publish the starter.

## Optional command-line installation

If you already have Node.js 22.20 or newer and prefer to install the skill yourself:

```sh
npx skills add alterdianne/orca-plugin-workshop -g
```

Choose your agent when prompted, then ask it to use `setup-orca-workshop`.

## Files

- [Skill instructions](skills/setup-orca-workshop/SKILL.md)
- [Workshop publishing checklist](skills/setup-orca-workshop/references/publishing.md)

Community workshop resource; not affiliated with Orca or Stably.
