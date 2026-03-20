# ConsulAI — Indian Consular Services Assistant

Context-aware AI agent for Indian nationals in Germany. Built with vanilla HTML/JS + Anthropic Claude API.

---

## 🚀 Deploy in 15 minutes (GitHub + Vercel)

### Step 1 — Push to GitHub

1. Go to **github.com** → click **New repository**
2. Name it `consulai` → set to **Public** → click **Create repository**
3. Upload these files (drag and drop onto the page):
   - `index.html`
   - `vercel.json`
   - `api/chat.js`
   - `.gitignore`

### Step 2 — Deploy on Vercel

1. Go to **vercel.com** → sign up with your GitHub account
2. Click **Add New Project** → import your `consulai` repository
3. Vercel auto-detects the config — just click **Deploy**
4. Your site goes live at `https://consulai-yourname.vercel.app`

### Step 3 — Add your API key (IMPORTANT — do this or the chat won't work)

1. In Vercel dashboard → go to your project → **Settings** → **Environment Variables**
2. Add a new variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your key from console.anthropic.com
3. Click **Save** → go to **Deployments** → click **Redeploy**

That's it — your app is live and the API key is safe on the server. ✅

---

## 🔁 Auto-deploy on every update (optional)

Every time you push changes to the `main` branch on GitHub, Vercel auto-deploys. No manual steps needed.

To enable GitHub Actions auto-deploy:
1. In Vercel → Settings → Tokens → create a token, copy it
2. In GitHub repo → Settings → Secrets → add:
   - `VERCEL_TOKEN` — your Vercel token
   - `VERCEL_ORG_ID` — found in Vercel Settings → General
   - `VERCEL_PROJECT_ID` — found in your project Settings → General

---

## 🌐 Custom domain (optional)

1. Buy a domain e.g. `consulai.in` at namecheap.com
2. In Vercel → your project → **Domains** → add your domain
3. Follow Vercel's DNS instructions (takes ~10 minutes to propagate)

---

## 📁 File structure

```
consulai/
├── index.html          ← the entire app (HTML + CSS + JS)
├── vercel.json         ← Vercel routing config
├── .gitignore
└── api/
    └── chat.js         ← serverless proxy (keeps API key secret)
```

---

## 🔐 Security

- Your `ANTHROPIC_API_KEY` is stored as a Vercel environment variable — never exposed in browser source code
- The `/api/chat` proxy validates requests before forwarding to Anthropic
- Set a monthly spend limit at console.anthropic.com → Settings → Limits as an extra safeguard
