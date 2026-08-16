# 🚀 How to publish (5 minutes)

## 1. Create the repo on GitHub
Go to https://github.com/new
- Repository name: `draftguard`
- Visibility: **Public** (this repo contains NO source code — only marketing)
- Don't initialize with anything (no README/license — we have them)

## 2. Push this folder
Open a terminal inside the `draftguard-site` folder and run:

```bash
git init
git add .
git commit -m "DraftGuard website & README"
git branch -M main
git remote add origin https://github.com/talaurlove/draftguard.git
git push -u origin main
```

(GitHub will ask you to log in — use your browser or a Personal Access Token.)

## 3. Turn on GitHub Pages
On github.com → your `draftguard` repo → **Settings** → **Pages**:
- Source: **Deploy from a branch**
- Branch: **main** / folder: **/ (root)** → Save

⏱ Wait ~1 minute. Your site goes live at:
**https://talaurlove.github.io/draftguard/**

## 4. Done — username already set
Your username (talaurlove) is already baked into all links in:
- `README.md`
- `index.html`

Then commit & push again:
```bash
git add -A && git commit -m "Set username" && git push
```

## 5. (Optional) Upload the extension as a Release
Repo → **Releases** → **Draft a new release**
- Tag: `v2.0.0`
- Attach: `draftguard.zip` (the packaged extension from the workspace)
- Publish — the download links on the site/README now work.

## ⚠️ Keeping it closed source
- The extension source (`draftguard/` folder) must NEVER be pushed to this
  public repo — the `.gitignore` here blocks it as a safety net.
- The zip you attach to Releases contains the shipped extension (users can
  unzip any Chrome extension anyway — that's true for every extension on the
  Web Store). Your legal protection is the proprietary LICENSE.
- If you also want private version control for the source code, make a
  SECOND repo, set it to **Private**, and push the `draftguard/` folder there.
