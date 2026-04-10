# 🏀 Hoop Log — Basketball Training App

A gamified basketball training log for kids. Built as a Progressive Web App (PWA) — install it to your home screen and it works like a native app, including offline.

## Features

- **Multiple player profiles** — each player has their own XP, streaks, and badges
- **7 drill types** — Shooting, Dribbling, Layups, Mikan, Free Throws, Fitness, and 1:1
- **XP & levelling system** — earn XP every session and climb from Rookie to Legend
- **Streak tracking** — daily training streaks with personal best records
- **Shot tracking** — log shots made per session, see today's total on the home screen
- **14 achievement badges** to unlock
- **Session editing** — edit or delete any past session
- **Offline support** — works without internet once installed
- **Dark mode** — automatically follows your device setting

## Install on your phone

**iPhone (Safari only):**
1. Open the app URL in Safari
2. Tap the Share button → Add to Home Screen
3. Tap Add

**Android (Chrome):**
1. Open the app URL in Chrome
2. Tap the three-dot menu → Add to Home screen

## Local development

No build tools required. Just open `index.html` in a browser, or serve it locally:

```bash
npx serve .
```

## Deploying

Drag and drop the project folder to [Vercel](https://vercel.com), [Netlify](https://netlify.com), or [Cloudflare Pages](https://pages.cloudflare.com) for a free live URL.

For GitHub Pages, push this repo and enable Pages from the repository Settings → Pages → set source to the main branch root.

## Tech

Plain HTML, CSS, and vanilla JavaScript. No frameworks, no dependencies, no build step. Data is stored in `localStorage` on the device.
