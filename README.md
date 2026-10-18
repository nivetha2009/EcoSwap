# EcoSwap

Don’t Waste It. Reimagine It. A static website (HTML, CSS, JavaScript). No build step, no dependencies, no API keys.

## Files
- `index.html`, `styles.css`, `app.js`: the website
- `_headers`: security headers for Netlify and Cloudflare Pages
- `vercel.json`: the same headers for Vercel
- `robots.txt`, `.gitignore`

## Try it locally
Double-click `index.html`, or run `python3 -m http.server 8000` and open http://localhost:8000.

## Publish (pick one, all free)

### Option A: GitHub Pages
1. Create a new public repository on github.com (for example `ecoswap`).
2. Click **Add file → Upload files**, drag in every file from this folder, then **Commit changes**.
3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/ecoswap/`.
Note: GitHub Pages ignores `_headers`, but `index.html` already contains a Content-Security-Policy meta tag.

### Option B: Netlify (easiest)
1. Sign in at app.netlify.com.
2. Open **Add new site → Deploy manually** and drag this whole folder onto the page.
3. Your site is live at a `*.netlify.app` address. Rename it under **Site configuration**.

### Option C: Vercel
1. Put the files in a GitHub repository.
2. At vercel.com choose **Add New → Project**, import the repository, leave the settings as they are, and click **Deploy**.

## Custom domain
Buy a domain, then add it in your host’s settings (Pages: **Custom domain**; Netlify: **Domain management**; Vercel: **Domains**) and copy the DNS records it shows into your registrar.

## What is real and what is a demo
- Recommendations are rule-based (see the `C`, `SC` and `recs` parts of `app.js`). They are not AI.
- Photos never leave the visitor’s device.
- Journey data and demo listings are stored in each visitor’s browser and are not shared or synced.
- Community listings are samples. There are no accounts, payments or messaging.

## Before calling it a real product
- Add a short privacy notice (what is stored, and where).
- Add a real backend (accounts, moderation, database, rate limiting) before any live marketplace.
- Add AI photo recognition only through your own server endpoint (see the `recognise` hook in `app.js`). Never put API keys in these files.
- Add region-specific recycling rules, since acceptance differs by area.
- Test with a screen reader and on several phones.
