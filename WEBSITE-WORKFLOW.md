# Karina Cross Fitness — Website Workflow

**Live site:** https://karinacrossfitness.netlify.app/  
**Repo:** https://github.com/gilkman/karinacrossfitness  
**Files:** `~/karina-cross-v2/`

---

## One-Time Setup (done)

- [x] GitHub repo created and code pushed
- [x] Netlify site deployed and linked to GitHub
- [x] `netlify.toml` config added

---

## How to Edit the Site

### 1. Open the project folder
```
cd ~/karina-cross-v2
```

### 2. Create a working branch (recommended)
```
git checkout -b your-name-edit
```
This keeps `main` clean and gives you a preview URL before going live.

### 3. Edit the files
Open `index.html` in any text editor (VS Code, TextEdit, etc.)

### 4. Preview locally
```
cd ~/karina-cross-v2
python3 -m http.server 8080
```
Then open `http://localhost:8080` in your browser.

### 5. Commit and push
```
git add .
git commit -m "describe what you changed"
git push -u origin your-name-edit
```

### 6. Review the preview
Netlify will post a comment on the commit with a preview URL. Open it and check everything looks good.

### 7. Merge to main
```
git checkout main
git merge your-name-edit
git push
```
Netlify auto-deploys `main` to the live site within ~30 seconds.

---

## Useful Commands

**Check git status:**
```
cd ~/karina-cross-v2
git status
```

**See recent commits:**
```
cd ~/karina-cross-v2
git log --oneline -5
```

**Switch back to main (before starting new work):**
```
cd ~/karina-cross-v2
git checkout main
git pull
```

---

## Troubleshooting

**Netlify deploy didn't trigger?**
Go to app.netlify.com → karinacrossfitness → Deploys → click "Trigger deploy" → "Deploy last commit"

**Site looks broken after a push?**
Go to app.netlify.com → karinacrossfitness → Deploys → find a working commit → click "Deploy preview"

**Git auth issues (read-only error)?**
Run `gh auth login --hostname github.com --token` and paste your GitHub PAT with `repo` scope.

---

## Quick Reference

| Task | Command |
|------|---------|
| Start local preview | `cd ~/karina-cross-v2 && python3 -m http.server 8080` |
| Push changes | `cd ~/karina-cross-v2 && git add . && git commit -m "msg" && git push` |
| Check status | `cd ~/karina-cross-v2 && git status` |
| Create branch | `cd ~/karina-cross-v2 && git checkout -b branchname` |
| Merge branch | `cd ~/karina-cross-v2 && git checkout main && git merge branchname && git push` |

---

## Netlify Dashboard
https://app.netlify.com/teams/tom-av-onfe/projects

Any questions — just ask Hermes. Good luck with the redesign!
