# MenuAI — Deploy Guide

## What's in this folder

```
menuai-backend/
├── server.js          ← Node.js backend (proxies Claude API)
├── package.json
├── .env.example       ← copy this to .env for local testing
├── .gitignore
└── public/
    └── index.html     ← the full frontend app
```

---

## Deploy on Railway (free, 5 minutes)

Railway is the easiest option — free tier, no credit card needed.

### Step 1 — Push to GitHub
1. Create a new repo on github.com (name it `menuai` or anything)
2. Upload ALL files from this folder into the repo (drag & drop on GitHub works fine)

### Step 2 — Deploy on Railway
1. Go to railway.app → "Start a New Project"
2. Click "Deploy from GitHub repo" → select your repo
3. Railway auto-detects Node.js and deploys

### Step 3 — Add your API key
1. In Railway dashboard → your project → "Variables" tab
2. Add variable:
   - Key: `ANTHROPIC_API_KEY`
   - Value: your key from console.anthropic.com
3. Railway automatically restarts with the key

### Step 4 — Get your public URL
1. Go to "Settings" tab → "Domains"
2. Click "Generate Domain"
3. You get a URL like `https://menuai-production.up.railway.app`

**That's your shareable link. Send it to anyone.**

---

## Deploy on Render (also free)

1. Push code to GitHub (same as above)
2. Go to render.com → "New Web Service"
3. Connect your GitHub repo
4. Build command: `npm install`
5. Start command: `node server.js`
6. Add environment variable: `ANTHROPIC_API_KEY` = your key
7. Deploy → get your `.onrender.com` URL

---

## Test locally first

```bash
# 1. Install dependencies
npm install

# 2. Create .env file
cp .env.example .env
# then edit .env and paste your real API key

# 3. Run
npm start

# 4. Open http://localhost:3000
```

---

## Get your Anthropic API key

1. Go to console.anthropic.com
2. Sign up / log in
3. "API Keys" → "Create Key"
4. Copy the key (starts with sk-ant-...)
5. Add some credits ($5 is enough for hundreds of menus)

---

## Cost per menu generated

Each menu generation makes 2 API calls:
- ~$0.01–0.03 per menu (depends on photo size and menu length)
- $5 of credits = ~200 menus generated
