# n8n-smm
[n8n](https://github.com/n8n-io/n8n) workfow for automate my blog publishing process.

# Roadmap
- [x] Dummy n8n setup in compose
- [x] Find free hosting to host this (xxx-dev)
- [x] Docker compose + GitHub Actions + free hosting CI/CD 
- [x] Trigger workflow when new post was published in telegram channel
- [ ] ~~Git Keeper to automatically commit & push when workflows has been modified~~
- [x] Process the telegram post
- [ ] Translate into english
- [x] Parse post meta (Title, content, tags)
- [ ] Publish post in two languages to Hugo blog
- [ ] Publish en IT publications to LinkedIn

# Run

```bash
docker compose up -d
```

# Setup 

## Telegram bot trigger

1. Create new bot in BotFather
2. Provide token to n8n
3. Add bot as an admin to the channel
4. Provide correct https webhook

```bash
curl -s "https://api.telegram.org/bot8181930383:<tg-token>/getWebhookInfo" | jq
curl -s "https://api.telegram.org/bot8181930383:<tg-token>/deleteWebhook?drop_pending_updates=true" 
curl -s "https://api.telegram.org/bot8181930383:<tg-token>/setWebhook" \
  --data-urlencode "url=https://n8n.leins275.xyz/webhook/<n8n-token>/webhook" \
  --data "allowed_updates[]=channel_post" \
  --data "ip_address=$(dig +short n8n.leins275.xyz A | head -n1)"
```