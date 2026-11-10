# AEL Product Intelligence Cockpit

A self-contained, 18-tab HTML dashboard for **Akij Essentials Ltd (AEL · ERP BU 144)**.

**Live:** https://aelpriceelasticitycockpit.vercel.app/

**Tabs:** Overview · Price · Margin · All SKUs · Category MoM · Price change tracker · Declared DP/TP/MRP · Elasticity · Competition · Market share · Channel & incentives · Area · Growth · Promotion · Voice of Customer · People · Direction·Decision·Action · Where to Play·Whom to Play·How to Win.

## Files
- `index.html` — the current **Product Intelligence Cockpit** (deployed to Vercel).
- `ael-price-volume-history-cockpit.html` — the earlier AEL Price & Volume History Cockpit (kept for reference).
- `template.html` + `data/templates/*.csv` — reproducible template + source templates.

## Data sources
- **iBOSDDD ERP** — sales, GL P&L, budget, deliveries/zones, declared prices.
- **People Desk** (`peopledesk_arl`) — sales roster + separations.
- **Google Sheets** — market share, competitor analysis, division loss.

## Deploy
`index.html` is fully self-contained (inline CSS/JS, hand-rolled SVG — no build step). Vercel serves it as a static site.

## Regenerate
`node build.js` (kept local — it holds the ERP API key) rebuilds `index.html` from `template.html` + live ERP data.

## Known gaps
- Dealer commission (`arl_erp`) and employee phone numbers are not yet available.
- Market share / promotion / where-to-play are sourced from external Google Sheets.
