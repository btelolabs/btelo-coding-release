<p align="center">
  <img src="logo_v2.png" width="120" alt="vibe-remote" />
</p>

<h1 align="center">vibe-remote</h1>

<p align="center">
  Native iPhone remote for AI coding on your machine.
  <br />
  Run Claude Code, Codex, Gemini CLI, or OpenCode on your Mac/Linux/Windows box — and control it from your phone with no VPN, no SSH gymnastics, and no desk required.
</p>

<p align="center">
  <a href="https://vibe-remote.com">Website</a>
  &nbsp;·&nbsp;
  <a href="https://vibe-remote.com/doc">Docs</a>
  &nbsp;·&nbsp;
  <a href="https://apps.apple.com/app/id6759615708">iOS App</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/ymzuiku/vibe-remote/releases">Downloads</a>
</p>

---

## What it is

`vibe-remote` lets you run AI coding sessions on your own machine and control them from your iPhone.

Instead of remote-desktopping into your laptop or fighting with SSH + tmux on a phone screen, you:

1. Run `vibe-remote` on your machine
2. Scan a QR code from the iPhone app
3. Prompt the AI from your phone
4. Let the work happen where your code, tools, and credentials already live

## Why it feels different

- **AI-native, not a tiny IDE** — direct the agent instead of editing files line-by-line on your phone
- **Your machine does the work** — builds, tests, git, and long-running sessions stay local
- **No model lock-in** — works with Claude Code, Codex, Gemini CLI, and OpenCode
- **Simple by default** — use the public relay for instant setup, or self-host your own relay

## Quick start

### 1) Install one supported provider

- **Claude Code:** `npm install -g @anthropic-ai/claude-code`
- **Codex:** `npm install -g @openai/codex`
- **OpenCode:** `go install github.com/opencode-ai/opencode@latest`
- **Gemini CLI:** install it normally and make sure it is available in your `PATH`

### 2) Install vibe-remote

**macOS / Linux**

```bash
curl -fsSL https://vibe-remote.com/install.sh | sh
```

**Windows (PowerShell)**

```powershell
irm https://vibe-remote.com/install.ps1 | iex
```

### 3) Start and pair

```bash
vibe-remote
```

Press `c` to set your **connector name** and **password**, then scan the QR code in the iPhone app.

If you are on Windows or a non-TUI environment, use:

```bash
vibe-remote --headless --connector myconnector --password mypassword
```

### 4) Send your first prompt

- `read the README and explain this repo`
- `run the test suite and tell me what failed`
- `start the dev server and give me the local preview URL`

## Security & pricing

- **End-to-end encrypted communication**
- **Zero-knowledge relay model**
- **Connector password stored locally and hashed with bcrypt**
- **Free forever tier:** 3 directories, 1 persistent session window per directory, 1 scheduled task
- **Free PRO trial** for new users

## Learn more

- [Getting started](https://vibe-remote.com/doc/getting-started)
- [Providers](https://vibe-remote.com/doc/providers)
- [Relay & self-hosting](https://vibe-remote.com/doc/relay)
- [Pricing](https://vibe-remote.com/pricing)

## Changelog

### v1.2.12 — 2026-04-14

Swipe to dismiss Dynamic Island banner.

### v1.2.11 — 2026-04-14

Blog integration from btelo.com with voice input improvements

### v1.2.10 — 2026-04-11

Auto-resume interrupted turns when a new message supersedes an in-progress task

[View all changelogs →](changelogs/)

## License

Proprietary. All rights reserved.
