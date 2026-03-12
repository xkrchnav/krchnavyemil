# MISSION & ROLE
You are an Elite Frontend Engineer and UI/UX Designer specializing in ultra-fast static sites. 
Your task is to build the official portfolio/racing website for **Emil Krchňavý #87**, a professional Slovak road racer. 
He competes in the IRRC, European Series Road Racing, and is making history as the **first Slovak ever at the legendary North West 200 (2025)**.

**Goal:** Create a blazing-fast, aggressive, bilingual (SK/EN) one-page website using Astro.js and Tailwind CSS for Cloudflare Pages. Burn minimal tokens—skip generic explanations and output production-ready code populated with the EXACT real data provided below.

## 1. TECH STACK & ARCHITECTURE
- **Framework:** Astro (SSG strictly).
- **Styling:** Tailwind CSS.
- **Images:** Strictly use Astro's native `<Image />` component. All images are in `src/assets/`.
- **i18n:** Simple sub-route system (`/` for Slovak, `/en/` for English). Use `src/i18n/sk.json` and `src/i18n/en.json`.

## 2. DESIGN SYSTEM (Aggressive Motorsport Theme)
- **Vibe:** Adrenaline, speed, asphalt, raw mechanical power.
- **Color Palette:**
  - **Background:** Deep Dark Gray/Pitch Black (`bg-zinc-950`).
  - **Primary Accent:** Neon/Kawasaki Green (`#39FF14` or `lime-500`). Use for #87, main CTA buttons, and highlights.
  - **Secondary Accent:** Racing Red (`#FF0000` or `red-600`). Use for secondary badges, hover states, and to match his Dynamax livery.
  - **Detail Accent:** Subtle Slovak Tricolor (White/Blue/Red) used as a tiny strip border on specific cards (e.g., the NW200 card) to emphasize national representation.
- **Typography:** Bold, aggressive sans-serif (`Oswald` or `Teko`). Apply `italic` and uppercase to headings to simulate motion. Use sharp edges (`rounded-none` or diagonal cuts).

## 3. PAGE STRUCTURE & EXACT CONTENT MAPPING

### A. Hero Section
- **Visual:** Full-screen background using `src/assets/hero-action.jpg` (use a shot with a high lean angle). Add a dark vignette overlay.
- **Content:** 
  - Subtitle (Small above name): "Official page of 🇸🇰 roadracer"
  - Main Title: "EMIL KRCHŇAVÝ"
  - Huge Watermark/Accent: "#87" in Neon Green.
  - Category: "Superbike / Superstock 1000"
- **CTA Buttons:** 
  1. "Sleduj Sezónu" (Neon Green, anchors to Updates)
  2. "Podpor NW200" (Red Outline, anchors to NW200 section)

### B. History Maker: North West 200 (Special Highlight Section)
- **Design:** This must pop. Use a skewed container with a red/green gradient border.
- **Text:** "North West 200 2025 - First 🇸🇰 rider ever."
- **PR Article Card:** Create a visually distinct card linking to his main sponsor's PR article.
  - *Title:* "Prvý Slovák na legendárnom Northwest 200"
  - *Excerpt:* "Emil Krchňavý prepisuje históriu slovenského motoršportu. Bude štartovať na jednom z najrýchlejších a najnebezpečnejších pretekov sveta."
  - *Link:* `https://www.dynamaxoil.com/emil-krchnavy-prvy-slovak-na-legendarnom-northwest-200/`
- **Visuals:** Display `src/assets/nw200-poster.jpg` (the crowdfunding poster) alongside `src/assets/nw200-letter.jpg` (the official Briggs Equipment entry acceptance letter).

### C. Career Highlights & Stats
- **Layout:** Aggressive timeline or grid format. Use the exact medals from his FB.
- **Stats to display:**
  - **Slovakia Cup +600:** 🥈2020 | 🥇2021 | 🥈2022
  - **IRRC Superbike:** Championship rider since 2022
  - **TOP 10 IRRC:** Horice 2023, Frohburg 2024
- **Visuals:** Insert a masonry gallery next to stats using `src/assets/wheelie-crest.jpg`, `src/assets/podium-trophy.jpg`, and `src/assets/track-pack.jpg`.

### D. The Machine & Fan Support
- **Content:** Detail the Kawasaki ZX-10R. Mention Mitas tires, Dynamax oil, Komaxit.
- **Fan Element:** Create a cool "Wall of Fame" block showcasing the image `src/assets/tail-fans.jpg` (the rear seat cowl with handwritten names of supporters). Text: "Hnaný vpred vďaka vám." (Driven forward thanks to you).

### E. Sponsors & Partners
- **Grid:** Clean layout for partner logos.
- **Key Logos:** Feature `src/assets/zd-motorsport.jpg` prominently (KRS Racing by ZD-Motorsport). 
- **CTA:** "Staň sa partnerom / Become a Partner" linking to the contact form.

### F. Contact & Socials
- **Form:** Simple static HTML form (Name, Email, Message) pointing to a dummy endpoint `https://api.web3forms.com/submit`.
- **Social Links:** Icons for Facebook and Instagram.

## 4. ASSET MAPPING INSTRUCTIONS (For the Agent)
Assume the following files exist in `src/assets/`. Use them exactly in these sections:
- `hero-action.jpg` -> Hero Section background.
- `nw200-poster.jpg` -> NW200 Promo card.
- `nw200-letter.jpg` -> NW200 Proof/History card.
- `wheelie-crest.jpg` -> Action gallery / Highlights.
- `podium-trophy.jpg` -> Near the SK Cup stats.
- `tail-fans.jpg` -> Fan support / The Machine section.
- `bike-detail.jpg` -> Near the technical specs.
- `zd-motorsport.jpg` -> Main sponsor in the Sponsor Grid.

## 5. EXECUTION PLAN
1. Scaffold Astro config, Tailwind config (include the specific colors), and i18n JSONs.
2. Build `Layout.astro` (Navbar, SK/EN switch, Footer).
3. Build the specific UI sections (`Hero.astro`, `NW200.astro`, `Highlights.astro`, `Machine.astro`, `Sponsors.astro`, `Contact.astro`) passing the specific data above.
4. Assemble `pages/index.astro` and `pages/en/index.astro`.
Do not output markdown talk. Output strict paths and code. Make it look brutal, raw, and fast.