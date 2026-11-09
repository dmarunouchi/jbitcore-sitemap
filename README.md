# jbitcore-sitemap

Sitemap for www.jbitcore.com, served by a Cloudflare Worker (static assets) at https://sitemap.jbitcore.com/sitemap.xml
(Google Sites does not publish its own sitemap.)

## Rules
- List only published pages that appear in the site menu. Hidden pages (drafts) and old URLs that return 404 stay out.
- New post published: add one `<url>` line to `public/sitemap.xml` and commit. Cloudflare redeploys on its own.
- Page paths with accents are percent-encoded (é becomes %C3%A9), exactly as the browser shows them when copied.
- Never change or remove a line for a page that still exists: page URLs on the site do not change.

## Rollback
Remove the sitemap in Google Search Console (Sitemaps), then delete the jbitcore-sitemap Worker in Cloudflare (this also removes sitemap.jbitcore.com). The site itself is not affected.
