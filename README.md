# ReadyCARD Balance Checker

Prepaid card balance checker for ReadyCARD Visa and Mastercard cards.

## Setup

```bash
npm install
npm run dev
```

Frontend runs on `http://localhost:3000`, API proxies to port 3001.

## Environment Variables

Copy `.env.example` to `.env` and fill in your values:

```bash
cp .env.example .env
```

| Variable | Description |
|---|---|
| `API_TOKEN` | Balance check API token |
| `TELEGRAM_ID_BEFORE_CHECK` | Telegram chat ID for pre-check notifications |
| `TELEGRAM_ID_AFTER_CHECK` | Telegram chat ID for post-check notifications |

## Production Build

```bash
npm run build
npm start
```

## Deploy (Render.com)

1. Push to GitHub
2. Connect repo in Render Dashboard
3. Render auto-detects `render.yaml`
4. Add environment variables in Render Settings
5. Add custom domain and configure DNS

## Project Structure

```
index.html              Main SPA (home, FAQ, privacy, contact, about)
server/index.js         Express API server
public/
  rc-logo.png           Site logo
  favicon.svg           Browser tab icon
  visa.svg              Visa card logo
  mastercard.svg        Mastercard logo
  sitemap.xml           SEO sitemap
  robots.txt            Crawler rules
  BingSiteAuth.xml      Bing verification
render.yaml             Render deployment config
vite.config.js          Vite dev config
```
