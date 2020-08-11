# LINE VideoPlayComplete & Unsend event handle bot

News:

- [Video play complete](https://developers.line.biz/en/reference/messaging-api/#video-viewing-complete)
- [Unsend](https://developers.line.biz/en/reference/messaging-api/#unsend-event)

## Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

# Developer Side

## LINE account

- Got A LINE Bot API devloper account
Make sure you already registered, if you need use LINE Bot.


- Go to LINE Developer Console
    - Close auto-reply setting on "Messaging API" Tab.
    - Setup your basic account information. Here is some info you will need to know.
        - Callback URL: `https://{NGROK_URL}/webhooks/line`
        - Verify your webhook.
- You will get following info, need fill back to `.env` file.
    - Channel Secret
    - Channel Access Token (You need to issue one here)

## Normal testing

1. first terminal window
```
cp .env.sample .env
pip install -r requirements.txt --user
python api.py
```

> [2020/03/28] LINE just not already release tag in SDK, so I use git method to install NEW feature package(icon switch).
2. Create a provisional Https:

```
ngrok http 5000
```

or maybe you have npm environment:

```
npx ngrok http 5000
```
![](https://i.imgur.com/azVdG8j.png)

3. Copy url to LINE Developer Console

# License

MIT License

