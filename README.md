# Shadaj Graam Foundation – Website

A fast, one-page website. No database, no monthly fees.

## Preview before uploading
Unzip and double-click `index.html` – it opens in your browser with all animations.

## What's inside
- `index.html` – the whole website (text, design and layout)
- `assets/` – logo, emblem, 8th Nerve poster, concert photos

## Put it online for FREE (GitHub Pages, about 10 minutes)
1. Create a free account at https://github.com
2. Click **New repository** → name it `shadajgraam` → Public → Create.
3. Click **uploading an existing file**, drag in `index.html` and the whole `assets` folder → **Commit changes**.
4. Go to **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / `(root)` → **Save**.
5. In 1–2 minutes the site is live at `https://<your-username>.github.io/shadajgraam/`

(Alternative: https://pages.cloudflare.com or https://app.netlify.com/drop – just drag the folder in.)

## Connect your GoDaddy domain
**Step A – tell GitHub your domain**
1. GitHub → your `shadajgraam` repository → **Settings → Pages**.
2. Under **Custom domain** type your domain (for example `shadajgraam.org`) → **Save**.

**Step B – point GoDaddy to GitHub**
1. Log in to GoDaddy → **My Products** → next to your domain click **DNS** (or *Manage DNS*).
2. **Delete** the existing `A` record for `@` that says **Parked** (and any *Forwarding* set on the domain).
3. Click **Add New Record** four times and add these `A` records (Name = `@`, TTL = default):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
4. Find the `CNAME` record with Name `www` → **Edit** → Value = `<your-github-username>.github.io` → Save.
   (If there is no `www` CNAME, add one.)

**Step C – switch on https**
1. Wait 15 minutes to a few hours for DNS to update.
2. Back in GitHub → **Settings → Pages** → tick **Enforce HTTPS** (it becomes clickable once DNS is ready).
3. Open `https://yourdomain` and `https://www.yourdomain` – both should show the site.

Tip: in GoDaddy you can also create a free email forward like `info@yourdomain` → `shadajgraam@gmail.com` (under *Email Forwarding*, if your plan includes it).

## How to update the site later
- **Change text:** open `index.html` on GitHub → pencil icon → edit → Commit. Live in about a minute.
- **Committee:** photos are in `assets/team/` (manohar.jpg, vipul.jpg, priyanka.jpg, omkar.jpg, chaitra.jpg,
  soham.jpg, pranay.jpg). To change one, replace the file with a square photo (about 600×600 JPG) using the
  same name. To add a member, copy one `<div class="member …">…</div>` block in the *COMMITTEE* section.
- **Countdown:** the live countdown in the Upcoming section points to 28 Dec 2026, 8:00 PM. For the next
  concert, change the date in the line `new Date('2026-12-28T20:00:00+05:30')` near the bottom of `index.html`.
- **Concert photos:** each concert's photos are in `assets/gallery/` named `c1-1.jpg`, `c1-2.jpg` … (c1 = concert 1). The first photo is the cover; the card cycles through all photos and opens a full-screen viewer on tap.
- **Share preview image:** `assets/og-image.jpg` is what WhatsApp/Facebook show when the link is shared.
- **New concert:** copy one `<article class="concert">…</article>` block in the *Our Journey* section,
  change the photo, name, date and place, and upload the new photo into `assets/concerts/`.
- **New upcoming concert:** edit the *Upcoming* section (poster file, title, date, venue, ticket link).
- Keep photos under ~200 KB each (resize to ~900–1000 px wide) so the site stays fast.
