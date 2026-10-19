# Sopanix — free starter website

A responsive bilingual (English/Bengali) blue-and-white Coming Soon website with five founding-team profiles.

## What's included
- `index.html`, `styles.css`, `script.js`: public website
- `content/team.json`: five founder profiles and English/Bengali text
- `admin/`: Decap CMS configuration and admin screen
- `assets/uploads/`: uploaded team photos will be stored here
- `netlify.toml`: static Netlify publish settings

## Important CMS hosting note
This starter uses Decap CMS with Netlify Identity + Git Gateway because it is a common no-cost path for a small static site. However, Netlify currently marks Git Gateway as **deprecated** and does not recommend new configurations. It may continue to work, but don't treat it as a guaranteed long-term CMS service. The public site itself is static and can be hosted on other providers. If Git Gateway is unavailable for your account, use the fallback below or switch to a maintained GitHub OAuth backend.

## Publish free (Netlify + GitHub)
1. Download and unzip this folder.
2. Sign in to GitHub and create a new repository, e.g. `sopanix-website`.
3. Upload all files and folders from this package to the repository root. Keep the folder names exactly as supplied. The repository branch should be `main`.
4. Sign in to Netlify and choose **Add new site → Import an existing project**. Connect GitHub and select `sopanix-website`.
5. Deploy as a static site. Build command: leave blank. Publish directory: `.`.
6. Open the deployed site once and check the home page.
7. In Netlify, open the site's Identity/Authentication settings. If Identity is available, enable it and set registration to **Invite only**. Invite only your own email address.
8. Under Identity → Services, enable Git Gateway if the option is available for the site.
9. In the repository, open `admin/config.yml` and replace both occurrences of `https://YOUR-NETLIFY-SITE.netlify.app` with your real Netlify site URL. Commit the change.
10. In Netlify, accept the invite email and set your password. Then open `https://YOUR-NETLIFY-SITE.netlify.app/admin/` on your phone and sign in.
11. In the CMS, open **Founding Team → Five Founders**. Change names/roles/bios, upload photos, and click **Publish**. Netlify redeploys the site after the repository is updated.

### If Git Gateway / Identity is unavailable
You can still publish the public site free. On a phone, open the GitHub repository, edit `content/team.json`, and commit the change. For photos, upload the image into `assets/uploads/` first, then set that member's `"image"` to a path like `"/assets/uploads/rez...jpg"`. This fallback is less convenient than a CMS but does not require a paid hosting plan.

## Connect Sopanix.com later
1. In Netlify site settings, add `sopanix.com` and `www.sopanix.com` as custom domains.
2. At the company where you purchased the domain, open DNS settings.
3. Enter exactly the DNS records Netlify displays for your site. Do not guess or copy records from another site.
4. Wait for DNS propagation and enable HTTPS in Netlify.
5. Once HTTPS works, update `site_url` and `display_url` in `admin/config.yml` to your final domain and commit.

Your domain registration remains separate and may need renewal fees even if hosting is free.

## Edit team profiles on mobile
Preferred (if CMS is enabled):
1. Visit `your-site.netlify.app/admin/`.
2. Sign in with the invited admin email.
3. Open Founding Team → Five Founders.
4. Edit English/Bengali name, role, bio or photo.
5. Press Publish and wait for deployment.

Fallback (without CMS):
1. Open your GitHub repository in Chrome.
2. Edit `content/team.json` using the pencil icon.
3. Change the relevant text and commit. Keep valid JSON syntax.
4. To add a photo, upload it to `assets/uploads/`, then paste its path into the matching `"image"` field.

## Before going live
- Check spellings and Bengali names.
- Upload one portrait photo per founder (square or 4:5 crop works well).
- Keep CMS registration invite-only.
- Never publish passwords, private phone numbers, or confidential company details in the public JSON.
- This starter is a static company profile, not an online store. WooCommerce or another ecommerce system can be added later.
