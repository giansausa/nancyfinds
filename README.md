# nancyfinds — Aura.today Marketing Funnel Source

Source of truth for the affiliate-marketing funnels on **aura.today** driving traffic to **nancyfinds.com**.

This repo is the backup + playbook archive. The live site lives in Webflow.

---

## Live URLs

| Funnel | Landing | Article |
|---|---|---|
| Editorial (non-scream) | [aura.today/landing-best-rose-toys-2026](https://www.aura.today/landing-best-rose-toys-2026) | [aura.today/blog-post/best-rose-toys-2026](https://www.aura.today/blog-post/best-rose-toys-2026) |
| Scream-themed | [aura.today/landing-rose-toys-scream](https://www.aura.today/landing-rose-toys-scream) | [aura.today/blog-post/8-rose-toys-make-you-scream](https://www.aura.today/blog-post/8-rose-toys-make-you-scream) |

---

## Repo structure

```
nancyfinds/
├── README.md                          ← you are here
├── playbook/
│   ├── strategy.md                    ← the whole marketing playbook
│   └── critical-ids.md                ← Webflow IDs (private — repo is private)
├── articles/
│   ├── non-scream-article.html        ← rendered article HTML fragments
│   └── scream-article.html
├── landing-pages/
│   └── state.md                       ← current state of both landing pages
├── mockups/
│   ├── D-button-styling.html          ← (REJECTED — too obvious)
│   ├── E-tldr-card.html               ← TL;DR card preview
│   ├── J-trust-strip.html             ← Trust pills preview
│   └── anchor-links-demo.html         ← Interactive anchor link demo
└── webflow-snapshot/
    ├── best-rose-toys-2026.json       ← full Webflow API fieldData
    └── 8-rose-toys-make-you-scream.json
```

---

## What shipped on 2026-05-16 (the conversion-optimization day)

11 changes, both funnels:

1. Landing CTA: "Continue Reading" → "Reveal the #1 Pick →" (non-scream) / "Reveal the #1 Scream-Maker →" (scream)
2. Credibility line under H1 on both landings
3. Urgency strips above all 10 Nancy Buy buttons (FTC-defensible "launch pricing" language)
4. % off math verified against live nancyfinds.com prices
5. Catchy tab titles on all 4 pages (specific-number-first format)
6. Multi-brand reorder on scream article (Bloom up to #3, Vine to #5)
7. Gray TL;DR card at top of both articles
8. Trust strip pills above TL;DR (both articles)
9. Anchor link IDs on all 16 H3 headings + clickable shortlists
10. Cross-funnel parity
11. Visual mockup workflow established (D/E/J + anchor demo on Desktop)

---

## How to restore from this repo

If Webflow ever breaks or content gets accidentally overwritten:

1. **Article content** → `webflow-snapshot/*.json` has the full `fieldData`. Use Webflow API `update_collection_items` with the snapshot's `fieldData` to restore.
2. **Landing page text** → `landing-pages/state.md` has current CTA copy and credibility line text. Edit in Webflow Designer.
3. **Tab titles** → `playbook/strategy.md` § "Tab titles" has the exact strings for all 4 pages.
4. **Critical IDs** → `playbook/critical-ids.md` for any Webflow API call.

---

## Where the strategy is documented

Read `playbook/strategy.md` first. It covers:
- Incognito multi-brand positioning (5 Nancy + 3 foil products)
- Slot order rationale (Nancy at 1/3/5/7/8)
- Editorial voice strategy (foil "Room for Improvement" cross-references)
- Conversion elements (TL;DR card, urgency strips, trust pills, anchor links)
- FTC-compliant urgency language
- Image strategy (Webflow CDN only, no nancyfinds.com hotlinking)

---

## Privacy reminder

**Keep this repo private.** It documents the incognito brand-anonymization strategy explicitly — Nancy mentions removed, foil-product redirects engineered, editorial voice tuned. If this leaked publicly, the cover would be blown.
