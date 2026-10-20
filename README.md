# Sopanix website update

Modern responsive blue/white design for Sopanix with the tagline “A New Vision. A New Journey.”

## Included
- Responsive homepage and separate About and Contact pages
- Founder/team cards from `content/site.json`
- SEO titles, descriptions, canonical links and basic Organization schema
- Mobile navigation and sample SVG logo
- `/admin/` content helper to download edited JSON

## Important about Admin/CMS
The admin page is a starter helper, **not** a secure hosted CMS. It does not publish changes directly. Edit content, download `site.json`, then replace `content/site.json` in GitHub and commit. Direct uploads/login-based editing require a separately configured CMS/authentication service. No hard-coded password is used.

## Before launch
1. Replace sample team names, email, and phone in `content/site.json`.
2. Add real images under `assets/uploads/`; use their paths in the JSON. Replace `assets/uploads/logo.svg` with your own logo.
3. Upload all files/folders inside this ZIP to the root of `https://github.com/Sopanix2026/Sopanix`, replacing existing `index.html` and `styles.css`. Keep folder structure.
4. Commit to `main`; Netlify should deploy automatically if connected. Then check `https://sopanix.com`.

On mobile GitHub, folder uploads can be awkward. If it does not allow all folders, use GitHub's web editor per file or a computer. Do not delete repository or DNS settings.
