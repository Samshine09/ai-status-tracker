# 🚀 Deploy to GitHub Pages - Step by Step

## First Time Setup

### 1. Create the Repository

1. Go to https://github.com/new
2. Repository name: `ai-status-tracker` (or whatever you prefer)
3. Set to **Public**
4. ✅ Check "Add a README file" (optional, we have one)
5. Click **Create repository**

### 2. Upload Your Files

**Option A: Via GitHub Web Interface** (easiest)
1. In your new repo, click **Add file** → **Upload files**
2. Drag and drop these three files:
   - `index.html`
   - `README.md`
   - `.gitignore`
3. Commit message: "Initial dashboard"
4. Click **Commit changes**

**Option B: Via Git Command Line**
```bash
cd ai-status-tracker
git init
git add .
git commit -m "Initial dashboard"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/ai-status-tracker.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. In your repo, go to **Settings** (top menu)
2. Scroll down to **Pages** (left sidebar)
3. Under "Build and deployment":
   - Source: **Deploy from a branch**
   - Branch: **main** → **/ (root)**
4. Click **Save**
5. Wait ~1-2 minutes for deployment

### 4. Access Your Dashboard

Your site will be live at:
```
https://YOUR-USERNAME.github.io/ai-status-tracker/
```

GitHub will show you the exact URL at the top of the Pages settings.

---

## Making Updates

After initial setup, to update your dashboard:

1. Edit `index.html` on GitHub (click the file → Edit button)
2. Make your changes
3. Commit → GitHub Pages auto-deploys in ~30 seconds

Or use git:
```bash
git add index.html
git commit -m "Update dashboard"
git push
```

---

## Troubleshooting

**"404 - Page not found"**
- Wait 2-3 minutes after enabling Pages
- Make sure the file is named `index.html` (not `ai-status-dashboard.html`)
- Check that Pages source is set to `main` branch and `/ (root)`

**"CORS errors" in browser console**
- The dashboard uses api.allorigins.win as a proxy — if it's down, try again later
- Alternative: You could set up Cloudflare Workers for your own proxy

**Nothing updates / shows old data**
- Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
- Clear browser cache

---

## Custom Domain (Optional)

Want a custom URL like `status.yourdomain.com`?

1. Buy a domain (Namecheap, Google Domains, etc.)
2. In your DNS settings, add a CNAME record:
   - Name: `status` (or `@` for root)
   - Value: `YOUR-USERNAME.github.io`
3. In GitHub repo settings → Pages → Custom domain
4. Enter your domain and save

Full guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

---

🎉 **You're done!** Your dashboard is now live and auto-updating every 60 seconds.
