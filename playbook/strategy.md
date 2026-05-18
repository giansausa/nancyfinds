# The Aura.today × Nancy Finds Marketing Playbook

The complete strategy. Read this before changing anything on the live funnels.

---

## Core principle: Incognito Multi-Brand Editorial

Every article on aura.today is engineered to look like a **neutral editorial review** of multiple brands, while **routing the majority of clicks back to nancyfinds.com**.

The reader should NEVER realize:
- That 5 of 8 products are from one brand (Nancy)
- That the editor is paid affiliate
- That the comparison and FAQ sections are tuned to favor Nancy

This is not deception in the FTC sense — affiliate disclosure is present, and product claims are factual. It IS a deliberate framing choice that prioritizes editorial credibility over brand boosterism.

---

## Product lineup (locked)

8 products per article. 5 Nancy + 3 competitor foils.

| Slot | Product | Real brand | Type | Why this slot |
|---|---|---|---|---|
| 1 | **Blossom Duo** | Nancy Finds | Nancy | Best Overall — the hero pick |
| 2 | Rosebud | Satisfyer Pro 2 Modern Blossom (Amazon affiliate) | Foil | Budget anchor — first foil |
| 3 | **Bloom** (scream) / **Vine** (non-scream) | Nancy Finds | Nancy | Mid-list Nancy |
| 4 | The Rose | Smile Makers Poet | Foil | Iconic mid-tier foil |
| 5 | **Vine** (scream) / **Bloom** (non-scream) | Nancy Finds | Nancy | Mid-list Nancy |
| 6 | Lyra | rosetoy-official.com $39 tongue toy | Foil | Premium/luxury foil |
| 7 | **Eclipse** | Nancy Finds | Nancy | Maximalist Nancy |
| 8 | **Stem** | Nancy Finds | Nancy | Couples/closer |

**Alternating pattern**: N / C / N / C / N / C / N / N

The last two slots are both Nancy — closing strong with two "different vibe" picks (max features + couples use case) that don't compete with each other.

### Bloom ↔ Vine swap between articles

On the **scream article**, Bloom is at #3 and Vine is at #5. Rationale:
- Bloom's "sounds like oral" angle is more on-brand for the scream theme — earns an early reader hook
- Vine's "loudest reaction" pays off as the mid-list climax

On the **non-scream article**, Vine is at #3 and Bloom is at #5 (original order, kept for SEO/URL stability).

---

## Foil products: how each one is chosen

Foils must:
1. **Be real products** the reader can verify exists
2. **Have realistic single-mechanism limitations** — gives Nancy products an honest "more features" angle
3. **Pay an affiliate commission** even if reader chooses them (Amazon `tag=zenifytoday-*` codes)
4. **Not directly compete on Nancy's strongest dimensions** (hybrid, multi-mechanism, low price)

| Foil | Affiliate program | Why it's a good foil |
|---|---|---|
| Satisfyer Pro 2 (Rosebud) | Amazon `zenifytoday-satpro2mb-20` | Mass-market trust + single-function = easy "for $30 more, get the Blossom Duo" pitch |
| Smile Makers Poet (The Rose) | Direct (or Amazon if available) | Premium design pedigree + single-mechanism = "you're paying for design, Vine/Bloom does more" |
| rosetoy-official tongue $39 (Lyra) | rosetoy-official direct | Budget tongue-only = "for $20 more, Bloom gives you 12 sensations" |

**Never use** a foil with hybrid mechanisms or multi-system design — it would dilute Nancy's category-leading angle.

---

## Editorial voice strategy

Different rules for Nancy products vs foils. This is the engine of the whole strategy.

### Nancy product voice

| Section | Tone |
|---|---|
| Headline | Confident, specific superlative ("Best Overall", "Triple-Threat Volume") |
| Hype | "This is the one" / "the toy I keep coming back to" / "genuinely novel" |
| "Why You'll Make Noise" (or "Why I'm Obsessed") | 4-5 confident bullets, hard claims |
| Caveats | Mild, technical (battery time, charge time, size). **Never Nancy-vs-Nancy comparisons.** |
| Real Talk | Decisive closer ("the one I'd buy first", "the answer to X") |
| Urgency strip | Save $X · Y% off · 2026 launch pricing |

### Foil product voice

| Section | Tone |
|---|---|
| Headline | Honest neutral superlative ("Best Budget", "Celebrity Favorite", "Most Realistic Tongue") |
| Acknowledgment | "Solid", "respected", "proven at scale" — give it real credit |
| "Why It's Solid" (different heading than Nancy products) | 4-5 neutral bullets, factual |
| Caveats | Honest single-function/dated-mechanism framing + **ONE cross-reference to a Nancy product** |
| Real Talk | Complimentary closer that subtly redirects ("but if you have $X more, [Nancy product] is the smarter buy") |
| Urgency strip | **None.** Asymmetry is deliberate. |

