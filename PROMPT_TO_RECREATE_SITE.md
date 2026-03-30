# Prompt Used to Recreate This Site

Use this prompt with an AI coding agent when you want a one-for-one local mirror of an existing website.

## Copy/Paste Prompt

```text
Recreate this website one-for-one locally so it can later be hosted as static files:
<TARGET_WEBSITE_URL>

Requirements:
1) Direct copy approach
- Do not redesign or reinterpret.
- Mirror the real site structure and content as-is.

2) Full sitemap coverage
- Discover and list the sitemap/routes (from robots/sitemap and crawl).
- Ensure each route is saved locally and works when opened directly.

3) Match styles and behavior
- Capture all stylesheets, scripts, fonts, images, icons, and required static assets.
- Rewrite links so local files resolve correctly in a local static server.
- Keep external-only services external where required (for example video embeds), but document them clearly.

4) Verify responsiveness
- Check at minimum desktop and mobile breakpoints.
- Validate key routes visually (homepage, about, and major project pages).
- Confirm no major layout regressions.

5) Check your work with evidence
- Produce a local route list (sitemap file).
- Provide a mirror report with:
  - pages captured
  - files downloaded
  - known external dependencies
  - visual comparison results (local vs live)
- Include commands to run locally.

6) Output format
- Create clear markdown docs:
  - README with run commands
  - Mirror report
  - Local run walkthrough
- Keep all generated artifacts in the repository.

7) Safety constraints
- Do not deploy anything.
- Do not change DNS.
- Do not run destructive cleanup commands unless explicitly requested.

Definition of done:
- The mirrored site runs locally from a static server.
- All sitemap routes resolve locally.
- Styling/assets are matched to live as closely as possible.
- Verification artifacts and documentation are committed.
```

## Notes

- This prompt is intentionally strict about fidelity and verification.
- It is optimized for static mirroring and handoff to hosting platforms like Cloudflare Pages.
