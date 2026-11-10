---
name: setup-orca-workshop
description: Prepare college design students to build and publish an Orca plugin with AI, including local tools, GitHub, optional Figma MCP, a working starter, and idea exploration.
---

# Prepare for the Orca plugin workshop

Help a college design student arrive ready to build their own plugin, with a working starter and an idea of what they want to make. The workshop outcome is a tested plugin published to Orca's community directory. Pre-work prepares their setup and idea, not a finished or published plugin.

Assume little experience with coding, terminals, Git, or development tools. Perform supported technical steps directly. Explain progress briefly in plain language; give one instruction at a time when the student must act. Let them enter credentials and complete authorization themselves. Skip completed setup and preserve existing work.

## 1. Identify the environment

Detect the OS and whether the host agent is Claude or Codex; respect an explicit choice. Say, “You're using <agent>. I'll help you get ready to build your own Orca plugin.” Ask only if detection is unclear. Verify local filesystem and terminal access; otherwise help the student move to a local agent.

Inspect existing project folders, installations, authentication, and Git remotes before creating anything. Reuse compatible setup. Use OS-appropriate paths and commands.

## 2. Install Orca and the tools

Install or verify the released desktop app from https://www.onorca.dev/download, using an instructor-specified version if supplied. Verify its `orca` CLI is available and supports plugin development. Install or configure the chosen coding agent where the student will use it, and verify authentication without starting an unnecessary paid task.

Read the current [plugin authoring guide](https://github.com/stablyai/orca/blob/main/docs/reference/plugin-authoring.md) and CLI help. Install Git, GitHub CLI (`gh`), and only the additional tools required by the chosen plugin starter. This workflow uses the installed app; it does not require cloning or building Orca itself or starting its web frontend.

## 3. Set up GitHub

Check for a GitHub account. If needed, open https://github.com/signup and guide account creation and email verification step by step. Verify sign-in.

Check `gh auth status`. If needed, run `gh auth login --hostname github.com --web --git-protocol https` and guide browser authorization. Verify the intended account and run `gh auth setup-git`. Don't unnecessarily log out of existing accounts. Verify the agent can access GitHub through these tools; configure another integration only if needed.

## 4. Create the student's plugin project

Use their preferred location or `~/Projects/ai-design-workshop/my-plugin`, under their home folder on Windows too. Create the parent folder and explain where the project lives. Reuse an existing plugin project without overwriting it.

Create an original student-owned repository, not a fork of Orca or a plugin example: forks are excluded from the community directory. Explain that publication requires a public repository. Guide repository creation with `gh`; never change an existing private repo's visibility silently. Clone the new repo locally, or connect an existing local project to it. Verify `origin` and the student's write permission without a test push. Configure missing Git author name/email locally using their chosen identity; offer their GitHub private email. Preserve any existing branch with work on it.

Scaffold a minimal plugin with `orca plugin create`, following the installed CLI's supported syntax. Keep `orca-plugin.json` at the repository root. Use a temporary scaffold folder if the generator requires an empty destination; preserve `.git`. Pick a starter with the student:

- **Components:** TypeScript/TSX using Orca's own controls; good for matching the app.
- **HTML panel:** HTML/CSS/JavaScript for more visual freedom.
- **Theme:** configuration for a visual-identity exercise.

Use an instructor starter when provided; otherwise show the options briefly and use a simple panel. The starter proves setup and can change after brainstorming. Install only its required dependencies. Don't build the student's final idea yet.

## 5. Connect Figma MCP when needed

Ask whether they plan to design in Figma unless the workshop brief already answers. If yes, help create or sign into a Figma account and configure the chosen agent's supported Figma MCP connection using current official instructions. Perform configuration directly where possible; guide settings and authorization one step at a time otherwise.

Verify the agent can read a student-provided or workshop reference frame. If no file is available yet, distinguish a configured connection from verified file access. If a restart is required, save a handoff first and resume verification afterward. Explain that the agent translates Figma into plugin code; MCP isn't an automatic import. Skip Figma when declined.

## 6. Verify the starter in Orca

Open the plugin project as a workspace in the installed app. Follow the authoring guide to enable plugins and load the development folder, normally with `orca plugin dev watch .`. Explain requested access and let the student approve it. Keep the watcher available with accessible logs.

Run `orca plugin validate .`, open the starter inside Orca, test one interaction (or apply a theme and verify its appearance), and verify an innocuous saved edit reloads. Inspect through available tools or obtain specific student confirmation; label the evidence honestly. A running watcher or passing validator alone does not prove the interface works.

Resolve setup failures from logs. After a targeted fix and recheck fails identically, report the blocker and next action rather than looping or rewriting Orca. Don't claim readiness while required steps remain blocked.

## 7. Save the workshop handoff

Save brief `WORKSHOP-SETUP.md` notes outside the plugin repository: project path, repo URL, branch, app version, authentication and Figma status, verification results, and exact steps to reopen the project and restart development. Keep credentials out. Link to the plugin authoring guide and the [publishing checklist](references/publishing.md), copying the latter's relevant instructions into the handoff so it works without this installed skill.

Explain the workshop finish line: test, document, validate, then publish a version for others to install. Don't push a release tag or add the discovery topic during pre-work. When the student requests publication later, follow [references/publishing.md](references/publishing.md).

## 8. Think about plugins you could build

Explain the canvas: a panel or editor can add an experience inside Orca; a theme changes appearance. Plugins use supported APIs and permissions, not unrestricted access to the whole app. Components follow Orca's plugin component catalog; custom HTML has more styling freedom within its frame and resource restrictions. Read the linked plugin UI and API references for the chosen approach rather than assuming the app's internal React/shadcn components are plugin imports.

Tell the student: “Come to the workshop with an idea for a plugin you'd like to build. It doesn't need to be fully worked out. You can ask me questions and brainstorm with me to help you decide.”

Start offering ideas proactively. Check the current [Orca plugin directory](https://www.onorca.dev/plugins), especially its most-installed plugins and popular categories. Link to a few relevant examples and explain the user needs they serve. Treat installs as evidence of adoption, not proof of quality or a guarantee that a similar idea will succeed. If live popularity data is unavailable, say so rather than inventing rankings.

Ask about the student's interests or recurring frustrations, then suggest a few achievable directions inspired by those examples. Translate successful patterns into an original small idea rather than copying an existing plugin: notes might inspire a design decision journal; a toolbox might inspire one useful design utility; a theme might inspire an original visual identity. For each suggestion, explain the user benefit, one core interaction, and any API or external-service dependencies. Check feasibility before promising automation or AI features.

Help them choose a preferred idea around one user, one problem, and one achievable workflow. Record it and a first sketch task in the handoff. If they remain undecided, save a shortlist and the questions to resolve, and remind them to pick an idea before the workshop. Don't start building the final plugin during pre-work.