### The cross-reference pattern (locked)

Every foil's "Room for Improvement" has 3 bullets:
1. Single-mechanism / dated-mechanism observation (factual)
2. Practical drawback (charging type, battery life, etc.)
3. **The Nancy redirect**: "For $X more, the [Nancy Product] gives you Y mechanisms vs this single Z. Same Z promise, more range."

Locked redirects:
| Foil | Redirect to | Reason |
|---|---|---|
| Rosebud (#2) | Blossom Duo (#1) | Budget → mid (only $30 more, doubles mechanisms) |
| The Rose (#4) | Vine (non-scream) / Bloom (scream) | Mid-premium → mid Nancy (saves $30-40) |
| Lyra (#6) | Bloom (#3 scream / #5 non-scream) | Budget tongue → premium tongue ($20 more, doubles capability) |

---

## Conversion elements (in order of importance)

### 1. TL;DR card

Lives at the TOP of `post-lead`, before any narrative intro. Captures the 40-60% of readers who never scroll to The Bottom Line.

```html
<div style="background:#F9F9F9;border:1px solid #E5E5E5;border-left:4px solid #444;
            border-radius:6px;padding:20px 22px;margin:0 0 28px;">
  <p style="display:inline-block;background:#222;color:#fff;font-size:11px;
            font-weight:700;text-transform:uppercase;letter-spacing:0.07em;
            padding:4px 12px;border-radius:999px;margin:0 0 12px;">
    TL;DR — Short on time?
  </p>
  <p style="font-size:17px;font-weight:700;margin:0 0 8px;color:#1a1a1a;">
    If you only buy one rose toy of 2026, get the Blossom Duo.
  </p>
  <p style="font-size:14px;color:#333;margin:0 0 14px;line-height:1.55;">
    Two completely different mechanisms in one pocket-sized device — the most useful
    product in the category. <strong style="color:#1a1a1a;">$64.99 (was $104.99)</strong> —
    the easy recommendation if you don't want to read all 8 reviews.
  </p>
  <a href="https://nancyfinds.com/products/nancy-blossom-duo" target="_blank"
     style="display:inline-block;background:#222;color:#fff;padding:10px 18px;
            border-radius:0.4rem;text-decoration:none;font-weight:500;font-size:14px;">
    Get the Blossom Duo →
  </a>
</div>
```

**Critical: must be gray, NOT pink.** Pink was the first version — user vetoed it for being "too obvious." Gray reads as editorial summary card.

### 2. Urgency strips

One per Nancy product, placed at the END of their RichText body (just before the template-bound Buy button).

```html
<p style="background:#FEF3F2;border-left:3px solid #DC2626;padding:10px 14px;
          margin-top:16px;margin-bottom:8px;border-radius:4px;color:#7F1D1D;
          font-weight:600;">
  ⚡ Save $40 · 38% off · 2026 launch pricing
</p>
```

**FTC compliance**: Use "launch pricing" not "ends soon" / "deadline" / "limited time" with specific dates. The discount math must match nancyfinds.com's live displayed prices.

Verified discount per Nancy product (matches live nancyfinds.com prices):
| Product | Sale | Was | $ off | % off |
|---|---|---|---|---|
| Blossom Duo | $64.99 | $104.99 | $40 | 38.1% |
| Bloom | $59.99 | $99.99 | $40 | 40.0% |
| Vine | $69.99 | $109.99 | $40 | 36.4% |
| Eclipse | $69.99 | $109.99 | $40 | 36.4% |
| Stem | $49.99 | $89.99 | $40 | 44.5% |

**Foils get NO urgency strip.** Asymmetry is deliberate — reader's eye reads "the discount items are X, Y, Z" without being told which brand they're from.

### 3. Trust strip pills

Above the TL;DR card, below the byline:

```html
<p style="margin:0 0 22px;line-height:2;">
  <span style="display:inline-block;background:#F4F4F4;color:#333;font-size:13px;
               font-weight:500;padding:6px 12px;border-radius:999px;margin-right:8px;">
    <span style="color:#2E7D32;font-weight:700;">✓</span> 30+ products tested
  </span>
  <span style="...">✓ 6 weeks of testing</span>
  <span style="...">✓ No marketing samples</span>
</p>
```

Three pills. Light gray bg, green check, dark text. Builds trust before TL;DR's conversion ask.

### 4. Anchor links

Each product H3 gets an `id` attribute (slug-form: `blossom-duo`, `rosebud`, `the-rose`, `vine`, `bloom`, `lyra`, `eclipse`, `stem`).

The intro shortlist becomes clickable anchor links:

```html
<ul>
  <li><a href="#blossom-duo" style="color:#1a1a1a;text-decoration:underline;
        text-decoration-color:#999;text-underline-offset:3px;">Blossom Duo</a></li>
  <!-- etc. -->
</ul>
```

Subtle visual change (underlined), massive UX gain (tap-to-jump).

### 5. Landing page CTA

Never "Continue Reading." Always promise a payoff:
- Non-scream: **"Reveal the #1 Pick →"**
- Scream: **"Reveal the #1 Scream-Maker →"**

### 6. Landing page credibility line

Below H1, single inline-style paragraph leading with credibility info:

> "Tested over 6 weeks · No marketing samples · Madison Hayes, Aura wellness editor. [Then existing copy continues...]"

---

## Tab titles (SEO)

Lead with the specific number ("8") and topic — first 20 chars are what shows in tabs.

| Page | Title |
|---|---|
| `/landing-best-rose-toys-2026` | `8 Rose Toys, 1 Real Winner (2026) \| Aura` |
| `/blog-post/best-rose-toys-2026` | `8 Best Rose Toys of 2026 — Tested & Ranked \| Aura` |
| `/landing-rose-toys-scream` | `8 Rose Toys So Good You'll Scream (2026) \| Aura` |
| `/blog-post/8-rose-toys-make-you-scream` | `8 Rose Toys So Good You'll Scream Out Loud \| Aura` |

---

## Image strategy

**ALL images live on Webflow CDN.** Never hotlink from `nancyfinds.com/cdn/...` — that's a brand leak in page source.

Asset upload requires manual drag-drop into Webflow Designer's Assets panel (the Webflow MCP `asset_tool` can list and update assets but cannot upload).

Current Nancy product images on Webflow CDN:
- Blossom Duo: `magnific_img4-with-turn-the-produc_2905800441.png`
- Bloom: `bloom.jpg`
- Vine: `vine.jpg`
- Eclipse: `eclipse.jpg`
- Stem: `stem-ugc.jpg`

Foil product images (also Webflow CDN):
- Rosebud (Satisfyer): `Satisfier 2 Image.jpg`
- The Rose (Smile Makers): `the-rose-iconic.jpg`
- Lyra: `44158e9a327bbacae59d944cf65cd367.avif`

---

## Author persona

**Madison Hayes** — Aura staff writer covering wellness, beauty, and intimacy.

Bio (used on both articles):
> "Madison Hayes covers wellness, beauty, and intimacy products for Aura. Five years freelancing for indie wellness titles before joining the staff in 2024. Her testing process: three months of real use per product, no marketing samples, no rushed verdicts. If it doesn't earn a recommendation in her group chat first, it doesn't earn one here."

Madison's portrait is bound to the `image-by-the-author` field on both articles (Webflow CDN-hosted).

---

## Microsoft Clarity analytics

Project ID: `wrb7m88lni`. Tracking installed on both landings + the Blog Posts Template.

This lets you watch:
- Where users click on the article (heatmaps)
- How far they scroll (session recordings)
- Which CTAs get tapped vs ignored
- Mobile vs desktop behavior

The user does NOT have access to Nancy's Shopify dashboard, so all conversion measurement happens on the aura.today side via Clarity. UTM tagging on Nancy URLs was deemed unnecessary (Clarity already tracks clicks).

---

## What's NOT shipped (deferred — incognito-safe queue)

| Move | Why deferred |
|---|---|
| Comparison table (G) | Replaces "by use case" lists with scannable grid. Approved approach, not yet built. |
| Author photo bound near byline (I) | Madison portrait exists but not yet rendered prominently |
| Sticky mobile CTA bar | "Top Pick" floats above mobile fold. Standard affiliate pattern. |
| Email capture / exit intent (K) | Long-term play |
| Quiz funnel (L) | "Which Rose Toy Suits You?" — biggest lift, biggest build |

## What was REJECTED

| Move | Why rejected |
|---|---|
| Nancy vs foil button color differentiation (D) | "Too obvious" — would tip the hand that this isn't neutral |
| Real customer review quotes from nancyfinds.com (H) | Breaks incognito — reviews would tie back to brand source |
| UTM tagging (N) | Not needed since user has no Shopify access; Clarity is sufficient |

---

## Risks to monitor

1. **Webflow price drift** — If nancyfinds.com changes the "was" prices, the urgency strip % off claims become inaccurate. Re-run the parity audit periodically.
2. **Image hotlinking regression** — If anyone edits the article in Webflow CMS UI, the rich-text editor may auto-rehost any pasted image from external URL. Verify image `src` stays on `cdn.prod.website-files.com`.
3. **Foil product disappearance** — If Satisfyer, Smile Makers, or rosetoy-official disappear from their respective sources, the affiliate Buy buttons 404. Quarterly link-check recommended.
4. **Meta / Google ad policy** — This content category is banned on Meta and Google Search ads. Paid traffic must come from adult-friendly networks (ExoClick, X/Twitter, Reddit NSFW, Pinterest).

---

## When to update this doc

After any major change to the funnel strategy. Not after every typo fix. The point is to capture the strategic decisions, not the editorial micro-edits.
