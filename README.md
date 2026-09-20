CHIP AI LABS — redesigned premium single-page site.

Content from the previous version is preserved. Contact and Careers are merged into one Connect & Careers section. The original logo remains the same and is also used as the favicon.


## Cloudflare caching recommendation

For GitHub Pages behind Cloudflare:
- Browser Cache TTL: **Respect Existing Headers**
- Do not use a site-wide **Cache Everything** rule.
- HTML: allow revalidation.
- CSS/JS: use the version query string added to local assets (currently `?v=20260920`).
- Images/fonts: normal caching is recommended.

When CSS/JS changes, increment the asset version (for example `?v=20260921`) so browsers fetch the new files immediately. Cloudflare cache purges cannot clear visitors’ browser caches.
