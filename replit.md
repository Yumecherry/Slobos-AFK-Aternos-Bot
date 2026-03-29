# Minecraft AFK Bot

A Minecraft AFK bot that keeps an Aternos server online 24/7 using Mineflayer. Includes an Express web dashboard for monitoring bot status.

## Architecture

- **Runtime**: Node.js 20
- **Entry point**: `index.js`
- **Config**: `settings.json`
- **Web dashboard**: Express server on port 5000

## Key Files

- `index.js` — Main bot logic and Express web server (dashboard at `/`)
- `settings.json` — Bot configuration (server IP, credentials, behavior)
- `leaveRejoin.js` — Leave/rejoin logic for queue handling
- `logger.js` — Log utility

## Features

- Auto-connects to Minecraft server via Mineflayer
- Anti-AFK movement (circle walk, random jumps, look-around)
- Auto-reconnect on disconnect
- Auto-auth support for whitelisted servers
- Web dashboard showing bot status, uptime, and logs
- Discord webhook notifications (optional)

## Running

The app runs via `node index.js`. The Express server listens on port 5000 (or `process.env.PORT`).

## Deployment

Configured as a VM deployment (always-running process) since the bot must maintain a persistent Minecraft connection.
