# poloniex_ethbot

A bot that does cost averaging into ether from bitcoin on Poloniex. It texts
you when your bitcoin balance gets low so you can send more bitcoin to your
account.

Before using the bot, you'll need to install its requirements. The easiest way
is via [pip](https://pip.pypa.io/en/stable/installing/):

```
pip install -r requirements.txt
```

To use this, copy `config.example.yaml` to `config.yaml` and fill in your
settings. The file should be pretty self-explanatory. Then set up
`python bot.py` to run periodically. I personally use cron for that. My crontab
is set up to run the script once every hour:

```
0 * * * * python /home/ryan/muninn/poloniex_ethbot/bot.py --log=WARN
```
