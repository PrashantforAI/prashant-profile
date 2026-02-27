# Setup Instructions — AI Prashant Chat

Follow these steps exactly, in order.

---

## STEP 1 — Add files to your project folder

Copy these files into your existing project folder (same level as index.html):

```
prashant-profile/
├── index.html          ← already exists
├── Images/             ← already exists
├── api/
│   └── chat.js         ← NEW — copy from this folder
├── vercel.json         ← NEW — copy from this folder
├── .env.example        ← NEW — copy from this folder
├── .gitignore          ← NEW — copy from this folder
└── .env                ← NEW — you create this (see Step 2)
```

---

## STEP 2 — Create your .env file

1. Duplicate `.env.example` and rename the copy to `.env`
2. Get your Gemini API key from: https://aistudio.google.com/app/apikey
3. Open `.env` and replace `your_gemini_api_key_here` with your actual key:

```
GEMINI_API_KEY=AIzaSy.....yourkey.....
```

4. Save it. Never share this file or commit it to GitHub.

---

## STEP 3 — Add the chat widget to index.html

1. Open `ANTIGRAVITY-CHAT-WIDGET-PROMPT.md`
2. Copy the entire prompt
3. Open Antigravity with your current `index.html`
4. Paste the prompt and let it add the chat widget
5. Save the updated `index.html`

---

## STEP 4 — Add environment variable to Vercel

This is critical — Vercel needs the API key too:

1. Go to vercel.com → your project → Settings → Environment Variables
2. Click "Add New"
3. Name: `GEMINI_API_KEY`
4. Value: your actual Gemini API key
5. Environment: check Production, Preview, and Development
6. Click Save

---

## STEP 5 — Push to GitHub

In GitHub Desktop:
1. You'll see all new files listed as changes
2. Write commit message: "Add AI chat widget and Gemini API backend"
3. Click "Commit to main"
4. Click "Push origin"

Vercel auto-deploys in ~60 seconds.

---

## STEP 6 — Test it

1. Go to your live Vercel URL
2. Wait 8 seconds — a tooltip should appear above the green chat button
3. Click the button — panel slides up
4. Ask "What have you built?" — should get a confident response as Prashant
5. Test a few more questions

---

## TROUBLESHOOTING

**Chat says "Something went wrong":**
- Check Vercel dashboard → Functions tab → look for errors in the chat.js logs
- Most likely the GEMINI_API_KEY env variable wasn't saved correctly in Vercel

**Panel opens but no response:**
- Open browser DevTools → Network tab → look for the /api/chat request
- Check what error is returned

**Works locally but not on Vercel:**
- Confirm the env variable is set in Vercel dashboard (not just in .env file)
- .env file is only for local development — Vercel uses its own env variable store

---

## TESTING LOCALLY (optional)

If you want to test before pushing:

```bash
npm install -g vercel
vercel dev
```

This runs your site locally at http://localhost:3000 with the API function working.
