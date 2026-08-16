# Dashavatara Runner — Prototype

A browser-based endless runner prototype testing the core mechanic: swap between
avatars (Matsya, Kurma, Varaha) to match the obstacle ahead, under a short
swap cooldown. Eras are time-based, each ending in a scripted "signature moment"
obstacle before transitioning to the next.

Single static HTML file — no build step, no dependencies.

## Run locally

Just open `index.html` in a browser. Or serve it:

```bash
npx serve .
```

## Deploy — GitHub

```bash
git init
git add .
git commit -m "Dashavatara Runner prototype"
gh repo create dashavatara-runner --public --source=. --remote=origin --push
```

(Or create the repo manually on github.com, then `git remote add origin <url>`
and `git push -u origin main`.)

## Deploy — Vercel

1. Go to vercel.com → **Add New... → Project**
2. Import the `dashavatara-runner` GitHub repo
3. Framework Preset: **Other** (no build command needed)
4. Root Directory: leave as `/`
5. Deploy

Vercel serves `index.html` at the project root automatically — zero config.

## Controls

- Tap the on-screen buttons, or press **1 / 2 / 3** on keyboard
- 1 = Matsya (dive water gaps)
- 2 = Kurma (shell vs falling debris)
- 3 = Varaha (dig under root walls)

## What to playtest

- Does the 450ms swap cooldown feel fair, too strict, or too loose?
- Does the signature moment (gold-outlined obstacle near era end) feel like a
  real beat, or does it blend in with regular obstacles?
- Does era length (starts at 26s, +4s per full cycle) feel right, or should
  it grow faster/slower?
- Does mixing older obstacle types into newer eras keep early avatars feeling
  relevant, or does it feel random?
