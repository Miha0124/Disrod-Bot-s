# Disrod-Bot-s

Discord bot for publishing formatted game announcements in Russian and English.

## Setup

1. Create a Discord application and bot in the Developer Portal.
2. Enable the **Message Content Intent** if you plan to use prefix commands (not required here).
3. Invite the bot to your server with the `applications.commands` scope.
4. Create a `.env` file or export `DISCORD_TOKEN` with your bot token.

## Install

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Run

```bash
python bot.py
```

## Usage

Use the `/announce` slash command and fill in the fields:
- **game**
- **version**
- **ru_description**
- **en_description**
- **ru_log1**
- **ru_log2**
- **en_log1**
- **en_log2**

The bot will send a formatted embedded message with both languages.
