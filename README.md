# 세종한국어 1B — Study Hub

A gamified, interactive 4-week review homepage for the King Sejong Korean 1B workbook (units 9–16).

## Features
- 4-week study plan with daily tasks and XP tracker
- Interactive Monday lesson: vocab table, dialogue, cover-and-recall cards, checklist
- Grammar quick-reference for all core patterns (units 9–16)
- LocalStorage progress persistence (XP, streak, daily award)
- Fully responsive — works on mobile and desktop

## Project structure
```
sejong-study/
├── index.html     # entire app — single self-contained file
├── Dockerfile     # for Railway / any Docker host
└── README.md
```

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/sejong-study.git
   git push -u origin main
   ```

2. In your repo on GitHub:
   - Go to **Settings → Pages**
   - Source: **Deploy from a branch**
   - Branch: `main` / `root`
   - Click **Save**

3. Your site will be live at:
   `https://YOUR_USERNAME.github.io/sejong-study/`

## Deploy to Railway

### Option A — via GitHub (recommended)
1. Push to GitHub (steps above)
2. Go to [railway.app](https://railway.app) → **New Project → Deploy from GitHub repo**
3. Select your `sejong-study` repo
4. Railway auto-detects the `Dockerfile` and builds it
5. Click **Generate Domain** to get a public URL

### Option B — via Railway CLI
```bash
npm install -g @railway/cli
railway login
railway init
railway up
```

## Local preview
Open `index.html` directly in any browser — no build step or server needed.

```bash
# Or serve with any static server:
npx serve .
python3 -m http.server 8080
```

## Customising
- **Add your XP manually**: Open browser DevTools → Console and run:
  `localStorage.setItem('sejong_xp', '200'); location.reload();`
- **Reset progress**: `localStorage.clear(); location.reload();`
- **Add more lessons**: Duplicate the lesson section in `index.html` and update the vocab/dialogue data arrays in the `<script>` block.
