# AI Provider Status Tracker 🔍

A live dashboard tracking error rates and incidents across major AI providers:
- **Anthropic** (Claude)
- **OpenAI** (ChatGPT)
- **Google** (Gemini)
- **xAI** (Grok)

## What It Does

- Fetches real-time status from official Statuspage APIs
- Shows 90-day incident history
- Auto-refreshes every 60 seconds
- Visualizes incident trends over time

## Quick Start

**Option A: View locally**
1. Download the repo
2. Open `index.html` in your browser
3. Done! No server needed.

**Option B: Host on GitHub Pages** (recommended)
1. Fork or create a new repo with these files
2. Go to **Settings** → **Pages**
3. Set source to **main branch** → **/ (root)**
4. Save and wait ~1 minute
5. Visit `https://YOUR-USERNAME.github.io/REPO-NAME`

## How It Works

The dashboard uses the public JSON APIs from Statuspage.io:
- `https://status.anthropic.com/api/v2/summary.json`
- `https://status.openai.com/api/v2/summary.json`
- `https://status.x.ai/api/v2/summary.json`

Since browsers block cross-origin requests, we route through a CORS proxy (`api.allorigins.win`). No API keys required!

## Note on Accuracy

Official status pages typically only show confirmed incidents, not elevated error rates or subtle degradation. This dashboard helps you spot patterns, but real-world reliability might differ from reported status.

## Tech Stack

- Pure HTML/CSS/JS (no build step)
- Chart.js for visualization
- Fetches from public Statuspage APIs

## License

MIT - feel free to modify and share!

---

*Built to test the theory that some AI providers are flakier than they admit* 😉
