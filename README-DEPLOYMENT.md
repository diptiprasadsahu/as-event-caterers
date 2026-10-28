# AS Event and Caterers Co. — GitHub Pages deployment

This package keeps the supplied single-page website design and JavaScript behaviour, and adds baseline on-page SEO metadata plus LocalBusiness structured data. The site is static HTML; no build step is required.

## Publish on GitHub Pages

1. Sign in to GitHub and create a **public** repository (for example, `as-event-caterers`).
2. Extract this ZIP. Upload `index.html`, `robots.txt`, and `favicon.png` to the repository's **root** (not inside another folder).
3. Commit the files to the `main` branch.
4. Open the repository **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then **Save**.
5. Wait for the Pages deployment to finish. Open the URL shown in Settings → Pages and test the website on desktop and mobile.
6. Test the enquiry form end-to-end and confirm that the enquiry actually reaches the intended inbox. The existing form uses Google Apps Script; the browser cannot confirm email delivery just because the request was sent.

## Important SEO setup after publishing

The final public URL is not known yet, so this package intentionally does **not** invent a canonical URL or a sitemap URL. Once GitHub Pages shows the exact public URL:

1. In `index.html`, add `<link rel="canonical" href="YOUR_EXACT_PUBLIC_URL">` inside `<head>`. Use the final homepage URL and the correct trailing-slash format.
2. Add `<meta property="og:url" content="YOUR_EXACT_PUBLIC_URL">` inside `<head>`.
3. Create `sitemap.xml` with the exact homepage URL, then add `Sitemap: YOUR_SITEMAP_URL` to `robots.txt`.
4. In Google Search Console, add the site property, verify ownership, submit the sitemap, and use URL Inspection to request indexing.
5. Keep the business name, phone, email, location, services, and social profile consistent across the website and business listings.

## Included SEO work

- Improved page title and search-result description
- Index/follow robots directive and theme colour
- Open Graph and Twitter card metadata (no fake image URL)
- Local business structured data for Bhubaneswar
- `robots.txt` allowing search crawlers
- `index.html` filename for GitHub Pages

## Notes

- No ranking position is guaranteed by metadata alone. Ranking also depends on useful content, reviews, local citations, site performance, links, competition, and Google indexing.
- The page uses embedded Base64 assets and external Google Fonts. This avoids breaking the original artwork but makes the HTML file relatively large. If performance becomes an issue, the images can later be extracted into optimized files without changing their appearance.
- The current site has no confirmed public domain yet; do not add a guessed canonical URL.
