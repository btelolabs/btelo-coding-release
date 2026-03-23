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

## What is vibe-remote?

`vibe-remote` lets you control AI coding sessions running on your own machine from your iPhone.

Instead of remote-desktopping into your laptop or fighting with SSH + tmux + Tailscale on a phone screen, you:

1. Run `vibe-remote` on your machine
2. Scan a QR code from the iPhone app
3. Chat with the AI on your phone
4. Let the AI do the work on your machine in real time

It is built for an **AI-native workflow**:

- **Your machine does the work** — builds, edits, tests, git operations, and long-running sessions happen where your code already lives
- **Your phone is the control surface** — review output, send prompts, monitor progress, and keep moving when you are away from your desk
- **The AI is the executor** — you describe intent; the agent handles the mechanics

## Why this exists

If you already use Claude Code or similar tools, you probably have one of these problems:

- You want to keep coding when you're away from your desk
- You have a dev machine at home, in the office, or on a cloud server
- You can technically remote in today, but the setup feels like a workaround, not a product
- You want something that feels native on iPhone, not like forcing a desktop workflow onto a small screen

`vibe-remote` exists to make that experience feel simple:

- **No VPN required**
- **No port forwarding**
- **No terminal UI wrestling on mobile**
- **No model lock-in**

## Why it feels different

### AI-native by design

`vibe-remote` is intentionally not an editor.

You don't open files and type code line-by-line on your phone. You tell the AI what you want, and the AI executes on your machine. That makes the product feel more like a remote control for your coding agent than a tiny IDE.

### Works with the best coding agents

Install the provider you already like and `vibe-remote` auto-detects it:

- **Claude Code** (recommended)
- **Codex**
- **Gemini CLI**
- **OpenCode**

### Your workflow, not ours

Use the official public relay for instant setup, or self-host your own relay if you want full control.

## Quick start

### 1) Install an AI coding provider

You need at least one provider installed on the machine running `vibe-remote`.

#### Claude Code (recommended)

```bash
npm install -g @anthropic-ai/claude-code
```

#### Codex

```bash
npm install -g @openai/codex
```

#### OpenCode

```bash
go install github.com/opencode-ai/opencode@latest
```

> If you use Gemini CLI, install it normally on your machine and make sure it is available in your `PATH`.

### 2) Install vibe-remote

**macOS / Linux**

```bash
curl -fsSL https://vibe-remote.com/install.sh | sh
```

**Windows (PowerShell)**

```powershell
irm https://vibe-remote.com/install.ps1 | iex
```

### 3) Start the agent

```bash
vibe-remote
```

The TUI opens.

Press **`c`** to configure your **connector name** and **password**.

The agent connects to the relay automatically and shows a QR code on the Dashboard tab.

### 4) Connect from iPhone

1. Install **vibe-remote** from the App Store
2. Tap **+** (Add Connector)
3. Scan the QR code from the TUI
4. Start a session and send your first prompt

That is it.

## First session in under a minute

A good first run looks like this:

```bash
vibe-remote
```

Then on your phone, try prompts like:

- `read the README and explain this repo`
- `run the test suite and tell me what failed`
- `check if the dev server is running and start it if needed`

## CLI reference

```bash
vibe-remote              Start TUI (default)
vibe-remote --headless   Start without TUI
vibe-remote relay        Run as relay server
vibe-remote update       Update to latest version
vibe-remote version      Show version
vibe-remote help         Show help
```

### Headless mode

Useful on Windows or for non-TUI environments:

```bash
vibe-remote --headless --connector myconnector --password mypassword
```

## TUI shortcuts

### Dashboard tab

| Key | Action |
| --- | --- |
| `c` | Config — set connector name & password |
| `w` | Switch relay server |
| `d` | Manage connected devices |
| `r` | Refresh QR code |
| `h` | Show / hide QR code |
| `m` | Toggle QR role (Admin / Member) |
| `y` | Copy QR link to clipboard |
| `t` | Desktop Help |
| `i` | Install QR (App Store link) |
| `s` | Stop server |
| `q` | Quit TUI |
| `1 / 2 / 3` | Switch tabs (Dashboard / Logs / Install) |

## Features

- **Native iOS experience** for controlling AI coding sessions
- **Zero-config relay** that works through NAT/firewalls without VPN setup
- **Multi-provider support** across Claude Code, Codex, Gemini CLI, and OpenCode
- **Persistent sessions** that survive long-running work
- **Live output streaming** back to your phone
- **Scheduled tasks** for automated jobs
- **Live localhost preview** on your phone
- **Team Mode** for shared access to the same machine *(experimental)*
- **Self-hosted relay option** for teams with stricter privacy requirements

## Security & privacy

`vibe-remote` is designed so the relay is transport, not trust.

- **End-to-end encrypted communication**
- **Zero-knowledge relay model** — the relay forwards what it cannot read
- **Connector password stored locally** and hashed with bcrypt
- **Cryptographically random session tokens**
- **Optional self-hosted relay** for teams that want full control

For relay setup and self-hosting details, see the docs:

- https://vibe-remote.com/doc/getting-started
- https://vibe-remote.com/doc/relay
- https://vibe-remote.com/doc/providers

## Pricing

`vibe-remote` is **free forever** with a generous free tier.

- Up to **3 directories**
- **1 persistent session window** per directory
- **1 scheduled task**
- No time limit
- No credit card required

New users also get a **free PRO trial** with full access.

PRO subscriptions are managed through the Apple App Store.

## Platform support

- **Machine running the agent:** macOS, Linux, Windows
- **Mobile app:** iPhone (iOS 26+)

> Windows does not have the TUI today. Use headless mode instead.

## Philosophy

> If an AI can do it, you should not have to do it manually on your phone.

`vibe-remote` is not trying to recreate a full desktop IDE on iPhone.
It is trying to give you the smallest, fastest control surface possible for modern AI coding workflows.

## License

Proprietary. All rights reserved.
