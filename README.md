# Hakuna Matata by Jannat — website

Multi-page restaurant site (Home · Menu · Deals · Order · Visit) in one `index.html`, no build step.

## Structure
```
index.html          ← the whole site (HTML + CSS + JS, hash-routed pages: #/menu, #/deals, #/order, #/visit)
assets/
  logo.svg          ← the Hakuna Matata mark, vector-traced from the menu board
  favicon.svg
  img/              ← food cut-outs (WebP with transparency) + blurred backdrop plates
```

## Deploy
Push to GitHub and import the repo in Vercel (framework preset: **Other**, no build command, output dir: `/`). GitHub Pages works too.

## Edit content
- **Prices / items / deals:** `MENU` and `DEALS` arrays near the top of the `<script>` in `index.html`.
- **Phone / WhatsApp:** search for `923298713517` and `0329-8713517`.
- **Address / hours / Instagram:** the `.tbc` placeholders on the Visit page.
- **Photos:** drop new WebPs into `assets/img/` and update the `src` paths (or the `IMG` map in the script).

## Stack
GSAP 3.12 + ScrollTrigger, Lenis smooth scroll (CDN). Orders are kept in `localStorage` and sent to WhatsApp as a pre-filled message. The chatbot is rule-based and reads the same `MENU`/`DEALS` data, so it needs no API key.
