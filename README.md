# Up Studios Website

Portfolio and booking site for Up Studios — GTA real estate photography & videography.

## Local Development

```bash
node serve.mjs
```

Opens at `http://localhost:3000`

## Project Structure

```
index.html          — entire site (single file, all styles inline)
serve.mjs           — local dev server
assets/             — images used by the site
brand_assets/       — logos, headshot, pricing PDF
```

## Deployment

The site is a single static HTML file with no build step required.

### Netlify (recommended)
1. Push this repo to GitHub
2. Connect repo at [app.netlify.com](https://app.netlify.com)
3. Build command: *(leave blank)*
4. Publish directory: `.` (root)
5. Set custom domain in Netlify → Domains

### Vercel
1. Push this repo to GitHub
2. Import at [vercel.com](https://vercel.com)
3. Framework preset: **Other**
4. Root directory: `.`
5. Set custom domain in Vercel → Domains

### GitHub Pages
1. Push to GitHub
2. Settings → Pages → Branch: `main` → Folder: `/ (root)`
3. Point GoDaddy domain to GitHub Pages (see below)

## Custom Domain (GoDaddy)

### Option A — Netlify (easiest)
1. In Netlify: **Domain settings → Add custom domain** → enter your domain
2. Netlify shows you two nameserver addresses (e.g. `dns1.p01.nsone.net`)
3. In GoDaddy: **DNS → Nameservers → Enter my own nameservers** → paste Netlify's nameservers
4. Wait up to 48h for propagation (usually under 1h)

### Option B — GitHub Pages
1. In GoDaddy DNS, add these **A records** pointing to GitHub Pages IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
2. Add a **CNAME record**: `www` → `your-github-username.github.io`
3. In GitHub repo: **Settings → Pages → Custom domain** → enter your domain
4. Check "Enforce HTTPS" once DNS propagates
