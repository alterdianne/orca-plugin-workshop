---
name: setup-orca-workshop
description: Prepare college design students for an Orca plugin workshop with product orientation, local setup, GitHub, verified Figma MCP, a working starter, and help choosing a plugin idea.
---

# Prepare for the Orca plugin workshop

Help a college design student arrive with a working plugin starter, verified Figma access, and an idea or shortlist to explore. During the workshop, they will design, test, and publish their plugin to Orca's community directory.

Assume little technical experience. Do the technical work directly when possible. Explain progress simply, and give one instruction at a time when the student must act. Let them handle passwords and authorization. Reuse existing setup and preserve their work. Pre-work ends before building or publishing the finished plugin.

## 1. Explain the workshop and check their setup

Before setup commands or idea questions, explain what the participant will use and build. Assume they may never have used Orca. For example:

> At the hackathon, you'll use AI to build a small plugin for Orca, an app for working with coding agents such as Claude Code and Codex. A plugin adds something inside Orca, such as a notes panel, an organization tool, or a visual theme. Today we'll prepare your computer and test a starter example. You'll build your own plugin during the hackathon, then publish it to Orca's community directory. You can explore Orca before deciding what to make.

Distinguish the workshop skill (instructions for the agent), the starter plugin (an example to test setup), and the participant's plugin (what they will build). An undecided plugin idea is a creative preparation task; never describe it as missing software or a missing plugin.

Detect their OS and whether they use Claude or Codex; follow an explicit preference. Say, “You're using <agent>. I'll help you get ready to build your own Orca plugin.” Ask only if unclear.

Check local file and terminal access, existing projects, installed tools, and authentication. If this is a chat-only environment, help them continue in a local agent.

## 2. Install Orca and tools

