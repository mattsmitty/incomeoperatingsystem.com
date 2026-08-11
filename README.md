# Income Operating System™ — Website V1

Single-page static site for **incomeoperatingsystem.com**. No build step, no dependencies — one `index.html` file.

## Deploy: GitHub Pages + GoDaddy

### 1. Push to GitHub
```bash
git init
git add index.html CNAME README.md
git commit -m "Income Operating System V1"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/incomeoperatingsystem.com.git
git push -u origin main
```

### 2. Enable GitHub Pages
Repo → **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / root → Save.
The `CNAME` file in this repo tells GitHub Pages the custom domain.

### 3. Point GoDaddy DNS at GitHub Pages
In GoDaddy → your domain → **DNS Management**:

| Type  | Name | Value               |
|-------|------|---------------------|
| A     | @    | 185.199.108.153     |
| A     | @    | 185.199.109.153     |
| A     | @    | 185.199.110.153     |
| A     | @    | 185.199.111.153     |
| CNAME | www  | YOUR_USERNAME.github.io |

Delete any existing "Parked" A record. DNS can take up to an hour to propagate.

### 4. HTTPS
Back in GitHub → Settings → Pages, once the domain check passes, tick **Enforce HTTPS**.

## Content swap list (before/after launch)
- **Book cover**: currently an SVG placeholder in `index.html` (`<svg class="book-cover">`). Replace with the real cover image.
- **Buy link**: the "Get Predictable Income" button href is `#` — point at Amazon/retailer.
- **Matt's photo**: the About section has a photo placeholder — swap in a real professional photo.
- **Email capture**: the form is front-end only. Wire the form action to ConvertKit/Beehiiv/Mailchimp when the list is set up.
- **Field Notes & Tools cards** link to `#` — point at real pages as they ship.
