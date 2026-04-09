# new-site
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Emerald Root Hemp</title>

<style>
body {font-family: Arial; margin:0; background:#f4f8f2;}
header {background:#1f4d2b; color:white; text-align:center; padding:20px;}
nav {background:#2f6d3c; padding:10px; text-align:center;}
nav a {color:white; margin:10px; text-decoration:none; font-weight:bold;}
section {padding:30px; display:none;}
.active {display:block;}
.products {display:flex; gap:20px; flex-wrap:wrap;}
.product {background:white; padding:15px; border-radius:10px; width:220px;}
button {background:#1f4d2b; color:white; border:none; padding:10px; cursor:pointer;}
footer {background:#1f4d2b; color:white; text-align:center; padding:20px;}
#cart {position:fixed; top:10px; right:10px; background:white; padding:10px; border-radius:10px;}
</style>

<script>
let cart = [];

function showPage(page) {
  document.querySelectorAll("section").forEach(s => s.classList.remove("active"));
  document.getElementById(page).classList.add("active");
}

function addToCart(name) {
  cart.push(name);
  document.getElementById("cartCount").innerText = cart.length;
}

function viewCart() {
  alert("Cart Items:\n" + cart.join("\n"));
}
</script>
</head>

<body>

<header>
<h1>Emerald Root Hemp</h1>
<p>Pure Plant. Clear Mind. Honest Growth.</p>
</header>

<nav>
<a onclick="showPage('home')">Home</a>
<a onclick="showPage('products')">Products</a>
<a onclick="showPage('about')">About</a>
<a onclick="showPage('contact')">Contact</a>
</nav>

<div id="cart">
🛒 <span id="cartCount">0</span> items  
<button onclick="viewCart()">View</button>
</div>

<section id="home" class="active">
<h2>Welcome</h2>
<p>Premium hemp products grown sustainably and lab-tested for quality.</p>
</section>

<section id="products">
<h2>Products</h2>

<div class="products">
<div class="product">
<h3>CBD Oil</h3>
<p>$39.99</p>
<button onclick="addToCart('CBD Oil')">Add to Cart</button>
</div>

<div class="product">
<h3>Hemp Flower</h3>
<p>$29.99</p>
<button onclick="addToCart('Hemp Flower')">Add to Cart</button>
</div>

<div class="product">
<h3>Hemp Cream</h3>
<p>$24.99</p>
<button onclick="addToCart('Hemp Cream')">Add to Cart</button>
</div>
</div>

</section>

<section id="about">
<h2>About Us</h2>
<p>We are committed to transparency, sustainability, and high-quality hemp products.</p>
</section>

<section id="contact">
<h2>Contact</h2>
<form onsubmit="event.preventDefault(); alert('Message sent!');">
<input type="text" placeholder="Name" required><br><br>
<input type="email" placeholder="Email" required><br><br>
<textarea placeholder="Message" required></textarea><br><br>
<button type="submit">Send</button>
</form>
</section>

<footer>
<p>© 2026 Emerald Root Hemp</p>
<p><small>Disclaimer: These products are not intended to diagnose, treat, cure, or prevent any disease.</small></p>
</footer>

</body>
</html>
