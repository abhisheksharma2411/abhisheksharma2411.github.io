# abhisharma.co.in

Personal website for Abhishek Sharma — Staff Software Engineer.
Single static HTML file. Hosted on GitHub Pages.

## What's in this folder

- `index.html` — the site (self-contained, no build step, no dependencies)
- `CNAME` — tells GitHub Pages this repo serves `abhisharma.co.in`
- `.nojekyll` — skips Jekyll processing so files are served exactly as written
- `README.md` — this file

The site uses three Google Fonts (Geist, Geist Mono, Instrument Serif) loaded
at runtime; no font files to host yourself.

## Before publishing — two small TODOs in `index.html`

The site has two link placeholders to replace once those destinations exist:

1. **Medium article URL.** Search for `data-replace="medium-url"` in `index.html`
   and replace its `href="#"` with the live Medium URL once *Design for Failure*
   is published.

2. **AffiliateForge repo URL.** Search for `data-replace="affiliateforge-url"`
   and replace its `href="#"` with the GitHub repo URL once the AffiliateForge
   repo is live.

Both links still render correctly while the placeholders are in place; they
just navigate to `#` (top of page) until updated.

## How to publish (first time, ~15 minutes total)

### 1. Create a GitHub repo

- Go to github.com → **New repository**
- Name: `abhisharma.co.in` (matches the domain — recommended)
- **Public** visibility
- Don't add a README from GitHub — we already have one in this folder

### 2. Upload the files

- On the empty repo's page, click **"uploading an existing file"**
- Drag all four files into the upload area:
  - `index.html`
  - `CNAME`
  - `.nojekyll`
  - `README.md`
- Commit directly to the `main` branch

### 3. Enable Pages

- In the repo, go to **Settings → Pages**
- **Source:** Deploy from a branch
- **Branch:** `main` / `(root)`
- Save

The site will be live at `https://<your-username>.github.io/abhisharma.co.in/`
within about a minute.

### 4. Point your domain (DNS at your registrar)

At whoever manages DNS for `abhisharma.co.in` (BigRock, GoDaddy, etc.), add these
records:

**Apex domain (`abhisharma.co.in`) — four A records:**

```
A   @   185.199.108.153
A   @   185.199.109.153
A   @   185.199.110.153
A   @   185.199.111.153
```

**`www` subdomain — one CNAME record:**

```
CNAME   www   <your-github-username>.github.io
```

DNS propagation usually completes in 10 minutes to a few hours.

### 5. Turn on HTTPS

Once DNS resolves, go back to **Settings → Pages** in your repo and check
**"Enforce HTTPS"**. GitHub will auto-issue a free Let's Encrypt certificate
within a few minutes.

You're live.

## How to update the site (after first publish)

Edit `index.html` locally or directly in GitHub's web editor. Commit. Push.
GitHub Pages redeploys in ~30 seconds. No build step.

## What's on the site

Five sections, in order:

1. **Hero** — name + positioning statement + CTAs
2. **Stats strip** — 15 years / 500M+ DAU / 20K TPM / 14M SKU
3. **§ 01 Writing** — featured *Design for Failure* essay + pipeline indicator
4. **§ 02 Open Source** — AffiliateForge project card
5. **§ 03 Experience** — QXO (featured), TikTok, Costco, Wayfair, Nagarro/ADSS
6. **§ 04 Community & Service** — IEEE, judging, mentorship
7. **§ 05 Contact** — gradient CTA block with email + LinkedIn

The commit history on this repo will accumulate as you update the site
over time — that history is itself useful EB1A evidence of consistent
activity on your professional presence.
