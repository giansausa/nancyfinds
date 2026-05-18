# Critical Webflow IDs

Reference for any Webflow API call. Repo is private — these IDs are safe to keep here, but **do not commit any API tokens or secrets**.

---

## Site

| Field | Value |
|---|---|
| Site name | Aura Lifestyle Magazine |
| Site ID | `679148ba0c2d7fe8766ce6cd` |
| Workspace ID | `6791480a0869abc069b33bd0` |
| Primary locale | English (`679148ba0c2d7fe8766ce708`) |
| CMS Locale ID | `679148ba0c2d7fe8766ce709` |
| Custom domain — root | `aura.today` (ID: `67915048f6cf85e50e38c04b`) |
| Custom domain — www | `www.aura.today` (ID: `67915048f6cf85e50e38c060`) |
| Staging subdomain | `aura-lifestyle-magazine.webflow.io` |

---

## Pages

| Slug | Page ID | Type |
|---|---|---|
| `landing-best-rose-toys-2026` | `6a057b479d9644a9b64e8f95` | Static landing (non-scream funnel) |
| `landing-rose-toys-scream` | `6a06cb8489d487d03c0c05c4` | Static landing (scream funnel) |
| `detail_blog-post` | `679b57c29c98d0ebaa767b38` | Blog Posts CMS template |

---

## CMS Collection: Blog Posts

| Field | Value |
|---|---|
| Collection ID | `679b57c29c98d0ebaa7678c5` |
| Template page | `679b57c29c98d0ebaa767b38` |

### CMS items (the articles)

| Slug | Item ID | Funnel |
|---|---|---|
| `best-rose-toys-2026` | `6a054f613630e12a56a2e38e` | Editorial (non-scream) |
| `8-rose-toys-make-you-scream` | `6a06c55ba44d4099c949bea6` | Scream-themed |

### Blog Post CMS fields used

| Field slug | Type | Purpose |
|---|---|---|
| `name` | PlainText | Article title (renders in H1) |
| `slug` | PlainText | URL slug |
| `title-tag` | PlainText | `<title>` tag — what shows in browser tabs |
| `post-introduction-2` | PlainText | Grid card teaser |
| `post-author-3` | PlainText | "Written by Madison Hayes" |
| `image-by-the-author` | Image | Madison's portrait |
| `about-the-author` | PlainText | Bio paragraph |
| `post-lead` | RichText | **Trust strip + TL;DR card + intro paragraphs + shortlist** |
| `post-body` | RichText | Slot 1 (Blossom Duo) |
| `post-body-2` | RichText | Slot 2 (Rosebud) |
| `post-body-3` | RichText | Slot 3 (Vine or Bloom) |
| `post-body-4` | RichText | Slot 4 (The Rose) |
| `post-body-5` | RichText | Slot 5 (Bloom or Vine) |
| `post-summary-2` | RichText | **Slots 6+7+8 + Comparison + FAQ + Bottom Line** |
| `button-for-post-N` | Link | Buy button URL (slots 1-5) |
| `button-text-for-post-N` | PlainText | Buy button label (slots 1-5) |
| `post-image` | Image | Hero image (renders above title in template) |
| `main-image` | Image | Bottom-of-article image |
| `text-under-the-main-image` | PlainText | FTC disclosure caption |

### Important: 5-slot template limit

The Blog Posts CMS template only renders 5 product slots via template binding (`post-body` through `post-body-5` + matching `button-for-post-1` through `button-for-post-5`). **Slots 6, 7, 8 are crammed inline into `post-summary-2`** as a workaround — each has its own inline `<a>` Buy button styled to match the template buttons.

The fields `post-body-6`, `post-body-7`, `post-body-8`, `button-link-for-post-6/7/8`, `button-text-for-post-6/7/8` exist in the schema but are NOT rendered by the current Designer template. Leave them `null`.

---

## Microsoft Clarity

| Field | Value |
|---|---|
| Project ID | `wrb7m88lni` |
| Snippet location | Webflow site script (registered as `microsoft_clarity_tracking`) |
| Applied to | Landing pages + Blog Posts Template |

Source snippet:
```js
(function(c,l,a,r,i,t,y){c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)};
t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;
y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y);})
(window,document,"clarity","script","wrb7m88lni");
```

---

## Asset library reference

| Asset | Asset ID | Filename |
|---|---|---|
| Blossom Duo product | (varies — see article HTML) | `magnific_img4-with-turn-the-produc_2905800441.png` |
| Bloom product | — | `bloom.jpg` |
| Vine product | — | `vine.jpg` |
| Eclipse product | — | `eclipse.jpg` |
| Stem product (UGC) | `6a06c4699acde6d9d2245450` | `stem-ugc.jpg` |
| Rosebud (Satisfyer) | `6a06b6d297ccb50b75edf7e8` | `Satisfier 2 Image.jpg` |
| The Rose (Smile Makers) | `6a06b70c22fadaaa762c5eff` | `the-rose-iconic.jpg` |
| Lyra (rosetoy-official) | `6a06b644b47516f783e15ae6` | `44158e9a327bbacae59d944cf65cd367.avif` |
| Madison author portrait | `6a056fc14683cea34e895d1b` (non-scream) / `6a06c79da44d4099c94b1459` (scream) | `image-1778737021638.jpg` (and .jpeg) |
| Landing hero (non-scream) | `6a06bd4ac1e2beb89be83551` | `landing-page-tight.jpg` |
| Landing hero (scream) | `6a07d5ab5510064bca236ab5` | `rose-toys-scream-hero.jpg` |

---

## Affiliate program codes

| Brand | Affiliate code | Where used |
|---|---|---|
| Nancy Finds | (none — direct URLs to nancyfinds.com/products/*) | Slots 1, 3, 5, 7, 8 + TL;DR + Bottom Line |
| Amazon (Satisfyer/Rosebud) | `tag=zenifytoday-satpro2mb-20` | Slot 2 Buy button |
| Smile Makers (The Rose) | direct (no affiliate program AFAIK) | Slot 4 Buy button |
| rosetoy-official (Lyra) | direct affiliate via rosetoy-official.com | Slot 6 inline Buy button |
