# Orca plugin workshop

An agent skill that helps college design students prepare to build and publish an Orca plugin with AI. Designed for students with little or no coding or terminal experience.

## Start with your agent

Open Claude Code or Codex on your computer, in an environment with permission to work with local files and run setup commands. Paste this message:

> Help me prepare for the Orca plugin workshop. Get the setup-orca-workshop skill from https://github.com/alterdianne/orca-plugin-workshop. Read skills/setup-orca-workshop/SKILL.md and follow it, fetching its referenced files when needed. Perform the technical setup for me and guide me one step at a time when I need to sign in or approve something. I am a design student with limited technical experience.

You don't need to run terminal commands yourself or create a GitHub account before starting. Your agent will help you. A chat-only session without access to your computer can explain the steps but cannot complete local installation.

The skill helps you:

- Install Orca and the tools you need.
- Create a GitHub account if needed and log in with GitHub CLI.
- Create your own plugin repository and local project folder.
- Connect Figma MCP if you plan to use Figma.
- Load and test a starter plugin in Orca.
- Save reopening instructions and brainstorm plugin ideas.

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
