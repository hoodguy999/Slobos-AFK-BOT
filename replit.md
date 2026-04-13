# Minecraft AFK Bot

A Node.js Minecraft AFK bot that keeps Aternos (or similar) servers online 24/7. It uses the `mineflayer` library to simulate a player and includes an Express-based web dashboard.

## Features

- **Auto-reconnect**: Rejoins automatically on disconnect/kick.
- **Anti-AFK**: Jumps, walks in circles, looks around, and sends periodic chat messages.
- **Web Dashboard**: Real-time status page at port 5000 showing bot state, uptime, and coordinates.
- **Self-Ping**: Pings itself every 10 minutes to prevent hosting platforms from sleeping.
- **Discord Webhooks**: Sends connect/disconnect notifications to a Discord channel.

## Tech Stack

- **Runtime**: Node.js 20
- **Minecraft Framework**: `mineflayer` + `mineflayer-pathfinder`
- **Web Server**: Express
- **Package Manager**: npm

## Project Structure

- `index.js` — Main entry point (Express server + bot logic)
- `settings.json` — Configuration (server IP, bot credentials, anti-AFK settings, Discord webhook)
- `leaveRejoin.js` — Periodic leave/rejoin cycle module
- `package.json` — Dependencies and scripts
- `launcher_accounts.json` — Minecraft account data placeholder

## Configuration

Edit `settings.json` to change:
- Target Minecraft server IP and port
- Bot username and authentication type
- Anti-AFK behavior (movement, chat messages, sneak)
- Discord webhook URL
- Auto-reconnect delays

## Running

```bash
npm start
```

The web dashboard is available on port 5000.

## Deployment

Configured as a VM deployment (`node index.js`) to run continuously.
