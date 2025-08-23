# n8n-smm
[n8n](https://github.com/n8n-io/n8n) workfow for automate my blog publishing process.

# Roadmap
- [x] Dummy n8n setup in compose
- [x] Find free hosting to host this (xxx-dev)
- [ ] Docker compose + GitHub Actions + free hosting CI/CD 
- [ ] Trigger workflow when new post was published in telegram channel
- [ ] ~~Git Keeper to automatically commit & push when workflows has been modified~~
- [ ] Process the telegram post
- [ ] Translate into english
- [ ] Parse post meta (Title, content, tags)
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
