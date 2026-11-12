---
name: setup-orca-workshop
description: "Prepare college design students for the Orca plugin workshop: explain what they will do, complete local setup, GitHub, and Figma MCP verification, then test a starter. Offer Orca exploration and plugin brainstorming afterward."
---

# Prepare for the Orca plugin workshop

Get the student's computer ready so they can be productive immediately at the workshop. Complete required setup before offering the optional Orca walkthrough and plugin brainstorming. Stop before building or publishing the finished plugin.

Assume little technical experience. Do setup work directly, reuse existing tools, and preserve the student's work. Explain progress simply; give one instruction at a time when they must act, and let them handle passwords and authorization.

## 1. Explain the workshop and check their setup

Start with brief context about the workshop. For example:

> At the hackathon, you'll use AI to build and publish a plugin for [Orca](https://www.onorca.dev/docs), an app for working with coding agents such as Claude Code and Codex. Plugins add features inside Orca, such as a notes panel, an organization tool, or a visual theme. Today we'll prepare your computer and test a starter so you can start working immediately at the workshop. At the end of this setup process, I will offer to help you explore Orca and brainstorm ideas for the plugin.

> If you don't understand something or something unexpected happens, send me a screenshot and I'll guide you through it.

Detect their OS and chosen agent (Claude or Codex), then check local file/terminal access, existing projects, tools, and authentication. Ask only if the agent choice is unclear. If this is a chat-only environment, help them continue in a local agent.

Verify terminal access and run setup commands directly. If blocked, explain what the student needs to do, then resume setup.

## 2. Install Orca and tools

Install or verify the released [Orca desktop app](https://www.onorca.dev/download) and its `orca` CLI, using the instructor's version if specified. Launch Orca to verify it starts. Install/configure the chosen coding agent if missing, guide sign-in, and verify access in the environment the student will use. Don't start a paid task just to test access.

Read the current [plugin authoring guide](https://github.com/stablyai/orca/blob/main/docs/reference/plugin-authoring.md) and CLI help. Install Git, GitHub CLI (`gh`), and tools required by the starter. No Orca source checkout or browser development server is needed.

## 3. Set up GitHub

Reuse their account, or guide signup and email verification at https://github.com/signup.

Run `gh auth status`. If needed, guide login with `gh auth login --hostname github.com --web --git-protocol https`. Verify the intended account, run `gh auth setup-git`, and check the agent's repository access. Keep working authentication; add an integration only if required.

## 4. Create a plugin project

Use their preferred folder or `~/Projects/ai-design-workshop/my-plugin` (under their home folder on Windows too), and explain where it lives.

Create or reuse an original student-owned repository with `gh`. Community listing requires a public repository and excludes forks. Explain visibility before creating it; don't silently change an existing repository's visibility. Clone it or connect the existing project. Verify `origin` and write permission without a test push. Configure missing Git author details locally with their chosen name and email; offer their GitHub private email.

Use the instructor's starter or scaffold a simple panel with `orca plugin create`, following the installed CLI's syntax. Keep `orca-plugin.json` at the repository root and preserve `.git` and existing files; scaffold elsewhere and copy if an empty folder is required. Install its dependencies. Defer architecture choices until the student chooses a plugin idea.

## 5. Verify Figma MCP or set it up

This step is required. Check Figma MCP in the selected coding agent:

- **Configured:** reuse the connection and verify the intended account; ask which account if unclear.
- **Missing:** configure it using current official Figma instructions for that agent, guiding signup/sign-in and authorization as needed.
- **In either case:** verify the agent can read a reference frame the student supplies. Browser sign-in or configuration alone does not prove file access.

Complete this step only after a successful frame read. Without a frame, record file access as unverified and setup as incomplete. Explain that MCP provides design context and the agent writes the code. Save a handoff before any required session restart and resume afterward.

If verification fails, explain the error, guide one corrective step, and recheck once. If it still fails, stop sign-in attempts, record the blocker and next action, and continue independent setup. Resume verification after the student completes that action and asks for a recheck. Preserve working connections to other accounts.

## 5b. Verify Paper MCP or set it up (optional)

Offer this after Figma MCP passes, for students who design in [Paper](https://paper.design). Skip it if they don't use Paper; it does not affect readiness.

Paper's MCP is served by the Paper desktop app on the student's computer, so Paper must be installed and open with a file. Check Paper MCP in the selected coding agent:

- **Configured:** reuse the connection.
- **Missing:** configure it using current official Paper instructions for that agent, guiding Paper install and sign-in as needed.
- **In either case:** verify the agent can read the open Paper file, such as listing its artboards or reading a selected frame. Configuration alone does not prove access.

If verification fails, explain the error, guide one corrective step, and recheck once. If it still fails, record the blocker and next action and continue. Preserve the Figma connection.

## 6. Test the starter

Open the project as an Orca workspace. Follow the authoring guide to enable plugins and load the development folder, normally with `orca plugin dev watch .`. Explain requested permissions and let the student approve them. Keep the watcher in an accessible persistent terminal; explain that it must stay open and stopping it may unload the plugin.

Run `orca plugin validate .`, guide one live interaction (or apply the theme), and verify a harmless edit reloads. Inspect with available tools or obtain specific student confirmation; record which. Validation alone is insufficient.

Use logs to fix problems. If an error persists after a targeted fix and recheck, report the blocker and next action; don't claim readiness.

## 7. Save reopening instructions

Save `WORKSHOP-SETUP.md` outside the plugin repo with the project path, repo URL, branch, Orca version, authentication/Figma status, Paper status if checked, test results, and exact reopening and watcher commands. Keep credentials out.

Include the authoring-guide link and a copy of the [publishing checklist](references/publishing.md) for use when publishing the finished plugin at the end of the workshop. Don't release the starter or add the discovery topic during setup.

## Optional closing activity: explore Orca and brainstorm

After all required setup checks pass and reopening instructions are saved, offer a walkthrough of Orca and help brainstorming. The student can stop here or choose an idea during the workshop; neither activity affects technical readiness.

If they continue, show how they can use Orca, then ask what they wish it helped them do. Explain that panels and editors add experiences inside Orca, while themes change its appearance.

Use examples from the current [community directory](https://www.onorca.dev/plugins) to suggest a few achievable ideas based on their interests or frustrations. Explain each idea's benefit, main interaction, and API or service requirements. Check the authoring guide's UI/API references before promising feasibility, including AI or automation.

Narrow the idea to one user, one problem, and one workflow. Recommend the simplest suitable approach: Orca components for an app-like interface, an HTML panel for custom visuals, or theme configuration for appearance. Record the idea, approach, and first sketch task in the handoff. If undecided, save a shortlist and open questions; defer architecture until they choose.
