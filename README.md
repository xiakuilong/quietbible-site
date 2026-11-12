# Quiet Bible — product site

A static marketing page for Quiet Bible Reader. No build step, no dependencies.

## Deploy

Upload this directory to any static host (Cloudflare Pages, Netlify, GitHub Pages, S3 + CDN, or the same host as the web app).

Before publishing:

1. Replace `href="../"` on the “Open web app” buttons with the real web app URL (or keep the app at the domain root and serve this page at `/site/`).
2. Replace the App Store call-to-action when the app is live. There is currently no App Store link on the page; add one to the hero and CTA when Apple approves the listing.
3. Host `privacy.html` and `terms.html` at stable public URLs and use those URLs in App Store Connect.
4. Fill in the publisher legal name, registered address and contact email in `privacy.html` and `terms.html` (they still contain the template placeholder note).
5. Confirm the AYT wording with the final licensing position. The page currently says AYT is for personal, non-commercial reading and that commercial distribution requires YLSA permission.

## Assets

`assets/*.webp` are resized from `docs/screenshots/ios-*.png`. Regenerate the source screenshots with:

```bash
node scripts/capture-screens.cjs
```

Requires Playwright with Chromium installed and the app running at `http://127.0.0.1:4173` (`npm run preview`).
