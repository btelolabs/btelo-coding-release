<p align="center">
  <img src="logo.png" width="120" alt="Vibe Remote">
</p>

<h1 align="center">Vibe Remote</h1>

<p align="center">
  Remotely control <a href="https://claude.ai/claude-code">Claude Code</a> to develop on your machine from anywhere.
  <br><br>
  <a href="https://vibe-remote.com">Official Website</a> &nbsp;·&nbsp; <a href="https://apps.apple.com/app/id6759615708">iOS App</a> &nbsp;·&nbsp; <a href="https://github.com/ymzuiku/vibe-remote/releases">Downloads</a>
</p>

---

Whether you're at home, in a cafe, or on your phone — Vibe Remote lets you manage and run AI coding sessions against directories on your local or remote machine.

## Prerequisites

Vibe Remote requires **at least one** AI coding agent CLI installed on your machine:

| Provider | Official Site | Status |
|----------|--------------|--------|
| Claude Code (recommended) | https://docs.anthropic.com/en/docs/claude-code | Stable |
| Codex | https://github.com/openai/codex | Stable |
| OpenCode | https://github.com/anomalyco/opencode | Experimental |

> **Tip:** You can install multiple providers. Vibe Remote auto-detects all available ones and lets you choose per session.

## Quick Start

**macOS / Linux:**

```bash
curl -fsSL https://vibe-remote.com/install.sh | sh
```

**Windows (PowerShell):**

```powershell
irm https://vibe-remote.com/install.ps1 | iex
```

Then start the agent:

```bash
vibe-remote
```

On first launch you'll set an account and password in the TUI. Then connect from the iOS app.

## Usage

```bash
# Start the agent
vibe-remote

# Show help
vibe-remote help

# Run headless (for scripts/CI)
vibe-remote --headless --account myname --password mypass
```

The default port is `24385`. If occupied, a random available port is used automatically.

## Why

You have a dev machine at home (or a cloud server). You want to use Claude Code to develop on it, but you're not always sitting in front of it. Vibe Remote bridges that gap:

- Start Vibe Remote on your dev machine
- Connect from your phone via the iOS app
- Point Claude Code at any directory and start coding
- Password protected — only you can access it

## Security

- Password is hashed with bcrypt and stored locally
- All communication is end-to-end encrypted
- Session tokens are cryptographically random

## License

Proprietary. All rights reserved.
