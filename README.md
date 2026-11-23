# Flash Poll landing page

Static, dependency-free landing page for GitHub Pages.

## Before publishing
Replace `yourdomain.com` with your real domain in: `index.html` (canonical, og:url, JSON-LD), `robots.txt`, `sitemap.xml`, `CNAME`, `.well-known/security.txt`.
(Example: `grep -rl yourdomain.com . | xargs sed -i 's/yourdomain.com/example.co.uk/g'`)

## Deploy on GitHub Pages
1. Create a repository and push all files to the root of the `main` branch.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.
3. Settings → Pages → Custom domain: enter your domain, then tick **Enforce HTTPS** once available.

## DNS (at your domain registrar)
- Apex domain: four `A` records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` (optionally the matching `AAAA` records).
- `www`: a `CNAME` record → `<your-username>.github.io`.
- Check GitHub's current docs for any IP changes.

## After going live
Add and verify the site in Google Search Console and Bing Webmaster Tools, then submit `sitemap.xml`.
