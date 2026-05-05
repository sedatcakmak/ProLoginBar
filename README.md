# ProLoginBar

A login bar plugin for AuthMe-based auth lobbies. While a player is logging in or registering, ProLoginBar shows a title, subtitle, action bar and boss bar with a live countdown, then optionally forwards the player to a BungeeCord server once authenticated.

## Features

- Hooks into AuthMe login / register events.
- Title and subtitle with configurable fade-in / stay / fade-out, separate texts for login, register, and post-login states.
- Action bar messages for login, register and generic password prompts.
- Boss bar with optional progress decrease and color shift over time.
- Optional kick after a configurable timeout if the player does not authenticate.
- Optional BungeeCord forwarding to a target server after successful login.
- `/send` and `/server` helper commands for BungeeCord transfers.

## Requirements

- Minecraft / Spigot 1.16+ (built against Spigot API 1.16.5).
- Java 8 or newer.
- AuthMe (soft dependency — required if you want the login bar behavior).
- BungeeCord (only if you enable `bungeecord: true` in config).

## Commands

- `/send [player] (server)` — send a player to a BungeeCord server.
- `/server (name)` — send the executing player to a BungeeCord server.

## Installation

1. Drop `ProLoginBar.jar` into `plugins/`.
2. Make sure AuthMe is installed.
3. Start (or restart) the server to generate `config.yml`.
4. Edit `plugins/ProLoginBar/config.yml`, then restart or reload.

## Configuration

`config.yml` controls:

- `bungeecord` — enable / disable BungeeCord transfer after login.
- `server` — target server name, teleport time, and related messages.
- `kick` — auto-kick on timeout (toggle, time, message).
- `boss_bar` — message, color, style, progress, color cycling.
- `action_bar` — login / register / generic messages.
- `title` — title and subtitle for login, register and post-login (teleporting) states with fade timings.

Set any message to `""` to disable that specific element.
