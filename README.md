
# BSCRE @ OSU — Static Site (GitHub Pages)

This is a lightweight static site for **Black Students in Commercial Real Estate @ Ohio State**.

## Pages
- `index.html` — Home
- `team.html` — Team grid
- `internships.html` — Internship board (embed AwesomeTable)
- `join.html` — Join / Interest form

## Quick Start (Local Preview)
Just open `index.html` in a browser. (For best results, use a local server like VS Code Live Server.)

## Deploy to GitHub Pages (Free)
1. Create a GitHub account at https://github.com/
2. Make a **public** repository (e.g., `bscreosu-site`).
3. Upload all files from this folder to the repo (drag & drop in the GitHub web UI).
4. In the repo: **Settings → Pages**.
   - Source: `Deploy from a branch`
   - Branch: `main` (or `master`) → `/ (root)` → Save
5. Wait ~1 minute. Your site will appear at:
   - `https://<your-username>.github.io/bscreosu-site/`

## Connect Custom Domain (bscreosu.com)
1. In the repo **Settings → Pages**, find **Custom domain**. Enter `bscreosu.com` and click **Save**. This creates a `CNAME` file.
2. In your domain registrar (where you bought bscreosu.com), set DNS:
   - For **apex domain** (`bscreosu.com`): Add four **A records** pointing to GitHub Pages:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - For **www subdomain** (`www.bscreosu.com`): Add a **CNAME** to `<your-username>.github.io`
3. Back in GitHub **Settings → Pages**, check **Enforce HTTPS** once the certificate is ready.

> Tip: If you prefer using only `www.bscreosu.com`, you can omit apex A records and just set the CNAME for `www`, then enable a redirect from apex to `www` in your DNS or GitHub Pages.

## AwesomeTable Embed (Internship Board)
1. Build your internship sheet in Google Sheets.
2. Create a new view at https://awesome-table.com/ (connect your sheet).
3. Configure filters for **Location, GPA, Class Year, Paid/Unpaid**.
4. Copy the **Embed > iframe** URL.
5. Replace the placeholder iframe `src` in `internships.html`.

## Customization
- Replace images in `assets/img/` (keep filenames or update paths).
- Edit colors in `assets/css/style.css` (`#bb0000` ≈ scarlet).
- Duplicate a `.card` in `team.html` for each member.
- Update `join.html` button link to your real Google Form.

## Notes
- This is a static site; no backend/server required.
- You can later migrate to a different builder and keep the same domain.
