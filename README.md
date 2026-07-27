# 0G Treasury Dashboard

Static, single-file treasury dashboard for 0G Foundation / Labs. Password-gated (client-side only — not real security, just a soft access gate), branded with 0G colors and logo.

## Deploy to GitHub Pages

```bash
# from this github-site/ folder
git init
git add .
git commit -m "Initial treasury dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/finance-dashboard.git
git push -u origin main
```

Then in the repo on GitHub: **Settings → Pages → Source: Deploy from branch → Branch: main / (root)**. GitHub will publish it at:

```
https://<your-username>.github.io/finance-dashboard/
```

It usually takes 1–2 minutes to go live after the first push.

## Updating data

Open `index.html`, find the `SNAPSHOTS` object near the top of the `<script>` block, and add a new dated entry (e.g. `"2026-07-28": [ ... ]`) following the same structure as the existing one. Commit and push — day-over-day change appears automatically once two dates exist.

## Password

Current password: `0g@2026` (set in `const PASSWORD = ...` in `index.html`). Change it there before pushing if you want a different one — remember this repo is public, so treat the password as a light deterrent, not real security.
