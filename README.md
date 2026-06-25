# Calcify

A single-page desk of calculators — Arithmetic, Scientific, Loan EMI, Compound Interest, BMI, Unit Converter, Age, and Speed. Pure HTML/CSS/JS in one file, no build step and no dependencies (other than Google Fonts loaded over CDN).

## Files

- `index.html` — the entire app. This is all you need to deploy.
- `vercel.json` — optional static config (clean URLs). Safe to delete.
- `README.md` — this file.

## Deploy to Vercel

Because the app is a single static `index.html`, Vercel needs no build step and no framework. Pick whichever method you prefer.

### Option A — Git import (recommended)

1. Put these files in a folder and push to a GitHub/GitLab/Bitbucket repo.
2. Go to https://vercel.com/new and import the repo.
3. Leave every setting at its default:
   - **Framework Preset:** Other
   - **Build Command:** (leave empty)
   - **Output Directory:** (leave empty / root)
4. Click **Deploy**. Done.

### Option B — Vercel CLI

```bash
npm i -g vercel       # install the CLI once
cd path/to/this/folder
vercel                # creates a preview deployment
vercel --prod         # promotes it to production
```

Accept the defaults when prompted (no build command, output directory = current directory).

## Local preview

Just open `index.html` in a browser, or run any static server:

```bash
npx serve .
# or
python3 -m http.server 8000
```

## Notes

- Calculations use standard math precedence (not left-to-right calculator chaining), and every tool computes live as you type.
- EMI and Compound Interest both use **compound** interest — EMI on a reducing loan balance, Compound Interest on a growing balance.
- No data leaves the browser; there is no backend and no storage.
