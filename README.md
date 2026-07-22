# EEE Journal — EmotionEvent Entanglement

**app.thinkandgrowjoy.com** · Hosted via GitHub Pages

Part of the [Think and Grow Joy](https://thinkandgrowjoy.com) system.

## What it is

A single-file emotional intelligence journaling app based on the Abraham-Hicks 22-point Emotional Guidance Scale. Log your emotional state. Log the experiences that manifest days later. Watch the entanglement emerge.

- **22-point Emotional Arc** — visualised as a live chart
- **F-Row Manifestation** — experiences link to the emotion that created them, however many days later
- **11-point Experience Quality Scale** — rate what manifested (1 Disgusting → 11 Divine)
- **Fully private** — all data stays on your device via localStorage. No server, no account, no tracking.

## Deploy

### 1. Create the repo
New repo on GitHub: `shaz010/eee-journal` (public)

### 2. Push
```bash
git init
git add .
git commit -m "EEE Journal — initial deploy"
git remote add origin https://github.com/shaz010/eee-journal.git
git push -u origin main
```

### 3. Enable GitHub Pages
Repo → Settings → Pages → Source: Deploy from branch → Branch: `main` / `/ (root)`

### 4. Point the subdomain
At your domain registrar, add one DNS record:

```
Type:  CNAME
Name:  app
Value: shaz010.github.io
```

SSL certificate is provisioned automatically by GitHub once DNS resolves (~minutes to a few hours).

### 5. Icons (required for PWA install prompt)
Add two PNG icons to an `icons/` folder:
- `icons/icon-192.png` — 192×192px
- `icons/icon-512.png` — 512×512px

Design: dark background (#070710), violet EEE monogram or symbol. Without these the app still works — just no install prompt on Android. iOS uses the apple-touch-icon fallback.

## Files

| File | Purpose |
|---|---|
| `index.html` | The complete app — b54 |
| `manifest.json` | PWA manifest — makes it installable |
| `sw.js` | Service worker — offline support |
| `CNAME` | GitHub Pages custom domain |
| `icons/` | App icons (add manually — see above) |

## Version history

- **b54** — emotion→experience causal link via `emotionDate` field; F-row shows manifestations by emotion date not experience date; experience picker follows emotion date
