
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Smart Choice | Shop Smarter</title>
<meta name="description" content="Discover smart shopping recommendations, technology, fashion, home essentials and product comparisons.">

<style>
:root {
  --navy: #101d35;
  --gold: #d6ae58;
  --light: #f5f6f8;
  --white: #fff;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  font-family: Arial, sans-serif;
  background: var(--light);
  color: #263348;
  line-height: 1.6;
}
header {
  background: var(--navy);
  color: white;
  padding: 18px 6%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 15px;
}
.logo { font-size: 25px; font-weight: bold; }
.logo span { color: var(--gold); }
nav { display: flex; gap: 16px; flex-wrap: wrap; }
nav a { color: white; text-decoration: none; font-size: 14px; }
nav a:hover { color: var(--gold); }

.hero {
  background: linear-gradient(120deg,#101d35,#29496b);
  color: white;
  text-align: center;
  padding: 85px 20px;
}
.hero h1 { font-size: clamp(35px,6vw,58px); }
.hero h1 span { color: var(--gold); }
.hero p { max-width: 650px; margin: 15px auto 25px; }
.btn {
  display: inline-block;
  background: var(--gold);
  color: var(--navy);
  padding: 12px 22px;
  border: 0;
  border-radius: 5px;
  text-decoration: none;
  font-weight: bold;
  cursor: pointer;
}
.btn:hover { opacity: .85; }

.container { max-width: 1150px; margin: auto; padding: 55px 20px; }
.section-title { text-align: center; margin-bottom: 30px; }
.section-title h2 { color: var(--navy); font-size: 29px; }
.section-title p { color: #667085; }

.categories {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 15px;
}
.category {
  background: white;
  border-radius: 9px;
  padding: 23px 10px;
  text-align: center;
  text-decoration: none;
  color: var(--navy);
  font-weight: bold;
  box-shadow: 0 3px 12px #00000008;
}
.category span { display: block; font-size: 36px; }
.category:hover { outline: 2px solid var(--gold); }

.search-wrap { max-width: 600px; margin: 0 auto 25px; }
.search-wrap input {
  width: 100%;
  padding: 14px;
  border: 1px solid #ddd;
  border-radius: 6px;
  font-size: 16px;
}
.filters {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 9px;
  margin-bottom: 25px;
}
.filter {
  border: 1px solid #ddd;
  background: white;
  padding: 9px 15px;
  border-radius: 20px;
  cursor: pointer;
}
.filter.active { background: var(--navy); color: white; }

.products {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 22px;
}
.product {
  background: white;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 3px 15px #0000000c;
}
.product-image {
  height: 165px;
  display: grid;
  place-items: center;
  background: #e9edf3;
  font-size: 65px;
}
.product-info { padding: 20px; }
.product-info h3 { color: var(--navy); margin-bottom: 8px; }
.product-info p { color: #667085; font-size: 14px; margin-bottom: 15px; }
.product-info .btn { width: 100%; text-align: center; }
.pending { display: block; font-size: 12px; color: #94702c; margin-top: 8px; }
.no-results { text-align: center; padding: 25px; display: none; }

.info-section {
  background: white;
  padding: 35px;
  border-radius: 10px;
  margin-bottom: 25px;
  scroll-margin-top: 20px;
}
.info-section h2 { color: var(--navy); margin-bottom: 15px; }
.info-section p { margin-bottom: 12px; }
.info-section a { color: #92702e; }
.contact-form { display: grid; gap: 12px; max-width: 550px; }
.contact-form input, .contact-form textarea {
  padding: 13px;
  border: 1px solid #ddd;
  border-radius: 5px;
  font: inherit;
}
footer {
  background: var(--navy);
  color: white;
  padding: 35px 20px;
  text-align: center;
}
footer p { color: #d0d6df; font-size: 13px; margin: 8px; }
footer a { color: var(--gold); margin: 0 8px; text-decoration: none; }

@media(max-width:750px) {
  header { justify-content: center; text-align: center; }
  nav { justify-content: center; }
  .categories { grid-template-columns: repeat(2,1fr); }
  .products { grid-template-columns: repeat(2,1fr); }
}
@media(max-width:480px) {
  .products { grid-template-columns: 1fr; }
  .hero { padding: 60px 18px; }
  .info-section { padding: 23px; }
}
</style>
</head>

<body>

<header>
  <div class="logo">SMART <span>CHOICE.</span></div>
  <nav>
    <a href="#home">Home</a>
    <a href="#categories">Categories</a>
    <a href="#products">Products</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero" id="home">
  <h1>Make Smarter <span>Choices.</span></h1>
  <p>
    Discover useful products, explore shopping recommendations
    and find better ways to shop.
  </p>
  <a href="#products" class="btn">Explore Products</a>
</section>

<main>

<section class="container" id="categories">
  <div class="section-title">
    <h2>Explore Our Categories</h2>
    <p>Discover products for everyday life.</p>
  </div>

  <div class="categories">
    <a class="category" href="#products" onclick="chooseCategory('Technology')">
      <span>📱</span>Technology
    </a>
    <a class="category" href="#products" onclick="chooseCategory('Home')">
      <span>🏠</span>Home & Living
    </a>
    <a class="category" href="#products" onclick="chooseCategory('Fashion')">
      <span>👗</span>Fashion & Beauty
    </a>
    <a class="category" href="#products" onclick="chooseCategory('Deals')">
      <span>⭐</span>Best Deals
    </a>
  </div>
</section>

<section class="container" id="products">
  <div class="section-title">
    <h2>Featured Products</h2>
    <p>Explore our product recommendations.</p>
  </div>

  <div class="search-wrap">
    <input id="search" type="search"
      placeholder="Search products..."
      oninput="filterProducts()">
  </div>

  <div class="filters">
    <button class="filter active" onclick="chooseCategory('All',this)">All</button>
    <button class="filter" onclick="chooseCategory('Technology',this)">Technology</button>
    <button class="filter" onclick="chooseCategory('Home',this)">Home</button>
    <button class="filter" onclick="chooseCategory('Fashion',this)">Fashion</button>
    <button class="filter" onclick="chooseCategory('Deals',this)">Deals</button>
  </div>

  <div class="products" id="productGrid">

    <article class="product" data-category="Technology">
      <div class="product-image">🎧</div>
      <div class="product-info">
        <h3>Wireless Headphones</h3>
        <p>Explore wireless headphones for music, calls and everyday use.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Technology">
      <div class="product-image">⌚</div>
      <div class="product-info">
        <h3>Smart Watches</h3>
        <p>Discover smart watches with useful everyday features.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Technology">
      <div class="product-image">📱</div>
      <div class="product-info">
        <h3>Smartphones</h3>
        <p>Compare smartphones and explore different features.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Home">
      <div class="product-image">🍳</div>
      <div class="product-info">
        <h3>Air Fryers</h3>
        <p>Explore practical kitchen appliances for your home.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Home">
      <div class="product-image">🛋️</div>
      <div class="product-info">
        <h3>Home Furniture</h3>
        <p>Find inspiration for comfortable living spaces.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Fashion">
      <div class="product-image">👟</div>
      <div class="product-info">
        <h3>Fashion & Shoes</h3>
        <p>Explore everyday fashion and footwear options.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Fashion">
      <div class="product-image">💄</div>
      <div class="product-info">
        <h3>Beauty Essentials</h3>
        <p>Discover skincare and beauty products.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Deals">
      <div class="product-image">🛍️</div>
      <div class="product-info">
        <h3>Shopping Finds</h3>
        <p>Explore interesting products and shopping ideas.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

    <article class="product" data-category="Deals">
      <div class="product-image">⭐</div>
      <div class="product-info">
        <h3>Top Recommendations</h3>
        <p>Discover products worth comparing before buying.</p>
        <a class="btn affiliate-link" href="#contact">View Product</a>
        <span class="pending">Product link to be added</span>
      </div>
    </article>

  </div>
  <p class="no-results" id="noResults">No products found. Try another search.</p>
</section>

<section class="container" id="about">
  <div class="info-section">
    <h2>About Smart Choice</h2>
    <p>
      Smart Choice was created to make online shopping easier.
      We share shopping ideas, product recommendations and
      helpful information to help visitors make informed decisions.
    </p>
    <p>
      Our categories include technology, home and living,
      fashion, beauty and everyday essentials.
    </p>
    <p><strong>Our mission:</strong> Help people make smarter choices.</p>
  </div>

  <div class="info-section">
    <h2>Why Shop With Smart Choice?</h2>
    <p>✓ Helpful product discovery.</p>
    <p>✓ Easy-to-explore categories.</p>
    <p>✓ Shopping inspiration.</p>
    <p>✓ Product information to support better decisions.</p>
  </div>
</section>

<section class="container" id="contact">
  <div class="info-section">
    <h2>Contact Us</h2>
    <p>Have a question, suggestion or business enquiry?</p>
    <p>Email: <a href="mailto:YOUR_EMAIL@example.com">YOUR_EMAIL@example.com</a></p>
    <p>Replace the example email with your real business email.</p>
  </div>

  <div class="info-section" id="disclosure">
    <h2>Affiliate Disclosure</h2>
    <p>
      Smart Choice may participate in affiliate marketing programmes.
      Some links may be affiliate links, meaning we may earn a
      commission when visitors make qualifying purchases through them,
      at no additional cost to the customer.
    </p>
    <p>
      We aim to be transparent about our affiliate relationships.
    </p>
  </div>

  <div class="info-section" id="privacy">
    <h2>Privacy Policy</h2>
    <p>
      Smart Choice respects the privacy of its visitors.
      Our website may use cookies and similar technologies
      to improve the visitor experience and understand website traffic.
    </p>
    <p>
      Third-party advertising and affiliate partners may use cookies
      or similar technologies to measure advertising performance,
      display advertisements and track referrals.
    </p>
    <p>
      Where required, visitors will be provided with appropriate
      cookie consent options.
    </p>
    <p>
      For privacy questions, contact us using the email address
      listed above.
    </p>
    <p>Last updated: November 2026.</p>
  </div>

</section>

</main>

<footer>
  <div class="logo">SMART <span>CHOICE.</span></div>
  <p>Make smarter choices. Discover better deals.</p>
  <p>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
    <a href="#privacy">Privacy Policy</a>
    <a href="#disclosure">Affiliate Disclosure</a>
  </p>
  <p>© <span id="year"></span> Smart Choice. All rights reserved.</p>
</footer>

<script>
let currentCategory = "All";

function chooseCategory(category, button) {
  currentCategory = category;

  document.querySelectorAll(".filter").forEach(b =>
    b.classList.remove("active")
  );

  if (button) {
    button.classList.add("active");
  } else {
    document.querySelectorAll(".filter").forEach(b => {
      if (b.textContent.trim() === category) {
        b.classList.add("active");
      }
    });
  }

  filterProducts();
}

function filterProducts() {
  const search = document.getElementById("search")
    .value.toLowerCase().trim();

  const products = document.querySelectorAll(".product");
  let visible = 0;

  products.forEach(product => {
    const category = product.dataset.category;
    const text = product.textContent.toLowerCase();

    const categoryMatch =
      currentCategory === "All" ||
      category === currentCategory;

    const searchMatch = text.includes(search);

    const show = categoryMatch && searchMatch;
    product.style.display = show ? "block" : "none";

    if (show) visible++;
  });

  document.getElementById("noResults").style.display =
    visible ? "none" : "block";
}

document.getElementById("year").textContent =
  new Date().getFullYear();
</script>

</body>
</html>
