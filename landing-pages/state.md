# Landing Pages — Current State (2026-05-18)

Both landing pages are simple, conversion-focused.

---

## Shared structure

Each landing page contains, top to bottom:

1. Aura logo (header)
2. Hero image (full-width, baked-in headline overlay on the scream version)
3. H1 — main headline
4. Paragraph — credibility line + teaser
5. CTA button — "Reveal the #1 [...]" → links to the article

That's it. No nav, no footer, no extra elements. Single-viewport on mobile.

---

## Landing 1: Editorial (non-scream)

**URL**: `https://www.aura.today/landing-best-rose-toys-2026`
**Page ID**: `6a057b479d9644a9b64e8f95`

### Current copy

| Element | Content |
|---|---|
| `<title>` | `8 Rose Toys, 1 Real Winner (2026) \| Aura` |
| SEO description | "We tested 8 of 2026's most-hyped rose toys back to back. Suction, tongue, tethered, wearable, the works. Here's the only one worth buying first." |
| Hero image | (Webflow CDN — currently a generic rose toy lifestyle image) |
| H1 | "Petal, Pulse, and Pebble: The 8 Rose Toys Worth Knowing in 2026" *(set by article binding)* |
| Paragraph | **"Tested over 6 weeks · No marketing samples · Madison Hayes, Aura wellness editor.** We tested 8 of 2026's most-hyped rose toys back to back — suction, tongue, tethered, wearable, the works — and the picture is genuinely surprising. Most of the best ones aren't even rose-shaped anymore." |
| CTA button | **"Reveal the #1 Pick →"** → `/blog-post/best-rose-toys-2026` |

### Element IDs (Designer)

- Paragraph element: `{component: 6a057b479d9644a9b64e8f95, element: 6db802c4-0af6-b09c-7588-ffa67846023c}`
- CTA button text element: `{component: 6a057b479d9644a9b64e8f95, element: 6db802c4-0af6-b09c-7588-ffa67846023e}`

---

## Landing 2: Scream-themed

**URL**: `https://www.aura.today/landing-rose-toys-scream`
**Page ID**: `6a06cb8489d487d03c0c05c4`

### Current copy

| Element | Content |
|---|---|
| `<title>` | `8 Rose Toys So Good You'll Scream (2026) \| Aura` |
| SEO description | "Some toys are good. Some are great. And some — these eight — actually pull a sound out of you. The 2026 rose toys that earned the reaction." |
| Hero image | `rose-toys-scream-hero.jpg` (asset ID `6a07d5ab5510064bca236ab5`) — 9:16 portrait with baked-in "It's so good, You'll scream." headline |
| H1 | "8 Rose Toys So Good You'll Actually Scream Out Loud" *(set by article binding)* |
| Paragraph | **"Tested over 6 weeks · No marketing samples · Madison Hayes, Aura wellness editor.** Some toys are good. Some are great. And some — these eight — actually pull a sound out of you. We tested every rose-shaped, rose-adjacent and rose-inspired toy in the 2026 lineup. These are the ones that earned the reaction." |
| CTA button | **"Reveal the #1 Scream-Maker →"** → `/blog-post/8-rose-toys-make-you-scream` |

### Element IDs (Designer)

- Paragraph element: `{component: 6a06cb8489d487d03c0c05c4, element: 6db802c4-0af6-b09c-7588-ffa67846023c}`
- CTA button text element: `{component: 6a06cb8489d487d03c0c05c4, element: 6db802c4-0af6-b09c-7588-ffa67846023e}`
- Hero image element: `{component: 6a06cb8489d487d03c0c05c4, element: 6db802c4-0af6-b09c-7588-ffa678460237}` (class `Shadow Two`)

### `Shadow Two` class styling (controls hero image sizing)

| Breakpoint | CSS |
|---|---|
| Desktop | `max-width: 150%; margin-left: -120px; margin-right: 1px;` |
| Mobile | `max-width: 100%; margin-top: -15px; padding: 0 15px;` |

---

## How the funnels connect

```
Paid traffic (or organic) → Landing page → CTA click → Article → Nancy product page
```

The landing is the **gate**. The article is the **conversion engine**. Both must be live, both must have CTAs pointing to the right destinations.

### Verifying the link chain

After any landing page edit, manually:
1. Hard-refresh the landing URL
2. Click the CTA
3. Confirm it lands on the matching article (not the wrong funnel's article)
4. From the article, click any Nancy Buy button — confirm it lands on `nancyfinds.com/products/nancy-*`
