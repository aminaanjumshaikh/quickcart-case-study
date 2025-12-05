# quickcart-case-study
 QuickCart – Grocery Delivery App Redesign (UI/UX Case Study)
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
