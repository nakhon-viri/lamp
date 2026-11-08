<p align="center">
  <img src="icon.png" width="128" height="128" alt="Lamp app icon">
</p>

<h1 align="center">Lamp</h1>

<p align="center">
  Save your shell commands and run them in one click from the macOS menu bar.
</p>

<p align="center">
  <a href="https://github.com/nakhon-viri/lamp/releases/download/v1.0.0/Lamp-1.0.0.dmg"><strong>Download for macOS</strong></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/nakhon-viri/lamp/releases">All releases</a>
</p>

---

Lamp is for developers who keep typing the same commands: dev servers, `docker compose`, project scripts. Save each one once, then start and stop it from the menu bar.

Commands run through your login shell, so your `PATH` and `.zshrc` work as they do in Terminal. Lamp handles all of these:

- Quick commands like `pwd`
- Commands that hand off to a daemon, like `docker compose up -d`
- Long-running processes like dev servers

## Features

| | |
|---|---|
| **Menu bar control** | Start, stop, and restart commands, with live status and the latest output line |
| **Organized commands** | Name, working directory, and environment variables per command, in nested folders, with search across all of them |
| **Real-time logs** | ANSI colors, search, copy, export, and optional per-command log files |
| **Port detection** | See the ports a process is listening on and open them in your browser |
| **Automation** | Start commands when Lamp launches, and restart them when they exit: never, on failure, or always |
| **Placeholders** | Write `{{name}}` in a command and Lamp asks for the value before running, remembering the last one |
| **Quick jumps** | Open a command's folder in Terminal, VS Code, or Finder |
| **Clean shutdown** | Stops the processes it started when it quits or crashes, and never touches processes it did not start |
| **Launch at login** | Optional, so your menu bar is ready when you are |

## Install

1. Download [`Lamp-1.0.0.dmg`](https://github.com/nakhon-viri/lamp/releases/download/v1.0.0/Lamp-1.0.0.dmg).
2. Open it and drag **Lamp** to **Applications**.
3. Launch Lamp from Applications. Its icon appears in the menu bar; there is no Dock icon.

Drag Lamp to Applications before launching it. Launch at login does not work correctly when the app runs from the disk image.

Lamp requires **macOS 26.4 or later**. The app is signed with a Developer ID and notarized by Apple.

## Your data

Lamp keeps everything on your Mac and has no account or telemetry.

| What | Where |
|---|---|
| Commands, folders, environment variables, and last placeholder values | `~/Library/Application Support/lamp/commands.json` |
| Log files, if you turn them on | `~/Library/Logs/lamp/` |

> [!WARNING]
> Environment variables and placeholder values are stored as plain text, readable only by your macOS user. While a command runs, its environment variables can also appear in `ps` output for that user. Keep this in mind before saving API keys or tokens.

## Security note

Lamp runs whatever you save, with your user's permissions, and is not sandboxed. Only add commands you trust.
