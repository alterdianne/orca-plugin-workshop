# Orca plugin workshop

An agent skill that helps college design students prepare to build and publish an Orca plugin with AI. Designed for students with little or no coding or terminal experience.

At the workshop, you'll use AI to build a small plugin for Orca, an app for working with coding agents such as Claude Code and Codex. Plugins add experiences inside Orca, such as a notes panel, an organization tool, or a visual theme. Preparation focuses on getting your computer ready so you can be productive immediately at the workshop; you'll build your own plugin there.

## Start with your agent

Open Claude Code or Codex on your computer, in an environment with permission to work with local files and run setup commands. Paste this message:

> Read and follow https://raw.githubusercontent.com/alterdianne/orca-plugin-workshop/main/skills/setup-orca-workshop/SKILL.md to prepare my computer for the workshop. Use your terminal tools to run the setup commands.

You can also attach the downloaded `SKILL.md` file and ask your agent to follow it. No npm, npx, or skill installation command is needed to begin.

You don't need to run terminal commands yourself or create a GitHub account before starting. Your agent will help you. A chat-only session without access to your computer can explain the steps but cannot complete local installation.

If you don't understand something or something unexpected happens, send your agent a screenshot and ask it to guide you through the next step.

The skill helps you:

- Install Orca and the tools you need, and verify that they start successfully.
- Create a GitHub account if needed and log in with GitHub CLI.
- Create your own plugin repository and local project folder.
- Verify your existing Figma MCP connection or set it up if missing, then test access to a reference frame. This is a required preparation step.
- Load and test a starter plugin in Orca.
- Save reopening instructions and report which setup checks passed or remain unfinished.

After all required setup is complete, your agent can optionally guide you through Orca and help brainstorm plugin ideas. You can stop after setup or choose an idea during the workshop; exploration and brainstorming are extra help, not requirements for computer readiness.

Your agent reports computer setup and Figma access, plus your plugin idea if discussed. A required setup or Figma check that remains unverified is unfinished preparation, with a next action to resolve it.

The workshop goal is a tested plugin published to the [Orca community directory](https://www.onorca.dev/plugins). Pre-work prepares your environment; it does not publish the starter.

## Files

- [Skill instructions](skills/setup-orca-workshop/SKILL.md)
- [Workshop publishing checklist](skills/setup-orca-workshop/references/publishing.md)

Community workshop resource; not affiliated with Orca or Stably.
