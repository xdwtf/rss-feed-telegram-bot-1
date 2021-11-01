# RSS Feed Telegram Bot
A bot to post messages to Telegram Groups or Channels from rss feed.
- This bot can also send /mirror commands to your mirror bot using your telefdsfdsfgram account.
bcoz bot can't read another bot's mag. So this bot will use your TG account to interact with mirror bot.
Fill `STR_SESSION` and `MIRROR_CHAT_ID` vars to enable it.

## Configuration
- Edit the [rss.py](./rss.py) as your needs.
- Edit values in [config.env](./config.env.template) or set it in Environment Variables. There is an template for `config.env` already exists just edit it and rename the file.

### Configuration Values
- `APP_ID` - Get it from [my.telegram.org](https://my.telegram.org/apps)
- `API_HASH` - Get it from [my.telegram.org](https://my.telegram.org/apps)
- `BOT_TOKEN` - Get it by creating a Telegram bot on [BotFather](https://t.me/BotFather)
- `FEED_URLS` - List of URLs of RSS Feed, sperated by `|` vertical bar.
- `LOG_CHAT` - ID of the Telegram Chat where messages are to be posted.
- `DATABASE_URL` - Here is a full [guide](https://github.com/SpEcHiDe/NoPMsBot/wiki/How-to-Install-Database-%3F). For Heroku, just add the `Heroku Postgres` add-on.
- `INTERVAL` - Checking Interval in seconds. (optional)
- `MAX_INSTANCES` - Max instances to be used while checking rss feed. (optional)
### Working as a userbot on your behalf to interact with mirror bot.

These variabls are required only if you want to use your tg account to send /mirror cmd to any mirror bot.
- `MIRROR_CHAT_ID` - Group/chat_id of mirror chat or mirror bot to send mirror cmd.
- `MIRROR_CMD` - if you have changed default cmd of mirror bot, replace this.
- `STR_SESSION` - String session generate using your tg mobile number for sending mirror cmd on your behalf. Generate by running
```
python gen_str.py 
```
(heroku users run in heroku console)

## Deployment

### Deploying on Railway
[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2FiamLiquidX%2Frss-feed-telegram-bot&plugins=postgresql&envs=API_ID%2CAPI_HASH%2CFEED_URLS%2CBOT_TOKEN%2CLOG_CHANNEL%2CINTERVAL%2CMAX_INSTANCES%2CSTR_SESSION%2CMIRROR_CHAT_ID%2CMIRROR_CMD&API_IDDesc=Get+it+from+my.telegram.org&API_HASHDesc=Get+it+from+my.telegram.org&FEED_URLSDesc=RSS+Feed+URL+of+the+site.+Split+by++%7C++if+there+are+more+than+one.&BOT_TOKENDesc=Get+it+by+creating+a+bot+on+https%3A%2F%2Ft.me%2Fbotfather&LOG_CHANNELDesc=Create+a+channel+%2C+send+a+message+and+forward+that+message+to+%40username_to_id_bot+%2C+you+will+get+channel+id.&INTERVALDesc=Times+between+checks.&MAX_INSTANCESDesc=2-3+is+more+than+enough.&STR_SESSIONDesc=Fill+this+if+you+wanna+setup+autoleech+or+automirror+system.&MIRROR_CHAT_IDDesc=Only+useful+if+u+filled+string+session+variable.+This+will+send+mirror+commands+on+your+behalf+to+the+mentioned+chat+id.&MIRROR_CMDDesc=Mirror+command+of+your+bot.)

### Deploying on Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

### VPS or any other server/pc

- Install requirements from [requirements.txt](./requirements.txt)
```
pip3 install -r requirements.txt
```
- Deploy
```
python3 rss.py
```

## Copyright & License
- Copyright (©) 2021 by [Adnan Ahmad](https://github.com/viperadnan-git)
- Licensed under the terms of the [GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007](./LICENSE)
