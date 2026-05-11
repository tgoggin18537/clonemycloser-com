# clonemycloser.com

Landing page for **Clone My Closer** — the productized SMS + email AI sales
bot service. We clone your top closer's writing into an AI that handles
your inbound 24/7, trained on thousands of their real conversations.

## Stack

- Vanilla HTML + Tailwind via Play CDN (no build step)
- Inter for body, Geist Mono for accents (Google Fonts)
- Phosphor icons (thin weight) via CDN
- Dark palette: `#0A0A0B` background, `#F5F2EC` text, `#FF6B35` signal
  orange accent
- Cloudflare Pages hosting on `clonemycloser.com`

## Pages

- `index.html` — main landing page (hero, demo, pricing, FAQ, CTA)

## Pre-launch swap checklist

Before pointing the domain at this and going live:

- [ ] Replace `[DEMO_PHONE_NUMBER]` with the real demo bot SMS line
- [ ] Replace `[CAL_LINK]` with the SavvyCal/Cal.com URL for booking
- [ ] Replace `[FOUNDER_LOOM_URL]` with the recorded founder video
- [ ] Add real client logos to `<div id="logo-strip">` (with permission)
- [ ] Add 1-2 written testimonials to `<div id="testimonials">` (with permission)
- [ ] Replace placeholder eval scorecard numbers with real eval data
- [ ] Configure a Cloudflare Worker to handle form submissions
      (forwards to GHL or to thomas@clonemycloser.com)
- [ ] Add Plausible or Cloudflare Web Analytics
- [ ] Verify all internal anchors scroll cleanly

## Deploy

First time:
```bash
wrangler pages project create clonemycloser-com
wrangler pages deploy . --project-name=clonemycloser-com --branch=main
```

Then in Cloudflare dashboard: add custom domain `clonemycloser.com`
(auto-creates CNAME).

Subsequent deploys: `./scripts/deploy.sh`

## Source

Generated 2026-05-11 from the SKU pivot deep dive. Master plan at
`~/Obsidian/Brain/03-projects/clone-my-closer/master-plan-2026-05-11.md`.
