# Tony Evans — Brag Book Setup Guide

This is a Mintlify docs site structured as an enterprise sales brag book.
All files are ready to publish. Your only job is to fill in the `[FILL IN: ...]` placeholders.

---

## Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and create a **new repository**
2. Name it something like `tony-evans-brag-book`
3. Set it to **Public** (required for Mintlify free tier)
4. Don't initialize with a README (you have one already)

---

## Step 2: Upload These Files

Upload all files from this ZIP to the root of your GitHub repo.
Your repo structure should look exactly like this:

```
tony-evans-brag-book/
├── mint.json
├── introduction.mdx
├── deal-index.mdx
├── deals/
│   ├── twilio-strategic-1-2m.mdx
│   ├── segment-kraken.mdx
│   ├── segment-elf-beauty.mdx
│   └── 2600hz-enterprise.mdx
└── README.md
```

The easiest way: drag-and-drop all files into the GitHub repo via the web UI.

---

## Step 3: Connect to Mintlify

1. Go to [mintlify.com](https://mintlify.com) and sign up / log in
2. Click **New Docs**
3. Select **Connect GitHub**
4. Choose your `tony-evans-brag-book` repo
5. Mintlify will auto-detect `mint.json` and deploy your site

Your site will be live at: `https://[your-handle].mintlify.app`

---

## Step 4: Fill In Your Deal Details

Every `[FILL IN: ...]` placeholder is where your real deal content goes.
Open each `.mdx` file in any text editor (or directly in GitHub) and replace the placeholders.

**Rules for editing without breaking anything:**
- Only change text between `**` bold markers, inside `>` blockquotes, and after `FILL IN:` labels
- Don't touch anything inside `{}` curly braces — that's layout/styling code
- Don't change the `---` front matter section at the top of each file
- Don't rename files (the navigation in `mint.json` references them by filename)

**The order to fill in (suggested):**
1. Start with **Deal 01 (Twilio Strategic)** — most recent, freshest in memory
2. Then **Deal 02 (Kraken)** — strongest competitive story
3. Then **Deal 03 (e.l.f.)** — expansion story
4. Then **Deal 04 (2600Hz)** — territory build story
5. Last: update **Introduction** stats and notable logos

---

## Step 5: Preview Changes

Every time you push a commit to GitHub, Mintlify auto-rebuilds in ~30 seconds.
You can also use the Mintlify CLI to preview locally:

```bash
npm i -g mintlify
mintlify dev
```

---

## Adding More Deals

To add a new deal page:

1. Copy any existing deal `.mdx` file in the `deals/` folder
2. Rename it (e.g., `deals/segment-one-finance.mdx`)
3. Update the front matter `title` and `description` at the top
4. Add the new filename to `mint.json` under `"Deal Case Studies"`:

```json
"pages": [
  "deals/twilio-strategic-1-2m",
  "deals/segment-kraken",
  "deals/segment-elf-beauty",
  "deals/2600hz-enterprise",
  "deals/segment-one-finance"   ← add here
]
```

---

## Customizing Colors / Branding

Everything visual is controlled by `mint.json`. To change:

- **Primary color:** Edit `"primary"` under `"colors"`
- **Site name:** Edit `"name"` at the top
- **Top bar CTA button:** Edit `"topbarCtaButton"`
- **LinkedIn link:** Edit `"topbarLinks"`

Current colors are set to Mintlify's own green (`#0D9373`) — which is a nice meta touch for this application.

---

## Questions?

If you get stuck on any step, the Mintlify docs are at [mintlify.com/docs](https://mintlify.com/docs).
The quickstart guide covers GitHub setup in detail.