Install or verify the [Orca desktop app](https://www.onorca.dev/download) and its `orca` CLI. Use the instructor's version if specified. Install or configure the chosen coding agent if missing, guide sign-in, and verify access where the student will use it. Don't start a paid task just to test access.

Read the current [plugin authoring guide](https://github.com/stablyai/orca/blob/main/docs/reference/plugin-authoring.md) and CLI help. Install Git, GitHub CLI (`gh`), and any tools the plugin starter requires. Use the released app; no Orca source checkout or browser development server is needed.

Once Orca opens, give a short walkthrough of projects, workspaces, terminals or agent chats, and where plugins appear. Use what is visible in the installed version. Let the participant explore before asking them to invent a feature for an unfamiliar product.

## 3. Set up GitHub

If they need an account, open https://github.com/signup and guide signup and email verification. Otherwise reuse their account.

Run `gh auth status`. If needed, guide browser login with `gh auth login --hostname github.com --web --git-protocol https`. Verify the intended account, run `gh auth setup-git`, and check the agent's repository access. Keep working authentication; add another integration only if required.

## 4. Create a plugin project

Use their preferred folder or `~/Projects/ai-design-workshop/my-plugin` (under their home folder on Windows too). Create it and explain where it lives.

Use `gh` to create an original student-owned repository. Community listing requires a public repository and excludes forks. Explain visibility before creating it; don't change an existing repository's visibility silently. Clone it locally or connect their existing project. Verify `origin` and write permission without a test push. Configure missing Git author details locally with their chosen name and email; offer their GitHub private email.

Scaffold a minimal starter with `orca plugin create`, using the installed CLI's supported syntax. Keep `orca-plugin.json` at the repository root and preserve `.git` and existing files. Generate elsewhere and copy the starter if an empty folder is required.

Use the instructor's starter or a simple panel, and install its dependencies. This is only a setup check. Don't ask the student to choose HTML, components, or a theme yet; recommend an approach after they choose their plugin idea.

## 5. Verify Figma MCP or set it up

Figma MCP verification is a required preparation step for this workshop. Check the selected coding agent's existing configuration before installing or adding a connection:

- **Already configured:** reuse it and verify the intended Figma account. When several accounts are available and the intended one is unclear, ask which to use.
- **Missing:** follow the current official Figma instructions for the selected agent, configure MCP directly where possible, and guide the participant through signup/sign-in and authorization as needed.
- **In either case:** ask for a reference frame they can access and verify that the selected agent can read it. A browser sign-in, installed plugin, or configured MCP server alone does not verify file access.

Mark this step complete only after a successful frame read. If no frame is available, report the connection as configured but file access unverified, and keep this required step incomplete. Explain that MCP gives the agent design context; the agent writes the plugin code. Save a handoff before any required session restart and resume afterward.

If verification fails, explain the specific error and guide one corrective step, then recheck once. If the same error remains, stop authentication attempts, record the blocker and next action, and continue independent setup work. Do not keep invoking checks that trigger sign-in prompts. Resume verification when the participant completes the corrective step and asks for a recheck; do not reinstall or replace a working connection to another account.

## 6. Test the starter

Open the project as a workspace in Orca. Follow the authoring guide to enable plugins and load the development folder, normally with `orca plugin dev watch .`. Explain requested permissions and let the student approve them. Keep the watcher in an accessible persistent session; explain which terminal must stay open and that stopping the watcher may unload the plugin.

Run `orca plugin validate .`. Open the starter and test one interaction, or apply the theme. Make a harmless edit and verify it reloads. Inspect with available tools or obtain specific student confirmation; record which. Passing validation alone isn't enough.

Point out the starter's panel or theme inside Orca so the participant connects the word "plugin" with an experience they have tried. Explain that the starter proves setup works; they do not need to build their final idea during preparation.

Use logs to fix setup problems. If the same error persists after a targeted fix and recheck, report the blocker and next action. Don't rewrite Orca or claim readiness while setup is blocked.

## 7. Save reopening instructions

Save `WORKSHOP-SETUP.md` outside the plugin repo with the project path, repo URL, branch, Orca version, authentication/Figma status, test results, and exact reopening and watcher commands. Keep credentials out.

Include the authoring-guide link and a copy of the [publishing checklist](references/publishing.md) so students can use it later without this skill. Explain that publishing happens at the end of the workshop; don't release a starter or add the discovery topic during pre-work. Use that checklist when publication is requested.

In the handoff and final chat, report these statuses separately:

- **Computer setup:** ready only when the required local tools, GitHub/project setup, and live starter checks pass; otherwise list the unfinished step and next action.
- **Figma access:** verified only after the frame-read check; otherwise say what is configured and what remains unverified or blocked.
- **Plugin idea:** chosen, exploring a shortlist, or undecided, with the next creative step.

Do not say all preparation is complete while a required setup or Figma check is unfinished. An undecided idea does not invalidate successful technical checks; report it separately so the participant knows whether they need software setup or time to explore.

## Last step: your plugin idea

Present this as a separate closing section in the student's chat, with the heading **Last step: your plugin idea**. Don't bury it in the setup report. Lead with:

> **Come to the workshop with an idea or a short list of plugins you'd like to build.**
> It doesn't need to be fully worked out. You can try Orca first and refine your choice during the workshop. Ask me questions and let me give you ideas.

Explain the possibilities and limits in terms of what they can build: panels and editors add experiences inside Orca; themes change appearance. Plugins use supported APIs and permissions. Check the authoring guide's UI and API references for the proposed idea.

Proactively offer ideas inspired by popular plugins in the current [community directory](https://www.onorca.dev/plugins). Link to relevant examples and explain the needs they serve. Use install counts as an adoption signal, not a quality guarantee; don't invent rankings if data is unavailable.

After the walkthrough and starter test, ask, "After trying Orca, is there something you wish it helped you do?" Ask about their interests and frustrations, then suggest a few original, achievable ideas. Notes could inspire a decision journal; a toolbox could inspire one design utility. Explain each idea's benefit, main interaction, and any API or service requirements. Verify feasibility before promising AI or automation.

Help them choose one user, one problem, and one small workflow. Once they choose an idea, recommend the simplest suitable approach and explain why:

- **Components:** TypeScript/TSX with Orca's plugin controls, for an interface that fits the app. These are separate from its internal React/shadcn components.
- **HTML panel:** HTML, CSS, and JavaScript for more custom visual design within the plugin frame and resource restrictions.
- **Theme:** configuration when the idea is about colors and visual identity.

Don't make the student choose technical architecture unaided. Record the idea, recommended approach, and first sketch task in the handoff. If undecided, save a shortlist and open questions to bring to the workshop; defer the technical recommendation until they choose. Stop before implementing the final plugin.
