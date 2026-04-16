# ZENGA-stores-<!DOCTYPE html><html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Free Top Up</title>
<style>
body{font-family:Arial;background:#0f172a;color:white;margin:0}
header{background:#020617;padding:15px;text-align:center;font-size:26px;color:#22c55e}
.container{padding:15px}
.card{background:#1e293b;margin:10px 0;padding:15px;border-radius:10px}
button{background:#22c55e;border:none;padding:8px 12px;border-radius:5px;color:white;cursor:pointer;margin-top:5px}
.cart{position:fixed;top:10px;right:10px;background:#22c55e;padding:10px;border-radius:10px}
input{width:100%;padding:8px;margin:5px 0;border-radius:5px;border:none}
.item{display:flex;justify-content:space-between;margin:5px 0}
.remove{background:red}
.games{display:flex;gap:10px;overflow:auto}
.game img{width:60px;height:60px;border-radius:10px}
.hidden{display:none}
</style>
</head>
<body><header>🔥 FREE TOP UP 🔥</header>
<div class="cart">🛒 <span id="count">0</span></div><div class="container"><h2>🎮 Chwazi jwèt</h2>
<div class="games">
<div class="game" onclick="show('ff')"><img src="https://upload.wikimedia.org/wikipedia/en/6/6b/Garena_Free_Fire_logo.png"></div>
<div class="game" onclick="show('roblox')"><img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Roblox_Logo_2022.jpg"></div>
<div class="game" onclick="show('pubg')"><img src="https://upload.wikimedia.org/wikipedia/en/4/44/PUBG_Mobile_logo.png"></div>
</div><div id="ff" class="card hidden">
<h2>💎 Free Fire Diamonds</h2>
<div class="item">100💎 - 175 HTG <button onclick="add('100💎',175)">Ajouter</button></div>
<div class="item">200💎 - 350 HTG <button onclick="add('200💎',350)">Ajouter</button></div>
<div class="item">310💎 - 500 HTG <button onclick="add('310💎',500)">Ajouter</button></div>
<div class="item">520💎 - 825 HTG <button onclick="add('520💎',825)">Ajouter</button></div>
<div class="item">1060💎 - 1650 HTG <button onclick="add('1060💎',1650)">Ajouter</button></div>
<div class="item">2180💎 - 4000 HTG <button onclick="add('2180💎',4000)">Ajouter</button></div>
<div class="item">5600💎 - 8500 HTG <button onclick="add('5600💎',8500)">Ajouter</button></div>
</div><div id="roblox" class="card hidden">
<h2>🟥 Roblox</h2>
<div class="item">100 Robux - 580 HTG <button onclick="add('100 Robux',580)">Ajouter</button></div>
<div class="item">400 Robux - 1250 HTG <button onclick="add('400 Robux',1250)">Ajouter</button></div>
<div class="item">800 Robux - 1989 HTG <button onclick="add('800 Robux',1989)">Ajouter</button></div>
<div class="item">1700 Robux - 3800 HTG <button onclick="add('1700 Robux',3800)">Ajouter</button></div>
</div><div id="pubg" class="card hidden">
<h2>🔫 PUBG Mobile</h2>
<div class="item">60 UC - 250 HTG <button onclick="add('60 UC',250)">Ajouter</button></div>
<div class="item">120 UC - 390 HTG <button onclick="add('120 UC',390)">Ajouter</button></div>
<div class="item">325 UC - 997 HTG <button onclick="add('325 UC',997)">Ajouter</button></div>
<div class="item">660 UC - 1800 HTG <button onclick="add('660 UC',1800)">Ajouter</button></div>
<div class="item">1800 UC - 3900 HTG <button onclick="add('1800 UC',3900)">Ajouter</button></div>
</div><div class="card">
<h2>🛒 Panier</h2>
<div id="cartItems"></div>
<p>Total: <span id="total">0</span> HTG</p>
</div><div class="card">
<h2>🧾 Infos Client</h2>
<input id="name" placeholder="Non ou">
<input id="player" placeholder="ID jwèt ou">
</div><div class="card">
<h2>💳 Paiement</h2>
<p>NatCash sèlman: +50942956341</p>
<button onclick="checkout()">Payer via WhatsApp</button>
</div></div><script>
let cart=[];
function show(id){
document.querySelectorAll('.card').forEach(c=>c.classList.add('hidden'));
document.getElementById(id).classList.remove('hidden');
document.querySelectorAll('.card')[3].classList.remove('hidden');
document.querySelectorAll('.card')[4].classList.remove('hidden');
document.querySelectorAll('.card')[5].classList.remove('hidden');
}
function add(name,price){
cart.push({name,price});
render();
}
function remove(index){
cart.splice(index,1);
render();
}
function render(){
let html="";
let total=0;
cart.forEach((item,i)=>{
total+=item.price;
html+=`<div class='item'>${item.name} - ${item.price} HTG <button class='remove' onclick='remove(${i})'>X</button></div>`;
});
document.getElementById('cartItems').innerHTML=html;
document.getElementById('total').innerText=total;
document.getElementById('count').innerText=cart.length;
}
function checkout(){
let name=document.getElementById('name').value;
let player=document.getElementById('player').value;
let total=document.getElementById('total').innerText;
let message=`Bonjou, mwen vle achte:%0A`;
cart.forEach(item=>{message+=`- ${item.name} (${item.price} HTG)%0A`;});
message+=`Total: ${total} HTG%0ANon: ${name}%0AID: ${player}`;
window.open(`https://wa.me/50942956341?text=${message}`);
}
</script></body>
</html>
