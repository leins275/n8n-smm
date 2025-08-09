# n8n-smm
[n8n](https://github.com/n8n-io/n8n) workfow for automate my blog publishing process.

# Roadmap
- [ ] Dummy n8n setup in compose to store workflow files in FS
- [ ] Find free hosting to host this
- [ ] Docker compose + GitHub Actions + free hosting CI/CD 
- [ ] Trigger workflow when new post was published in telegram channel
- [ ] Git Keeper to automatically commit & push when workflows has been modified
- [ ] Process the telegram post
- [ ] Translate into english
- [ ] Parse post meta (Title, content, tags)
- [ ] Publish post in two languages to Hugo blog
- [ ] Publish en IT publications to LinkedIn

# First run

```bash
mkdir -p n8n_files/workflows
# ensure your repo has 'origin' set and auth works (HTTPS PAT or SSH)
git status
docker compose up -d
```