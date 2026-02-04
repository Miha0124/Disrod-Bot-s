# Disrod-Bot-s

Discord bot for publishing formatted game announcements in Russian and English.

## Setup

1. Create a Discord application and bot in the Developer Portal.
2. Enable the **Message Content Intent** (required for DM parsing).
3. Invite the bot to your server with the `applications.commands` scope.
4. Export `DISCORD_TOKEN` with your bot token.
5. Add `ALLOWED_USER_IDS` with your Discord ID(s), comma-separated.
6. (Optional) Set `DISCORD_GUILD_ID` if the bot is in multiple servers.
7. (Optional) Set `TRANSLATE_URL` to a LibreTranslate-compatible endpoint.

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

Send the bot a direct message with key/value pairs (one per line).

### Update announcements

```text
game: updates-paradox
version: 1.2.3
ru_description: Русское описание
log: Первый пункт
log2: Второй пункт (опционально)
```

If you send only Russian (`ru_description`, `log`, `log2`) or only English
(`en_description`, `en_log1`, `en_log2`), the bot will auto-translate the
missing language using the configured translation endpoint.

### Project status (edits the last bot message if it exists)

```text
game: status-of-projects
project: Endless Void
version: 0.9.0
status: В разработке / In development
```

The bot will post into the matching channel:
- updates-paradox
- updates-bdft
- update-endless-void
- status-of-projects
