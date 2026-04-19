<!DOCTYPE html><html lang="ar">
<head>
<meta charset="UTF-8">
<title>Active Plus</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {font-family: Arial; background:#f5f5f5; text-align:center;}
h1 {color:#0a7cff;}
.card {
  background:#fff;
  margin:15px;
  padding:15px;
  border-radius:15px;
}
button {
  background:green;
  color:#fff;
  padding:10px;
  border:none;
  border-radius:10px;
}
</style>
</head><body><h1>Active Plus للأجهزة والمستلزمات الطبية</h1>
<p>مدينة نصر - مصطفى النحاس</p><div class="card">
<h2>جهاز قياس الضغط</h2>
<p>450 جنيه</p>
<button onclick="addToCart('جهاز ضغط',450)">اضف للسلة</button>
</div><div class="card">
<h2>جهاز سكر</h2>
<p>300 جنيه</p>
<button onclick="addToCart('جهاز سكر',300)">اضف للسلة</button>
</div><h2>🛒 سلة المشتريات</h2>
<ul id="cart"></ul><button onclick="sendToWhatsApp()">اطلب الآن عبر واتساب</button>

<script>
let cart = [];

function addToCart(name, price){
  cart.push(name + " - " + price + " جنيه");
  let list = document.getElementById("cart");
  list.innerHTML = "";
  cart.forEach(item => {
    let li = document.createElement("li");
    li.textContent = item;
    list.appendChild(li);
  });
}

function sendToWhatsApp(){
  let message = "عايز اطلب:%0A" + cart.join("%0A");
  window.location.href = "https://wa.me/201022241533?text=" + message;
}
</script></body>
</html>
