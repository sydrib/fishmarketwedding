# Libby & Josh — Wedding Website

Static site. No build step.

## Deploy (VS Code → GitHub → Vercel)
1. Put the contents of this folder at the root of your GitHub repo (keep the folder structure).
2. In Vercel: New Project → import the repo → Framework Preset: **Other** → no build command, output directory = root.
3. Add the domain **fishmarketwedding.com** in Vercel → Settings → Domains.

`vercel.json` rewrites `/` → `Home.dc.html`. Every other page is served by its own filename
(e.g. `/The%20Weekend.dc.html`, `/Travel%20%26%20Stay.dc.html`); internal links are already URL-encoded.

## Files
- `*.dc.html` — the seven pages
- `support.js` — page runtime (loads React from unpkg.com)
- `image-slot.js` + `image-slots.state.json` — photo frames and their saved photos/crops. Keep both.
- `assets/` — images, album photos, hero video (desktop + mobile)

RSVP talks to the live Apps Script web app set in `RSVP.dc.html` → `RSVP_API_URL`.
