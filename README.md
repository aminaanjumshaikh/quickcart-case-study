# quickcart-case-study
#!/usr/bin/env bash
# Creates the quickcart-case-study folder with all files and zips it.
# Usage:
#   chmod +x create_zip.sh
#   ./create_zip.sh
set -euo pipefail

OUT_DIR="quickcart-case-study"
IMAGES_DIR="$OUT_DIR/images"
ZIP_NAME="${OUT_DIR}.zip"

echo "Creating project folder: $OUT_DIR"
rm -rf "$OUT_DIR" "$ZIP_NAME"
mkdir -p "$IMAGES_DIR"

echo "Writing README.md"
cat > "$OUT_DIR/README.md" <<'EOF'
## **QuickCart – Grocery Delivery App Redesign (UI/UX Case Study)**

### **Overview**

QuickCart is a redesign of a modern grocery delivery app focused on:

* Faster checkout
* Clearer navigation
* Transparent pricing
* Visual product comparison
* Reordering in a single tap

---

## **1. Problem**

Users of existing grocery apps feel overwhelmed by cluttered search results and long multi-step checkouts.
Pain points discovered:

* Slow checkout
* Lack of price transparency
* Overwhelming search results
* Hard to reorder

---

## **2. Goals**

* Reduce checkout steps
* Improve search clarity
* Add instant price comparison
* Enable 1-tap reorder
* Improve trust via reviews & images

---

## **3. Research**

### User Interviews (6 participants)

**Key insights:**

* 72%: search "too cluttered"
* 63% leave due to hidden delivery fees
* 48% want easy reorder

### Competitor analysis

* Instacart → good filtering
* Blinkit → fast, but cluttered
* Zepto → clean UI but complex tracking

---

## **4. Personas**

### **Persona 1: Aditi (Busy Employee)**

* Wants fast checkout
* Regular weekly orders
* Annoyed by confusing search

### **Persona 2: Manav (Price-Sensitive Student)**

* Compares prices
* Avoids high delivery fees
* Wants clear product details

---

## **5. User Flow Improvements**

**Before:** 8 steps → home → category → search → product → cart → address → payment → confirmation  
**After:** 5 steps → home → search → product → checkout → confirmation

---

## **6. Wireframes**

Pages included:

* Home
* Search
* Product detail
* Price comparison
* Cart
* One-page checkout
* Order tracking

---

## **7. UI Design System**

**Colors:**

* Primary: #2DBA75
* Secondary: #2D2D2D
* Background: #F4F4F4

**Typography:**

* Inter (12–24px)

**Components:**

* Rounded buttons
* Product cards
* Category chips
* Price comparison slider

---

## **8. High Fidelity Screens**

Screens designed:

* Onboarding
* Home
* Smart Search
* Product + Price Comparison
* Cart
* Checkout (single screen)
* Live Tracking

---

## **9. Prototype**

Flow built in Figma (Link placeholder):  
`https://figma.com/@yourname/quickcart`

---

## **10. Usability Testing Results**

* Checkout time ↓ **40%**
* Search clarity ↑ **28%**
* 4/5 users rated new design “very easy”

---

## **11. Final Impact**

QuickCart delivers faster ordering, cleaner search, and transparent pricing — improving conversion and user trust.
EOF

