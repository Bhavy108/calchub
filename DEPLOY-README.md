# CalcHub — Deployment Guide

Your site is a **static website** (plain HTML/CSS/JS — no server or database needed). That makes it fast to put live, today, for free.

## Folder structure
```
calc-site/
├── index.html          ← homepage
├── style.css            ← shared styles
└── calculators/
    ├── chrome.js         ← shared header/footer
    ├── loan-emi.html
    ├── bmi.html
    ├── ... (23 calculator pages total)
```

---

## STEP 1 — Put it live (choose ONE, both are free)

### Option A: Netlify (easiest, recommended — 2 minutes)
1. Go to **https://app.netlify.com/drop**
2. Drag the entire `calc-site` folder onto the page
3. Netlify gives you a live URL instantly, like `https://your-name-123.netlify.app`
4. Done — your site is live on the internet right now.
5. (Optional) In Netlify dashboard → "Domain settings" → you can rename the subdomain or connect a custom domain like `calchub.com` if you buy one.

### Option B: GitHub Pages (also free, good if you already use GitHub)
1. Create a free account at **https://github.com** if you don't have one
2. Create a new repository, e.g. `calchub`
3. Upload all files from `calc-site` folder (drag-and-drop on the GitHub website works)
4. Go to repo **Settings → Pages**
5. Under "Source", select the `main` branch and `/ (root)` folder → Save
6. Your site goes live at `https://your-username.github.io/calchub/` within a few minutes

---

## STEP 2 — Get it on Google (so people can actually find it via search)

Going "live" (Step 1) just means the site has a URL. To appear in Google search results, you need to get it **indexed**:

1. Go to **Google Search Console**: https://search.google.com/search-console
2. Add your site URL (the Netlify or GitHub Pages link, or your custom domain)
3. Verify ownership (Search Console will guide you — usually a meta tag or DNS record)
4. Once verified, use **"URL Inspection"** → paste your homepage URL → click **"Request Indexing"**
5. Do the same for a few key calculator pages (loan-emi.html, bmi.html, etc.)
6. Google typically indexes new sites within a few days to 2 weeks — there's no way to force it faster, but requesting indexing speeds it up versus waiting for Google to find it on its own

### To actually rank well (not just appear), over time you'll want:
- A `sitemap.xml` listing all your pages (submit this in Search Console too)
- Unique, descriptive page titles (already done — each calculator has its own `<title>`)
- Some backlinks (other sites linking to you) and genuinely useful content
- Mobile-friendliness (already done — the site is fully responsive)

This part is gradual — calculator.net took years to reach its current ranking. Getting indexed (Step 2 above) is the fast part; ranking high is the slow part.

---

## STEP 3 — Optional but recommended before sharing widely
- [ ] Buy a custom domain (e.g. from Namecheap, GoDaddy, ~₹700-1000/year for a `.com`) and connect it in Netlify/GitHub Pages settings — looks far more trustworthy than a `.netlify.app` subdomain
- [ ] Add Google Analytics or Search Console to track visitors
- [ ] Test every calculator on a real phone before sharing the link
- [ ] Replace `hello@calchub.example` in the homepage CTA with a real email address

---

## Adding more calculators later
23 calculators are fully working now (Financial, Fitness, Math, Other categories). The remaining categories on the homepage link to "coming soon" pages so no link is ever broken. Come back anytime and ask to add a specific calculator — give the name and I'll build it directly into this same site structure.
