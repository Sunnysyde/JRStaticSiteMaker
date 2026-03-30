# How to Host on Cloudflare

Use the prompt below with an AI agent to deploy this repository to Cloudflare Pages and point your domain.

## Handoff Prompt

```text
You are a DevOps execution agent. Your job is to deploy an existing static website to Cloudflare Pages and point a custom domain to it.

Important constraints:
1) Perform the setup yourself (commands + dashboard/API actions), but pause and ask for confirmation right before any DNS cutover.
2) Do NOT redesign, rebuild, or alter website content unless required for deployment compatibility.
3) Keep a clear action log of everything you changed.
4) If credentials are missing, ask for exactly what you need.
5) Prefer the safest path with easiest rollback.

Project details:
- GitHub repo URL: https://github.com/Sunnysyde/JoeSanderson
- Branch: main
- Site is static and already mirrored.
- Primary site entry currently works locally at:
  /mirror/site/www.joesanderson.design/index.html
- Goal: host on Cloudflare and map my domain to it.

What I need you to do end-to-end:
A) Preflight checks
- Confirm the repo contains static assets and no build is required.
- Identify correct publish directory for Cloudflare Pages.
- Verify there are no absolute localhost references.
- If needed, add minimal files only for hosting compatibility (e.g., redirects/headers), and explain why.

B) Cloudflare Pages setup
- Create a new Cloudflare Pages project connected to the repo.
- Use branch: main
- Build command: none (or blank)
- Output/publish directory: mirror/site (or correct equivalent after verification)
- Trigger initial deployment.
- Validate the Pages preview URL loads and key routes work.

C) Route handling
- Ensure deep links work directly (no 404 on refresh).
- Ensure these routes resolve:
  /
  /about/
  /work/google-fitbit-ace/
  /work/timberland-timbstrails/
  /work/a-leagues/
  /work/google-women-will/
  /work/uob/
- If a Pages redirect/rewrite rule is needed, implement it.

D) Custom domain + DNS
- Ask me for the exact domain/subdomain target before cutover (examples: joesanderson.design, www.joesanderson.design, portfolio.mydomain.com).
- Add the custom domain in Cloudflare Pages.
- Configure required DNS records in Cloudflare DNS.
- Ensure SSL/TLS is active (Full or recommended secure mode).
- Confirm certificate issuance and HTTPS accessibility.
- Only then switch/confirm canonical host strategy:
  - Option 1: apex -> www redirect
  - Option 2: www -> apex redirect
- Implement canonical redirect consistently.

E) Verification checklist
- Verify desktop + mobile rendering.
- Verify static assets load (CSS/JS/fonts/images).
- Verify no mixed content warnings.
- Verify cache headers are reasonable.
- Verify links to external providers (e.g., Vimeo embeds) still function.
- Provide final validation report with URLs and status.

F) Deliverables I expect from you
1) Final production URL(s)
2) Exact settings used in Cloudflare Pages
3) DNS records created/updated (type, name, value, proxied yes/no)
4) Any repo changes made (with commit hash)
5) Rollback instructions (how to revert DNS/domain quickly)

Operational preferences:
- If CLI is available, you may use Wrangler/Cloudflare API; otherwise use dashboard workflow.
- Never delete existing DNS records without confirming impact.
- Before any risky action, show me:
  - what you will change
  - why
  - rollback plan

Start now with preflight and show me your plan + first actions.
```
