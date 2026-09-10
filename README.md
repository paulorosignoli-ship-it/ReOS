# The Unofficial Relocation Playbook — Landing Page

A single-page static site selling a 3-book series. No build step, no framework, no dependencies to install.

## Latest pass: the glossy makeover

Pushed the visual direction hard toward photo-saturated travel sites (Indonesia.travel, Bali Fun Day Tour) rather than a SaaS pricing page:

- **Hero** is now a full-bleed, slow-crossfading photo slideshow (4 images, pure CSS animation, no JS/video needed) with a scroll-cue indicator.
- **New Spotlight section** right after the hero — 4 large destination cards (one big feature + 3 standard), gold tier tags, hover zoom.
- **Pill-shaped buttons** everywhere (was rounded-rect, now fully rounded) for a warmer, less corporate feel.
- **New gold accent color** (`--gold` / `--gold-deep` / `--gold-tint`) used on ribbons, hero stats, prices, and one bonus card — breaks up the charcoal/teal palette without abandoning it.
- **Bonus Perks cards** now have rich teal→charcoal and gold→charcoal gradients with elevated icon badges instead of flat tint backgrounds.
- **CTA band** now has a photo backdrop (Costa Rica waterfall) with dark gradient overlay, bookending the hero visually.
- Tier card photo strips got a subtle hover zoom for interactivity.

Four new photos sourced for this pass: Argentina (Buenos Aires obelisk), Costa Rica (rainforest waterfall), Greece (Santorini), Japan (Kyoto), Vietnam (Hoi An lanterns), Malaysia (Petronas Towers) — all free-license Unsplash, hotlinked, no attribution required.

## What changed in the previous rebuild

The product is now three standalone ~30+ page books (not one book with bonus country packs):

- **Tier 1 — The Nearshore Playbook** ($27): Latin America & the Caribbean, 10 countries.
- **Tier 2 — The Old World & Mediterranean** ($37, includes Tier 1): Europe, Gulf & Africa, 10 countries.
- **Tier 3 — The Ultimate Arbitrage Suite** ($47, includes Tiers 1 & 2): Southeast Asia & the Indo-Pacific, 10 countries.

Each book follows the same 3-part system (Operational Framework → 10 Country Dossiers → Master Toolkit), but the framework chapters are region-specific, not shared/identical text — the site copy reflects that now.

Also added: a "Bonus Perks" section for the Notion trackers + comic companion that ship with every purchase, and a CSS-only "dossier format preview" mockup replacing the old page-screenshot gallery (which was built from a since-superseded single-book design).

**Tier 3's country list was corrected** to match the actual delivered book: Indonesia (Bali & Lombok, one dossier), plus Thailand, Vietnam, Malaysia, Philippines, Taiwan, Japan, South Korea, Sri Lanka, and Cambodia. Singapore is not in the current Tier 3 manuscript — Bali/Lombok were also merged into a single "Indonesia" dossier rather than two separate country chips.

## Files

- `index.html` — all page content
- `styles.css` — the full design system (charcoal/paper/teal palette, Lora + Inter + Poppins)
- `script.js` — mobile nav toggle + footer year

## Before you deploy

1. **Swap the three checkout links.** Search for `tier-btn` — three buttons ("Get The Nearshore Playbook", "Get The Old World Playbook", "Get The Arbitrage Suite"), each currently `href="#"`. Point each at its own Gumroad/Whop checkout URL.
2. **Optional: adjust pricing.** Search for `$27`, `$37`, `$47`.
3. **Optional: destination photos.** All photos are hotlinked from Unsplash (free license, no attribution required). Swap `src` attributes if you'd rather self-host.
4. **Optional: favicon.** None included yet.
5. **When the real PDFs are finalized:** the "Format Preview" section is currently a hand-coded CSS mockup of the Mexico dossier (not a screenshot), since the actual book designs are still in progress. Once final PDF layouts are locked, consider swapping it for a real page screenshot the same way the original single-book version did.

## Deploying

1. Push this folder to a GitHub repository (root, or point Vercel's "Root Directory" at wherever `index.html` lives).
2. Vercel: **Add New Project → Import** your repo.
3. Framework preset: **Other** (plain static HTML, no build command needed).
4. Deploy.

## Notes

- Fully responsive; mobile nav collapses into a hamburger menu below 640px.
- All copy is original.
- FAQ uses native `<details>/<summary>` — no JS needed for that part.
