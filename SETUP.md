# Setup Guide — Getting a Fresh Claude to Continue This Work

**Goal**: On a brand-new computer, a fresh Claude Code session should be able to pick up these funnels and work on them with the same strategy, same tools, same context as the original.

This guide covers what the repo CAN'T preserve: the operating environment and the conversation memory.

---

## What this repo has vs what you still need to set up

| Layer | In repo? | What you do |
|---|---|---|
| Article content + restoration HTML | ✅ Yes | Nothing — just `git clone` |
| Strategy playbook | ✅ Yes | Read `playbook/strategy.md` first |
| Webflow IDs + asset references | ✅ Yes | `playbook/critical-ids.md` is your cheat sheet |
| Mockups + design history | ✅ Yes | Open the HTML files locally to view |
| **Claude Code itself** | ❌ No | Install per below |
| **Webflow MCP + API token** | ❌ No | Configure per below — gives Claude write access to the CMS |
| **Microsoft Clarity dashboard** | ❌ No | Sign in to https://clarity.microsoft.com with the same account |
| **Skills (Agent Gian, etc.)** | ❌ No | Install per below — controls Claude's working style |
| **Conversation memory** | ❌ No | Paste the kickstart prompt below into the new Claude session |

---

## One-time machine setup

### 1. Install Claude Code

Mac/Linux:
```bash
npm install -g @anthropic-ai/claude-code
```

Windows (PowerShell, run as admin if needed):
```powershell
npm install -g @anthropic-ai/claude-code
```

Verify:
```bash
claude --version
```

If you don't have Node.js, install it first: https://nodejs.org

### 2. Configure the Webflow MCP

The Webflow MCP is what gives Claude the ability to read and update the live site via API. Without it, Claude is just reading the repo — it can't actually edit aura.today.

1. Sign in to Webflow → top-right user menu → **API access**
2. Create a new Site Token (or Workspace Token if you use Webflow API across multiple sites)
3. Scope: read + write on **Aura Lifestyle Magazine** (site ID `679148ba0c2d7fe8766ce6cd`)
4. Copy the token

In Claude Code, add the Webflow MCP to your settings:
```bash
claude mcp add webflow
```

When prompted, paste the token. Verify by running this command inside a Claude session:
```
List the pages on site 679148ba0c2d7fe8766ce6cd
```

Claude should return the list of pages — including `landing-best-rose-toys-2026`, `landing-rose-toys-scream`, etc.

### 3. (Optional but recommended) Install the Agent Gian methodology

The original session used Agent Gian — a shipping methodology that enforces things like:
- Peer-tone communication, no hedging
- Lead with answer + recommendation
- Auto-push commits after merging
- Honest dimension-scored reviews
- No optionality theater

If you want the new Claude to behave the same way:
```bash
# In a fresh terminal
claude --help  # confirm Claude Code is installed
# Then ask Claude to install Agent Gian
```

Then in Claude:
```
Install Agent Gian methodology with auto-push enabled.
```

This sets up the global `~/.claude/CLAUDE.md` with the 40 Agent Gian rules.

### 4. (Optional) Microsoft Clarity access

Conversion measurement happens via Microsoft Clarity (project `wrb7m88lni`). To see analytics:
1. Sign in at https://clarity.microsoft.com with the account that owns the project
2. Open the "Aura" project to see session recordings, heatmaps, click counts

Claude does NOT need direct Clarity access for editing — just for reading analytics when asked "how is the funnel performing?".

### 5. Clone the repo

```bash
git clone https://github.com/giansausa/nancyfinds.git
cd nancyfinds
```

---

## The kickstart prompt — paste this into a fresh Claude session

Once Claude Code is installed and the Webflow MCP is connected, open Claude inside the `nancyfinds` directory and paste this:

```
I'm continuing work on the Aura.today × Nancy Finds affiliate marketing
funnels. The strategy and current state are documented in this repo.

Before doing anything:
1. Read playbook/strategy.md — this is the complete marketing playbook.
   The "incognito multi-brand editorial" framing is non-negotiable.
   Nancy is at slots 1/3/5/7/8; foils at 2/4/6.
2. Read playbook/critical-ids.md — Webflow site/collection/page/item IDs
   for any API call you need to make.
3. Read README.md for the file map.

Then verify your tool access:
- Confirm the Webflow MCP is connected by listing the Blog Posts collection
  items (collection ID 679b57c29c98d0ebaa7678c5).
- You should see at least 2 items: "best-rose-toys-2026" (item ID
  6a054f613630e12a56a2e38e) and "8-rose-toys-make-you-scream"
  (item ID 6a06c55ba44d4099c949bea6).

Once verified, ask me what we're working on today. Do NOT make any edits
to the live site until I give you a specific instruction.

Important constraints (from the strategy doc):
- The incognito framing must be preserved. No edits that obviously favor
  Nancy (e.g., colored buttons, branded badges).
- Urgency strip language must stay FTC-defensible ("launch pricing",
  never "ends [date]").
- Images must live on Webflow CDN — never hotlink from nancyfinds.com.
- The author persona is Madison Hayes. Don't introduce other personas.
```

---

## How to verify everything works (5-minute sanity check)

Once you've pasted the kickstart prompt, ask Claude to:

1. **Read both articles** from the Webflow API:
   ```
   Show me the title-tag, post-author-3, and first paragraph of post-lead for both blog post CMS items.
   ```
   Expected: returns the current title tags and Madison Hayes byline.

2. **Verify pricing math** against nancyfinds.com:
   ```
   Fetch nancyfinds.com/products/nancy-blossom-duo and confirm the price is $64.99 (was $104.99).
   ```
   Expected: returns the prices, confirms 38% off math.

3. **Check the live URLs** are loading:
   ```
   Fetch https://www.aura.today/blog-post/best-rose-toys-2026 and report whether the TL;DR card and trust strip pills are present.
   ```
   Expected: returns yes — both elements visible in the HTML.

If all three pass, you're back at the same operating state as the original session.

---

## What still won't transfer

Even after this setup, the new Claude session WILL be missing:

1. **The decision history** — what we tried, what we rejected (e.g., D button styling, H review quotes), and why. The playbook captures the WHY for major decisions, but not every micro-iteration.

2. **The "in flight" intuitions** — the back-and-forth that shaped the gray-not-pink TL;DR, the softened-not-hard-deadline urgency language. The conclusions are in the repo. The reasoning gets reconstructed each session.

3. **The relationship cadence** — the new Claude won't know that you prefer visual mockups before shipping, that you check the % off math personally, that you reject anything "too obvious." These are the personality calibrations the original session learned mid-conversation.

You can speed this up by adding to the kickstart prompt:
- "I prefer visual mockups before shipping any UI changes."
- "I always verify pricing math before approving urgency claims."
- "Reject any change that visibly tips the hand on the incognito framing."

Or just let the new Claude learn it the same way — by asking the right questions and getting calibrated.

---

## When to update this guide

Update SETUP.md if:
- The Webflow API authentication flow changes
- A new MCP is added to the workflow
- The skill set changes (Agent Gian gets new rules, etc.)
- A new step is needed to onboard a fresh machine

This is the document that gets you from zero to "Claude can work on aura.today again." Treat it as the operating manual.