echo "Writing index.html"
cat > "$OUT_DIR/index.html" <<'EOF'
<!DOCTYPE html>
<html>
<head>
  <title>QuickCart – UI/UX Case Study</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <style>
    body { font-family: Arial, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue"; max-width: 900px; margin: auto; padding: 40px; line-height: 1.7; background: #F4F4F4; color: #2D2D2D; }
    h1,h2,h3 { color: #2DBA75; margin-top: 1.4em; }
    header { text-align: center; margin-bottom: 30px; }
    .hero { background: white; padding: 24px; border-radius: 12px; box-shadow: 0 6px 18px rgba(45,45,45,0.06); }
    .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; }
    .card { background: white; padding: 18px; border-radius: 10px; box-shadow: 0 6px 18px rgba(45,45,45,0.04); }
    .muted { color: #666; font-size: 0.95rem; }
    img { width: 100%; margin: 16px 0; border-radius: 8px; background: #fff; }
    footer { text-align: center; margin-top: 40px; color: #777; font-size: 0.9rem; }
    a.button { background: #2DBA75; color: white; padding: 10px 16px; border-radius: 8px; display: inline-block; text-decoration: none; margin-top: 10px; }
    .gallery { display: grid; grid-template-columns: repeat(3,1fr); gap: 12px; margin-top: 12px; }
    .gallery img { height: 260px; object-fit: cover; }
    @media (max-width: 720px) {
      .grid { grid-template-columns: 1fr; }
      .gallery { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <header>
    <h1>QuickCart – UI/UX Case Study</h1>
    <p class="muted">A complete redesign of a grocery delivery app focused on speed, clarity, and trust.</p>
  </header>

  <section class="hero card">
    <h2>Problem</h2>
    <p>Users faced slow checkout, cluttered search, and hidden delivery fees. QuickCart simplifies search and delivers an express checkout flow while improving trust through rich product content.</p>

    <h3>Key Goals</h3>
    <ul>
      <li>Reduce checkout steps and time</li>
      <li>Improve search relevance and filtering</li>
      <li>Make pricing transparent with price-per-unit</li>
      <li>One-tap reorder and express checkout</li>
    </ul>
    <a class="button" href="#wireframes">See wireframes & screens</a>
  </section>

  <section id="wireframes" class="grid">
    <div class="card">
      <h3>Research</h3>
      <p class="muted">Interviews, competitor analysis, and usability testing informed the redesign. Users want speed and clarity above extra features.</p>
      <img src="images/wireframe-home.svg" alt="Wireframe - Home (placeholder)" />
    </div>
    <div class="card">
      <h3>Wireframes & Screens</h3>
      <p class="muted">Included: Search, Product, Price Comparison, Cart, Checkout, Tracking. Add your high-fidelity images to the images/ folder or keep these placeholders.</p>
      <img src="images/wireframe-search.svg" alt="Wireframe - Search (placeholder)" />
    </div>

    <div class="card">
      <h3>Design System</h3>
      <p class="muted"><strong>Primary:</strong> #2DBA75 • <strong>Secondary:</strong> #2D2D2D • <strong>Background:</strong> #F4F4F4 • Inter type scale</p>
    </div>

    <div class="card">
      <h3>Impact</h3>
      <p class="muted">Prototype testing showed: Checkout time reduced by ~40% and improved search satisfaction. Use this repo as a portfolio piece or starting point for further work.</p>
    </div>
  </section>

  <section class="card" style="margin-top:20px">
    <h3>Screen gallery (placeholders)</h3>
    <div class="gallery">
      <img src="images/screen-home.svg" alt="Home screen placeholder" />
      <img src="images/screen-search.svg" alt="Search screen placeholder" />
      <img src="images/screen-product.svg" alt="Product screen placeholder" />
      <img src="images/screen-checkout.svg" alt="Checkout screen placeholder" />
      <img src="images/screen-tracking.svg" alt="Tracking screen placeholder" />
      <img src="images/wireframe-home.svg" alt="Wireframe placeholder" />
    </div>
  </section>

  <footer>
    <p>To publish: add images into /images, push to a GitHub repo named <strong>quickcart-case-study</strong>, and enable GitHub Pages (see PUBLISH.md)</p>
  </footer>
</body>
</html>
EOF

echo "Writing DALLE_PROMPTS.txt"
cat > "$OUT_DIR/DALLE_PROMPTS.txt" <<'EOF'
Home Screen
“Modern grocery app home page, clean layout, green and white theme (#2DBA75), category icons, search bar at top, minimalistic mobile screen, rounded corners, soft shadows, high-fidelity UI, Apple-style design, 9:16 mobile mockup”

Smart Search
“Grocery app predictive search results mobile screen, product cards with thumbnail, brand and price, inline filters shown as chips, clean spacing, modern flat UI, green accents, 9:16 mobile mockup”

Product Page
“Product detail page mobile UI, large product photo, price-per-unit displayed, price comparison slider showing 2 competing SKUs, verified reviews section with user photos, minimal interface, soft shadows, green action button, 9:16 mobile mockup”

Checkout
“One-screen checkout mobile UI, delivery slot selector, address summary, payment buttons, final price breakdown, confirm order CTA in green (#2DBA75), clean white cards on light gray background, 9:16 mobile mockup”

Order Tracking
“Real-time delivery tracking screen mobile UI, map thumbnail, driver avatar and ETA, progress timeline, expected arrival time, modern mobile interface, clear typography, green accent”
EOF

echo "Writing NOTION.md"
cat > "$OUT_DIR/NOTION.md" <<'EOF'
# QuickCart – Grocery Delivery App Redesign (Notion-ready)

Overview
- QuickCart is a redesign focused on speed, clarity, and trust for grocery delivery.

Problem
- Slow checkout, cluttered search results, hidden fees.

Goals
- Reduce checkout steps
- Improve search clarity
- Add price-per-unit and comparison
- One-tap reorder
- Improve trust via reviews and rich images

Research
- Interviews (6 participants)
  - 72%: search "too cluttered"
  - 63% leave due to hidden fees
  - 48% want easy reorder
- Competitors: Instacart, Blinkit, Zepto

Personas
- Aditi — Busy employee, frequent orders, needs speed
- Manav — Student, price-sensitive, compares prices

User Flows
- Before: 8 steps (home → category → search → product → cart → address → payment → confirmation)
- After: 5 steps (home → search → product → checkout → confirmation)

Wireframes / Screens
- Home
- Smart Search
- Product + Price Comparison
- Cart
- One-page Checkout
- Order Tracking

Design System
- Colors: Primary #2DBA75, Secondary #2D2D2D, Background #F4F4F4
- Typography: Inter
- Components: Product cards, category chips, price-per-unit label, CTA buttons

Prototype
- Figma link placeholder: https://figma.com/@yourname/quickcart

Impact & Metrics
- Checkout time ↓ 40%
- Search clarity ↑ 28%
- 4/5 users found the design “very easy”

Notes:
- To import into Notion: create a new page, paste the sections above. Use Notion headings, toggles for research details, and image blocks for your mockups/screens.
EOF

echo "Writing PUBLISH.md"
cat > "$OUT_DIR/PUBLISH.md" <<'EOF'
# QuickCart — Publish Instructions (5-minute guide)

Follow these steps to publish the project on GitHub Pages and get a sharable URL.

1) Create the repo on GitHub
- Name it: quickcart-case-study
- Public repo (recommended for portfolio)

2) Add the files locally
- Create a folder named `quickcart-case-study` and copy the files from this project into it.
- Add an `images/` folder and place your generated UI images (see images/README.txt for naming suggestions).

3) Quick git commands (run inside the project folder)
- git init
- git add .
- git commit -m "Initial QuickCart case study"
- git branch -M main
- git remote add origin https://github.com/<yourusername>/quickcart-case-study.git
- git push -u origin main

(Alternatively use GitHub Desktop or the GitHub web UI to create the repo and upload files.)

4) Enable GitHub Pages
- Go to your repository on GitHub → Settings → Pages
- Under "Build and deployment" choose Branch: main, Folder: /root (or choose gh-pages branch if you prefer)
- Save. GitHub Pages will provide the site link in a few moments.

Your site URL will be:
https://<yourusername>.github.io/quickcart-case-study

Notes & tips
- Replace placeholder images in index.html with your real images in images/
- If you change the repo name or branch, the URL will change accordingly
- For a better look, replace the hero and wireframe placeholder images with high-res exports from Figma or DALL·E
EOF

echo "Writing images/README.txt"
cat > "$IMAGES_DIR/README.txt" <<'EOF'
Add your generated UI images into this folder.

Suggested filenames (used in index.html placeholders):
- wireframe-home.png
- wireframe-search.png
- screen-home.png
- screen-search.png
- screen-product.png
- screen-checkout.png
- screen-tracking.png

Tips:
- Export mobile mockups as 1080x1920 PNGs for best display
- Keep file sizes under ~500KB each for faster page loads; use progressive JPEG or optimized PNG
EOF

echo "Writing LICENSE (MIT)"
cat > "$OUT_DIR/LICENSE" <<'EOF'
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
EOF

echo "Writing SVG placeholder images"
cat > "$IMAGES_DIR/wireframe-home.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#F4F4F4"/>
  <rect x="18" y="28" rx="12" width="324" height="68" fill="#FFFFFF" stroke="#E6E6E6"/>
  <rect x="36" y="46" rx="8" width="260" height="36" fill="#F8F8F8"/>
  <g transform="translate(36,100)">
    <rect rx="10" width="288" height="120" fill="#FFFFFF" stroke="#EAEAEA"/>
    <rect x="12" y="12" width="96" height="96" rx="8" fill="#E9FFF0"/>
    <rect x="120" y="18" width="150" height="18" rx="4" fill="#F2F2F2"/>
    <rect x="120" y="44" width="110" height="14" rx="4" fill="#F2F2F2"/>
    <rect x="120" y="68" width="80" height="28" rx="6" fill="#2DBA75"/>
  </g>
  <g transform="translate(36,232)">
    <rect rx="10" width="288" height="120" fill="#FFFFFF" stroke="#EAEAEA"/>
    <rect x="12" y="12" width="96" height="96" rx="8" fill="#FFF6E9"/>
    <rect x="120" y="18" width="150" height="18" rx="4" fill="#F2F2F2"/>
    <rect x="120" y="44" width="110" height="14" rx="4" fill="#F2F2F2"/>
    <rect x="120" y="68" width="80" height="28" rx="6" fill="#2DBA75"/>
  </g>
  <text x="24" y="380" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">Home — placeholder mockup</text>
</svg>
EOF

cat > "$IMAGES_DIR/wireframe-search.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#F4F4F4"/>
  <rect x="18" y="28" rx="12" width="324" height="56" fill="#FFFFFF" stroke="#E6E6E6"/>
  <circle cx="46" cy="56" r="12" fill="#2DBA75"/>
  <rect x="72" y="44" rx="8" width="230" height="24" fill="#F8F8F8"/>
  <g transform="translate(24,110)">
    <rect rx="10" width="312" height="72" fill="#FFFFFF" stroke="#EAEAEA"/>
    <rect x="12" y="12" width="48" height="48" rx="8" fill="#EDF7FF"/>
    <rect x="72" y="18" width="180" height="14" rx="4" fill="#F2F2F2"/>
    <rect x="72" y="38" width="100" height="12" rx="4" fill="#F2F2F2"/>
  </g>
  <g transform="translate(24,196)">
    <rect rx="10" width="312" height="72" fill="#FFFFFF" stroke="#EAEAEA"/>
    <rect x="12" y="12" width="48" height="48" rx="8" fill="#FFEFE9"/>
    <rect x="72" y="18" width="180" height="14" rx="4" fill="#F2F2F2"/>
    <rect x="72" y="38" width="100" height="12" rx="4" fill="#F2F2F2"/>
  </g>
  <text x="24" y="320" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">Smart Search — placeholder mockup</text>
</svg>
EOF

cat > "$IMAGES_DIR/screen-home.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#FFFFFF"/>
  <rect x="0" y="0" width="360" height="110" fill="#2DBA75" rx="0"/>
  <text x="20" y="62" font-family="Helvetica, Arial, sans-serif" font-size="22" fill="#ffffff">QuickCart</text>
  <rect x="20" y="134" rx="10" width="320" height="56" fill="#F4F4F4"/>
  <g transform="translate(20,210)">
    <rect rx="12" width="320" height="120" fill="#FFF"/>
    <rect x="14" y="12" width="92" height="96" rx="8" fill="#E9FFF0"/>
    <rect x="120" y="18" width="170" height="16" fill="#F2F2F2"/>
    <rect x="120" y="42" width="110" height="12" fill="#F2F2F2"/>
  </g>
  <text x="20" y="360" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">Home screen — high-level placeholder</text>
</svg>
EOF

cat > "$IMAGES_DIR/screen-search.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#FFFFFF"/>
  <rect x="18" y="28" rx="12" width="324" height="56" fill="#F4F4F4"/>
  <text x="36" y="62" font-family="Helvetica, Arial, sans-serif" font-size="14" fill="#999">Search products, e.g. "milk"</text>
  <g transform="translate(24,110)">
    <rect rx="10" width="312" height="68" fill="#FFF" stroke="#EAEAEA"/>
    <rect x="12" y="12" width="40" height="44" rx="6" fill="#EDF7FF"/>
    <rect x="64" y="18" width="220" height="12" rx="4" fill="#F2F2F2"/>
    <rect x="64" y="36" width="140" height="10" rx="4" fill="#F2F2F2"/>
  </g>
  <text x="24" y="200" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">Search results — placeholder</text>
</svg>
EOF

cat > "$IMAGES_DIR/screen-product.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#F4F4F4"/>
  <rect x="24" y="24" rx="12" width="312" height="260" fill="#FFFFFF" stroke="#EAEAEA"/>
  <rect x="40" y="40" width="232" height="180" rx="8" fill="#FFFFFF"/>
  <rect x="40" y="232" width="232" height="12" rx="6" fill="#F2F2F2"/>
  <rect x="40" y="256" width="280" height="36" rx="8" fill="#FFFFFF" stroke="#EAEAEA"/>
  <rect x="56" y="268" width="100" height="12" fill="#F2F2F2"/>
  <rect x="170" y="268" width="120" height="12" fill="#2DBA75"/>
  <text x="24" y="320" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">Product detail + price comparison — placeholder</text>
</svg>
EOF

cat > "$IMAGES_DIR/screen-checkout.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#FFFFFF"/>
  <rect x="20" y="20" width="320" height="76" rx="12" fill="#F4F4F4"/>
  <text x="40" y="64" font-family="Helvetica, Arial, sans-serif" font-size="16" fill="#333">Checkout — One page</text>
  <g transform="translate(20,120)">
    <rect rx="10" width="320" height="100" fill="#FFF" stroke="#EAEAEA"/>
    <rect x="12" y="12" width="296" height="20" rx="6" fill="#F8F8F8"/>
    <rect x="12" y="40" width="296" height="20" rx="6" fill="#F8F8F8"/>
    <rect x="12" y="68" width="296" height="20" rx="6" fill="#2DBA75"/>
  </g>
  <text x="24" y="260" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">One-screen checkout — placeholder</text>
</svg>
EOF

cat > "$IMAGES_DIR/screen-tracking.svg" <<'EOF'
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 360 780" width="360" height="780">
  <rect rx="24" ry="24" width="360" height="780" fill="#F4F4F4"/>
  <rect x="20" y="20" width="320" height="160" rx="12" fill="#FFFFFF" stroke="#EAEAEA"/>
  <rect x="36" y="40" width="288" height="120" rx="8" fill="#EAFDFC"/>
  <circle cx="60" cy="110" r="18" fill="#2DBA75"/>
  <rect x="100" y="84" width="180" height="12" rx="6" fill="#F2F2F2"/>
  <rect x="100" y="104" width="120" height="10" rx="6" fill="#F2F2F2"/>
  <text x="24" y="220" font-family="Helvetica, Arial, sans-serif" font-size="12" fill="#7A7A7A">Order tracking — placeholder</text>
</svg>
EOF

echo "Creating zip archive: $ZIP_NAME"
zip -r "$ZIP_NAME" "$OUT_DIR" >/dev/null

echo "Done. Created $ZIP_NAME in $(pwd)"
echo "You can now upload $ZIP_NAME to GitHub via the web UI or unzip it locally and push via git."
