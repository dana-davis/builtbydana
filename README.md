# builtbydana.com

Personal website for Dana — UI/UX Designer & Redesign Specialist.

**Stack:** Pure HTML, CSS, JavaScript — no build tools, no dependencies.

---

## Project structure

```
builtbydana/
├── index.html     ← main page
├── style.css      ← all styles
├── script.js      ← nav scroll, mobile menu, fade-in animations
└── README.md      ← this file
```

---

## Before you deploy — quick personalizations

Open `index.html` and update these things:

| What | Where to look |
|------|---------------|
| Email address | `href="mailto:hello@builtbydana.com"` — update to your real email |
| LinkedIn URL  | `href="#"` next to "LinkedIn" in the contact section |
| Dribbble URL  | `href="#"` next to "Dribbble" in the contact section |
| Read.cv URL   | `href="#"` next to "Read.cv" in the contact section |
| Your photo    | Replace the `<div class="about__photo-placeholder">` block with `<img src="your-photo.jpg" alt="Dana" style="width:100%;height:100%;object-fit:cover;border-radius:20px;">` |
| Portfolio work | Update the three `.work-card` sections with real project names, tags, and images |

---

## Deploy to Netlify (free — recommended)

Netlify is the fastest way to get `builtbydana.com` live. It takes about 5 minutes.

### Step 1 — Create a free Netlify account
Go to [netlify.com](https://netlify.com) and sign up (free tier is all you need).

### Step 2 — Deploy the site

**Option A — drag & drop (fastest):**
1. In Netlify dashboard, click **"Add new site" → "Deploy manually"**
2. Drag and drop the entire `builtbydana/` folder onto the page
3. That's it — Netlify gives you a `random-name.netlify.app` URL immediately

**Option B — connect to GitHub (recommended for future updates):**
1. Push this folder to a new GitHub repo:
   ```bash
   cd ~/builtbydana
   git init
   git add .
   git commit -m "Initial commit"
   gh repo create builtbydana --public --push --source=.
   # or use: git remote add origin <your-repo-url> && git push -u origin main
   ```
2. In Netlify: **"Add new site" → "Import an existing project" → GitHub**
3. Select your repo — Netlify auto-detects it's a static site, no build settings needed
4. Click **Deploy**

After this, every `git push` will automatically update your live site.

### Step 3 — Connect your Namecheap domain

**In Netlify:**
1. Go to your site → **"Domain management" → "Add a domain"**
2. Type `builtbydana.com` and confirm
3. Netlify will give you **2 nameservers** (looks like `dns1.p01.nsone.net` and `dns2.p01.nsone.net`)

**In Namecheap:**
1. Log in to Namecheap → go to your domain list → click **"Manage"** on `builtbydana.com`
2. Find **"Nameservers"** and change from "Namecheap BasicDNS" to **"Custom DNS"**
3. Paste in the Netlify nameservers and save

DNS propagation takes **a few minutes to a few hours** (usually under 30 min).

### Step 4 — Enable HTTPS (free)
Once DNS is live, go back to Netlify → Domain management → click **"Verify DNS configuration"**, then **"Provision SSL certificate"**. Done — your site is live on HTTPS.

---

## Alternative hosting options

| Option | Notes |
|--------|-------|
| **Vercel** | Same drag-and-drop flow as Netlify, also free |
| **Cloudflare Pages** | Free, very fast global CDN |
| **GitHub Pages** | Free if repo is public; slightly more steps |
| **Namecheap hosting** | If you already have Namecheap hosting, just upload via cPanel File Manager |

---

## Making updates later

Just edit `index.html`, `style.css`, or `script.js` and:
- **If using drag & drop:** Re-drag the folder into Netlify's "Deploys" tab
- **If using GitHub:** `git add . && git commit -m "update" && git push` — auto-deploys

---

## Adding a photo

1. Put your photo file (e.g. `dana.jpg`) in the `builtbydana/` folder
2. In `index.html`, find the `about__photo-placeholder` div and replace it with:
   ```html
   <img src="dana.jpg" alt="Dana" style="width:100%;height:100%;object-fit:cover;border-radius:20px;display:block;">
   ```

---

Good luck — go get those clients! ✦
