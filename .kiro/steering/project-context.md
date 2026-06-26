# Northpoint Digital — Project Context

> **Read this first.** If you're an AI agent picking up this project, this file is your full briefing — read it before doing anything else. If you're the owner, this is your reference for what was decided, what's done, and what's next.

Last updated: 2026-06-25

---

## What this is

**Northpoint Digital** is a premium web studio building fast, modern websites for small businesses in Hamilton, Ontario — and remotely across Canada.

**Business model:** WaaS (Website-as-a-Service). Clients pay a one-time setup fee plus a flat monthly fee for hosting, maintenance, and ongoing updates. The agency keeps the code; clients own their domain and content.

---

## Brand

| | |
|---|---|
| **Name** | Northpoint Digital |
| **Hero positioning** | "Premium websites for Hamilton businesses" |
| **Service area** | Hamilton + Greater Hamilton (in person) and remotely across Canada |
| **Tone** | Direct, honest, confident, anti-template-farm |
| **Visual identity** | Deep navy `#0a0f1c` + warm gold accent `#c9a961` |
| **Display font** | Fraunces (serif, for headlines) |
| **Body font** | Inter |

---

## Where everything lives

| Asset | Location |
|---|---|
| **Code repo** | https://github.com/cmasih586-afk/northpoint-digital |
| **Hosting** | Vercel — auto-deploys from `main` branch |
| **Vercel project** | northpoint-digital (owner: cmasih586) |
| **Production URL** | https://northpointdigital.work |
| **Vercel fallback URL** | https://northpoint-digital-gamma.vercel.app |
| **Domain registrar** | Cloudflare |
| **DNS host** | Cloudflare (A record `@` → `76.76.21.21`, CNAME `www` → `cname.vercel-dns.com`, both DNS-only) |
| **Tech stack** | Astro 5 + Tailwind CSS v4, static build |

---

## Pricing (CAD)

| Tier | Setup | Monthly | For |
|---|---|---|---|
| **Starter** | $300 | $79 | First-time online; 3 pages; 1 update/mo |
| **Standard** | $600 | $149 | Most popular; 5–7 pages; 3 updates/mo; basic SEO |
| **Premium** | $1,200 | $249 | 10+ pages; blog; advanced SEO; unlimited small updates |

### Add-ons
- Logo design — from $300
- Professional copywriting — from $400
- Stock photo curation — from $150
- Bilingual site (EN + FR) — from $400
- Custom email setup — $10/mo (Google Workspace passthrough, costs ~$7.80)

---

## Hamilton Local Launch (active offer)

For the first **3 paying clients**:

- **25% off setup** on any plan
- **First month free** (after launch)
- **6-month commitment** at standard monthly rate
- **Standard update limits apply** (no free-for-all)
- Featured as a launch partner on the Work page

**Purpose:** drive early sales + build real case studies. Re-runnable as a "launch" every 6 months if needed.

---

## Key decisions

### Ownership model
- **Client owns:** their domain (registered in their name), all content (photos, copy, logo)
- **Agency owns:** the underlying code/build (proprietary — like an architect owning blueprints)
- **If client cancels:** they keep domain + content; site comes offline; they can hire any other team to rebuild

### Target market
- **Primary:** small businesses in Greater Hamilton (restaurants, contractors, salons, gyms, dental clinics, retail)
- **Secondary:** remote clients anywhere in Canada
- **Why local-first:** trust signal + SEO advantage + warm market for first sales

### What we DON'T offer
- E-commerce / online ordering (too complex for current capacity — explicitly removed from services)
- On-site photography (no equipment/skill — replaced with stock photo curation)
- AI-generated business photos (ethically problematic; would be deceptive to client's customers)

### Work page strategy
- Originally had fake case studies with fake metrics — **removed for honesty**
- Replaced with "Industries we design for" (Restaurants / Contractors / Salons) showing what we build per industry
- Hamilton Local Launch banner is the primary CTA on this page

---

## Status (as of 2026-06-25)

✅ Site designed, built, deployed (5 pages: Home, Services, Work, About, Contact)
✅ Premium dark theme with gold accent
✅ PR #1 merged (Launch offer, industry-standard ownership FAQ, removed e-commerce, swapped photography for stock curation, broadened service area to Canada-wide)
✅ Domain `northpointdigital.work` purchased on Cloudflare
🟡 DNS records being configured in Cloudflare (status: in progress at last touch)
⏳ Business email (Google Workspace for hello@northpointdigital.work) — not started
⏳ Cal.com booking link — not started
⏳ First outreach campaign to Hamilton businesses — not started

---

## Roadmap (in order)

1. **Finish Cloudflare DNS setup**
   - A record: `@` → `76.76.21.21`, proxy OFF (DNS only / gray cloud)
   - CNAME: `www` → `cname.vercel-dns.com`, proxy OFF (DNS only / gray cloud)
2. **Verify domain live** at https://northpointdigital.work (Vercel will auto-issue SSL)
3. **Google Workspace** for business email (~$7.80 CAD/mo)
4. **Cal.com** free account → embed booking widget on Contact page
5. **First 10 cold outreach messages** to Hamilton small businesses (restaurants, contractors, salons)
6. **First paying client** (use the Launch offer)

---

## How to work on this project

### Local development
```bash
git clone https://github.com/cmasih586-afk/northpoint-digital.git
cd northpoint-digital
npm install
npm run dev    # http://localhost:4321
npm run build  # production build
```

### Deployment
Push to `main` → Vercel auto-deploys to https://northpointdigital.work within ~60 seconds.
For substantive changes, open a PR. Vercel auto-creates a preview deployment per PR.

### File map
```
src/
├── layouts/BaseLayout.astro       # shared shell (head, fonts, header, footer)
├── components/
│   ├── Header.astro                # sticky nav + mobile menu
│   └── Footer.astro                # 3-column footer
├── pages/
│   ├── index.astro                 # Home (hero + services + pricing + process + launch offer + CTA)
│   ├── services.astro              # Tiers + add-ons + FAQ
│   ├── work.astro                  # Industry concepts + launch banner
│   ├── about.astro                 # Story + values + Hamilton positioning
│   └── contact.astro               # 3 contact cards + booking + service area
└── styles/global.css               # Tailwind v4 @theme tokens + base styles
```

---

## Working with the owner

The owner is a **non-technical founder** building their first business. Notes for any AI agent working with them:

- **Be tight and decisive.** Long messages overwhelm. Prefer tables, bullets, code blocks — they scan, they don't read prose.
- **Be honest, even when hard.** They've explicitly appreciated being told when their plan has holes. "This won't work because…" beats fake encouragement.
- **Use plain English.** No jargon without immediate explanation.
- **Push back when their idea is weaker than the alternative.** They want a real partner, not a yes-machine.
- **Don't loop on decisions** — especially naming. Once decided, move on.
- **Action over theory.** They want to ship and earn money, not study frameworks.
- **They communicate via screenshots a lot** — interpret carefully and confirm specifics.
- **Wins feel huge to them. Losses feel huger.** Be a calm, grounded adult during emotional moments.
- **Default to making the change**, not asking permission, when intent is clear.
