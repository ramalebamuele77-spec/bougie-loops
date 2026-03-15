<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🧶 Crocheting Away</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">

<style>
/* ===== Reset ===== */
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family: 'Dancing Script', cursive; background: linear-gradient(135deg,#ffe4e1,#ffb6c1); color:#ff69b4; overflow:hidden; }
a { text-decoration:none; color:#ff69b4; }
button { cursor:pointer; font-family: inherit; }

/* ===== Header ===== */
header { text-align:center; padding:20px; background:#ffe4e1; border-bottom:3px dashed #ffb6c1; }
.logo { display:flex; justify-content:center; align-items:center; gap:10px; }
.logo .yarn-ball { font-size:50px; animation:bounce 1s infinite alternate; }
.subtitle { font-size:18px; color:#ff69b4; }

/* ===== Nav ===== */
nav { display:flex; flex-wrap:wrap; justify-content:center; gap:10px; background:#ffe4e1; padding:10px; border-bottom:3px dashed #ffb6c1; }
nav a { padding:5px 10px; border-radius:10px; transition: all .3s; }
nav a:hover { background:#ffb6c1; color:#fff; transform:scale(1.2); }

/* ===== Sections ===== */
section { display:none; padding:30px; text-align:center; }
section.active { display:block; }
.hero h2 { font-size:35px; margin-bottom:10px; animation:fadeIn 1s ease; }
.cute-btn { background:#ffb6c1; border:none; padding:12px 25px; border-radius:20px; font-size:18px; transition:.3s; box-shadow:0 5px 15px rgba(255,105,180,0.3); }
.cute-btn:hover { transform:scale(1.1); background:#ff69b4; color:#fff; box-shadow:0 10px 20px rgba(255,105,180,0.5); }

/* ===== Products ===== */
.products-grid { display:flex; flex-wrap:wrap; justify-content:center; gap:20px; }
.product-card { background:#fff0f5; border:2px dashed #ffb6c1; border-radius:20px; width:220px; text-align:center; padding:15px; transition:.3s; }
.product-card:hover { transform:scale(1.05); box-shadow:0 5px 20px rgba(255,105,180,0.3); }
.product-card img { width:100%; border-radius:15px; margin-bottom:10px; }

/* ===== Cart ===== */
#cart-items { list-style:none; padding:0; margin-bottom:15px; }
#cart-items li { margin:5px 0; background:#fff0f5; border:1px dashed #ffb6c1; border-radius:10px; padding:5px; animation:fadeIn 0.5s; }

/* ===== Gallery ===== */
.gallery-grid { display:flex; flex-wrap:wrap; gap:15px; justify-content:center; }
.gallery-grid img { width:200px; border-radius:15px; border:2px solid #ffb6c1; transition:.3s; }
.gallery-grid img:hover { transform:scale(1.1); box-shadow:0 10px 20px rgba(255,105,180,0.5); cursor:pointer; }

/* ===== Cards ===== */
.card { background:#fff0f5; border:2px dashed #ffb6c1; border-radius:15px; padding:15px; margin:10px; width:250px; display:inline-block; transition:.3s; }
.card:hover { transform:scale(1.05); box-shadow:0 10px 20px rgba(255,105,180,0.3); }

/* ===== Contact Form ===== */
.contact-form { display:flex; flex-direction:column; max-width:400px; margin:20px auto; gap:15px; }
.contact-form input, .contact-form textarea { padding:10px; border-radius:10px; border:2px dashed #ffb6c1; resize:none; }
.contact-form button { padding:12px; border-radius:15px; background:#ffb6c1; border:none; color:#fff; font-size:18px; transition:.3s; }
.contact-form button:hover { background:#ff69b4; transform:scale(1.05); }

/* ===== FAQ Accordion ===== */
.accordion { background:#ffb6c1; color:#fff; cursor:pointer; padding:12px 20px; width:100%; border:none; text-align:left; outline:none; transition:.3s; border-radius:10px; margin:5px 0; }
.accordion:hover { background:#ff69b4; }
.panel { padding:0 20px; display:none; background:#fff0f5; border-radius:10px; margin-bottom:10px; }

/* ===== Footer ===== */
footer { text-align:center; padding:20px; background:#ffe4e1; border-top:3px dashed #ffb6c1; }

/* ===== Stars ===== */
.star { color:#ff69b4; font-size:20px; margin-right:2px; }

/* ===== Animations ===== */
@keyframes addCartAnim {0%{transform:scale(1) rotate(0deg);opacity:1;}50%{transform:scale(1.5) rotate(20deg);opacity:0.7;}100%{transform:scale(1) rotate(0deg);opacity:1;}}
@keyframes bounce {0%{transform:translateY(0);}100%{transform:translateY(-10px);}}
@keyframes fadeIn {0%{opacity:0;}100%{opacity:1;}}

/* ===== Responsive ===== */
@media(max-width:768px){.products-grid, .gallery-grid{flex-direction:column; align-items:center;}}
</style>
</head>
<body>

<!-- ===== Header ===== -->
<header>
  <div class="logo"><div class="yarn-ball">🧶</div><h1>Crocheting Away</h1></div>
  <p class="subtitle">Handmade Crochet Creations 💖</p>
</header>

<!-- ===== Nav ===== -->
<nav>
  <a href="#" onclick="showSection('home')">Home</a>
  <a href="#" onclick="showSection('products')">Products</a>
  <a href="#" onclick="showSection('cart')">Cart</a>
  <a href="#" onclick="showSection('gallery')">Gallery</a>
  <a href="#" onclick="showSection('faq')">FAQ</a>
  <a href="#" onclick="showSection('blog')">Blog</a>
  <a href="#" onclick="showSection('reviews')">Reviews</a>
  <a href="#" onclick="showSection('contact')">Contact</a>
  <a href="#" onclick="showSection('custom-orders')">Custom Orders</a>
</nav>

<!-- ===== Sections ===== -->
<section id="home" class="active">
  <h2>Welcome to Your Cozy Crochet Shop!</h2>
  <p>Discover adorable handmade crochet items made with love 💕</p>
  <button class="cute-btn" onclick="showSection('products')">Shop Now</button>
</section>

<section id="products">
<h2>Our Crochet Items 🧵</h2>
<div class="products-grid">
<div class="product-card">
  <img src="https://via.placeholder.com/220.png?text=Plushie">
  <h3>Crochet Plushie</h3><p>R120</p>
  <button onclick="addToCart('Crochet Plushie',120)">Add to Cart</button>
  <button onclick="orderWhatsApp('Crochet Plushie')">Order WhatsApp</button>
</div>
<div class="product-card">
  <img src="https://via.placeholder.com/220.png?text=Bag">
  <h3>Crochet Bag</h3><p>R200</p>
  <button onclick="addToCart('Crochet Bag',200)">Add to Cart</button>
  <button onclick="orderWhatsApp('Crochet Bag')">Order WhatsApp</button>
</div>
<div class="product-card">
  <img src="https://via.placeholder.com/220.png?text=Hat">
  <h3>Crochet Hat</h3><p>R90</p>
  <button onclick="addToCart('Crochet Hat',90)">Add to Cart</button>
  <button onclick="orderWhatsApp('Crochet Hat')">Order WhatsApp</button>
</div>
</div>
</section>

<section id="cart">
<h2>🛍 Shopping Cart</h2>
<ul id="cart-items"></ul>
<h3>Total: R<span id="total">0</span></h3>
<button class="cute-btn" onclick="checkout()">Checkout via WhatsApp</button>
</section>

<section id="gallery">
<h2>Gallery 📸</h2>
<div class="gallery-grid">
<img src="https://via.placeholder.com/200.png?text=Plushie">
<img src="https://via.placeholder.com/200.png?text=Bag">
<img src="https://via.placeholder.com/200.png?text=Hat">
<img src="https://via.placeholder.com/200.png?text=Scarf">
<img src="https://via.placeholder.com/200.png?text=Blanket">
</div>
</section>

<section id="faq">
<h2>FAQ ❓</h2>
<button class="accordion">How long does shipping take?</button>
<div class="panel"><p>Shipping usually takes 3–5 business days.</p></div>
<button class="accordion">Can I request custom designs?</button>
<div class="panel"><p>Yes! Fill the custom orders form.</p></div>
<button class="accordion">How do I pay?</button>
<div class="panel"><p>All payments are via WhatsApp after checkout.</p></div>
</section>

<section id="blog">
<h2>Blog 📝</h2>
<div class="card"><h3>Top 5 Crochet Trends</h3><p>Discover the cutest crochet patterns 💕</p></div>
<div class="card"><h3>DIY Crochet Tips</h3><p>Simple techniques for cozy projects.</p></div>
<div class="card"><h3>Caring for Your Items</h3><p>Keep your handmade items soft and beautiful.</p></div>
</section>

<section id="reviews">
<h2>Reviews ⭐</h2>
<div class="card"><h3>Sarah W.</h3><p>★★★★★</p><p>"Absolutely adorable plushie!"</p></div>
<div class="card"><h3>Jessica M.</h3><p>★★★★★</p><p>"Beautiful crochet bag, fast WhatsApp order!"</p></div>
<div class="card"><h3>Emily T.</h3><p>★★★★☆</p><p>"Lovely crochet hat, soft and well crafted."</p></div>
</section>

<section id="contact">
<h2>Contact Us 💌</h2>
<form class="contact-form" onsubmit="alert('Message sent! 💖'); return false;">
<input type="text" placeholder="Your Name" required>
<input type="email" placeholder="Your Email" required>
<textarea placeholder="Your Message" rows="5" required></textarea>
<button type="submit">Send Message</button>
</form>
<p>Or message us on WhatsApp: <a href="https://wa.me/27721278697">072 127 8697</a></p>
</section>

<section id="custom-orders">
<h2>Custom Orders ✨</h2>
<form class="contact-form" onsubmit="alert('Custom order sent via WhatsApp! 💖'); return false;">
<input type="text" placeholder="Your Name" required>
<input type="email" placeholder="Your Email" required>
<textarea placeholder="Describe your order" rows="5" required></textarea>
<button type="submit" onclick="orderWhatsApp('Custom Order')">Send via WhatsApp</button>
</form>
</section>

<footer>
<p>© 2026 Crocheting Away | Designed with 💖</p>
</footer>

<script>
// ===== Section switching =====
function showSection(id){
  const sections=document.querySelectorAll('section');
  sections.forEach(sec=>sec.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

// ===== Cart =====
let cart=[], total=0;
function addToCart(itemName,price){
cart.push({itemName,price});
total+=price;
const li=document.createElement('li');
li.textContent=`${itemName} - R${price}`;
li.style.animation='addCartAnim 0.5s ease';
document.getElementById('cart-items').appendChild(li);
document.getElementById('total').textContent=total;
}
function checkout(){
if(cart.length===0){ alert("Your cart is empty!"); return; }
let message="Hi! I want to order:\n";
cart.forEach(item=>message+=`- ${item.itemName} : R${item.price}\n`);
message+=`Total: R${total}`;
window.open(`https://wa.me/27721278697?text=${encodeURIComponent(message)}`,'_blank');
cart=[]; total=0;
document.getElementById('cart-items').innerHTML=''; 
document.getElementById('total').textContent='0';
}
function orderWhatsApp(itemName){
window.open(`https://wa.me/27721278697?text=${encodeURIComponent("Hi! I want to order a "+itemName)}`,'_blank');
}

// ===== FAQ Accordion =====
document.addEventListener('DOMContentLoaded',function(){
const acc=document.getElementsByClassName("accordion");
for(let i=0;i<acc.length;i++){
acc[i].addEventListener("click",function(){
this.classList.toggle("active");
const panel=this.nextElementSibling;
panel.style.display=(panel.style.display==="block")?"none":"block";
});
}
});
</script>

</body>
</html>
