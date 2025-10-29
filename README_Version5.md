```markdown
# akramcell.com — Link page

This repository contains a single-file customizable link page for Akramcell.

How to customize
1. Open `index.html`.
2. Edit the top JS CONFIG block:
   - `shopTitle` — the display name for your shop.
   - `handle` — optional small handle.
   - `avatarSrc` — URL to your logo (or leave empty to show initials).
   - `accentColor` — brand color hex.
   - `links` — an array of link objects: `{ title, url, desc }`.
3. Save and push.

Quick publish (web UI)
1. Go to https://github.com/new and create a new repository named `akramcell.com` (Public).
   - Description (optional): Link page for Akramcell
   - Leave "Initialize this repository with a README" unchecked.
2. After the repo is created click Add file → Upload files and upload:
   - index.html
   - README.md
   - CNAME
   Commit directly to the main branch.

Enable GitHub Pages
- Go to Settings → Pages
- Under Source choose Branch: main and folder: / (root), then Save.
- In the "Custom domain" box enter `akramcell.com` (or upload the CNAME file which already contains it).

DNS (set at your domain registrar)
- For the root/apex domain akramcell.com add these A records (Host @):
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- Optionally add a CNAME for www:
  - host: www → value: akramcell-hub.github.io
- If your DNS provider supports a proxy (e.g., Cloudflare), set the records to DNS-only (no proxy) until GitHub verifies and issues HTTPS.

Quick local git commands (alternative)
```bash
git init
git checkout -b main
git add index.html README.md CNAME
git commit -m "Initial link page for akramcell.com"
git remote add origin https://github.com/akramcell-hub/akramcell.com.git
git push -u origin main
```

Notes
- GitHub will provision HTTPS automatically once DNS is correct (may take a few minutes to an hour).
- If you want me to edit the page with your real social links & logo before you upload, paste your links in this chat and I'll update the files.
```