# Joy Bot

## Overview
This is a Facebook Messenger bot built with Node.js. It provides an automated bot system for Facebook Messenger with various commands, premium features, and admin controls.

## Project Structure
- `JOY/catalogs/JOYA.js` - Main entry point, starts Express server and bot
- `JOY/catalogs/JOYB.js` - Core bot logic and Facebook login
- `JOY/catalogs/JOYC.js` - Logger utility
- `JOY/catalogs/JOYD.js` - Additional utilities
- `JOY/system/` - Core system files (database, handlers, WebSocket FCA)
- `scripts/commands/` - Bot commands
- `scripts/events/` - Event handlers (join, leave, update)
- `Config.json` - Bot configuration (name, prefix, admins)
- `JOY/configs/Joy.json` - Advanced bot settings
- `Joystate.json` - Facebook session state (required for authentication)

## Setup Requirements
1. The bot requires a valid Facebook `Joystate.json` to authenticate
2. Configure `Joy.json` with your bot settings
3. The web interface runs on port 5000

## Key Configuration Files
- `Joy.json` - Main bot settings (bot name, prefix, operators)
- `JOY/configs/JOY.json` - Login options and API settings
- `JOY/configs/api.json` - API credentials
- `JOY/configs/console.json` - Console output settings

## Running
The bot starts via `node JOY/catalogs/JOYA.js` which:
1. Starts an Express server on port 5000
2. Spawns the main bot process (JOYB.js)
3. Handles auto-restart on crashes

## Database
Uses SQLite database stored at `JOY/botdata/maindata.sqlite`

## Technologies
- Node.js with Express
- ws3-fca (Facebook Chat API)
- Sequelize + SQLite for data persistence
