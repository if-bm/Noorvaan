
# Noorvaan — Static Site Starter (no monthly fees)

A premium, fast static site you can host for free on GitHub Pages or Cloudflare Pages.
Buttons use **Stripe Payment Links** so you only pay processing fees when you sell.

## What's inside
- Plain HTML/CSS/JS (no frameworks)
- Pages: Home, Shop, Story, Care, Contact
- `data/products.json` — add/edit products + Stripe links
- SEO basics + `robots.txt` + `sitemap.xml`
- Accessible, responsive, black-and-gold design

## Edit products
Open `data/products.json` and replace each `stripe_link` with your real Payment Link from Stripe.

## Stripe — create Payment Links
1. Create a Stripe account (no monthly fee).
2. Products → Add product (name, price).
3. Click **Create payment link**; enable shipping address collection + flat shipping (or Shipping rates).
4. Copy the link and paste into `data/products.json` → `stripe_link`.

## Deploy (GitHub Pages, free)
1. Create a new GitHub repo → upload this folder.
2. Settings → Pages → Deploy from branch: `main` / root (`/`).
3. Your site will appear at `https://USERNAME.github.io/REPO`.
4. Optional: add a custom domain in Pages and set A/ALIAS records at your DNS.

## Deploy (Cloudflare Pages, free)
1. In Cloudflare → Pages → **Create project** → Connect to your repo.
2. Build settings: Framework = **None**, Build command = (leave blank), Output directory = `/`.
3. Deploy. Add your custom domain and update DNS to point to Cloudflare.

## Custom domain + email (free routing)
- Registrar: Cloudflare Registrar or Namecheap.
- DNS: Add `A`/`CNAME` to your host (GitHub Pages docs or Cloudflare instructions).
- Email: Cloudflare Email Routing can forward `hello@yourdomain` to your Gmail for free.

## Analytics (free)
- Cloudflare Web Analytics: add the script tag from your Cloudflare dashboard to `index.html` before `</body>`.

## Contact form (free)
- Formspree: replace `YOUR_FORM_ID` in `contact.html` with your form ID (free tier available).
- Or embed a Google Form.

## Notes
- For taxes, Stripe can calculate US sales tax if you enable Stripe Tax (fees apply) or you can bake tax into the price and keep it simple at launch.
- Inventory is manual with Payment Links (toggle availability in Stripe or edit the site).

— Generated 2025-09-02


## Deployment — Step-by-step

### Option A) GitHub Pages (Actions workflow)

1. Create a **new GitHub repo** (public or private).
2. Push all files (including `.github/workflows/deploy.yml`) to the **main** branch.
3. In the repo: **Settings → Pages → Build and deployment → Source = GitHub Actions**.
4. Push a commit (or go to **Actions** and run **Deploy static site to GitHub Pages**).
5. Your site URL will appear in the workflow output and in **Settings → Pages**.
6. (Optional) **Custom domain:** Add `noorvaan.com` under **Settings → Pages** and create the suggested DNS records.

### Option B) Cloudflare Pages

1. In Cloudflare → **Pages → Create project → Connect to Git** (select your repo).
2. Framework preset: **None**; Build command: *(leave empty)*; Output: `/`.
3. Deploy. You’ll get `<project>.pages.dev`.
4. Add your custom domain: **Pages → Custom domains → Set up a domain** and follow the DNS prompt.
5. (Optional) Enable **Web Analytics** and paste the token in `index.html` (see comment).

### After go-live
- Replace `https://example.com` in `sitemap.xml`, `robots.txt`, and the JSON-LD in `index.html` with your domain.
- Submit `sitemap.xml` in **Google Search Console**.
- Swap placeholder SVGs for real photos (WebP/JPEG ≤ 400 KB).

— Updated 2025-09-02
