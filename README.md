# Author Website (Vite + React + Tailwind)

## Local dev
```bash
npm install
cp .env.example .env   # you can leave it empty pre-launch
npm run dev
```

## Deploy to Vercel (recommended)
1. Create a Vercel account and click **New Project** → **Import** your repo/folder.
2. Framework preset: **Vite** (auto-detected). Build: `npm run build`. Output: `dist/`.
3. (Optional pre-launch) You can deploy without env vars; the site will use **mailto** fallbacks.
4. When ready, add in **Settings → Environment Variables**:
   - `VITE_FORMSPREE_ID` = your Formspree form ID
   - `VITE_NEWSLETTER_POST_URL` = your Mailchimp POST URL
5. Deploy. Then in **Domains**, add `thefirstfamilyae.org`.
   - **A** `@` → `76.76.21.21` (Vercel apex IP)
   - **CNAME** `www` → `cname.vercel-dns.com`

## Netlify (alternative)
- Build `npm run build` • Publish `dist/`
- Add the same env vars when you’re ready to enable forms.

## Press Kit
- Files live in `src/press/` and a bundled ZIP at `src/press/press-kit.zip`.

## Delayed Forms (pre-launch defaults)
- **Contact:** shows an **Email Us** button (mailto:info@thefirstfamilyae.org) until Formspree is configured.
- **Newsletter:** shows **Email Me Updates** until Mailchimp is configured.
- To enable forms later, fill `.env` or host env vars and redeploy.
