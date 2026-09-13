<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>MAA ARANAYA ENTERPRISES - Electrical Wholesale & Retail</title>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@600;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Plus Jakarta Sans',sans-serif}
body{background:#f1f5f9;color:#0f172a}
.header{background:#0f4da8;color:white;padding:12px 18px;display:flex;justify-content:space-between;align-items:center;position:sticky;top:0;z-index:99}
.logo{font-weight:900;font-size:18px;line-height:1.1}.logo span{color:#facc15}
.btn{padding:10px 18px;border-radius:100px;border:none;font-weight:800;cursor:pointer}
.btn-y{background:#facc15;color:#000}.btn-b{background:#0f4da8;color:white}
.hero{background:linear-gradient(90deg,#0f172a 0%,#1e40af 100%);color:white;padding:28px 18px;display:grid;grid-template-columns:1.2fr.8fr;gap:16px}
@media(max-width:700px){.hero{grid-template-columns:1fr}}
.card{background:white;border-radius:18px;padding:16px;box-shadow:0 4px 14px rgba(0,0,0,.06);border:1px solid #e2e8f0}
.cat-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:12px}
.prod-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:14px}
.price-w{color:#16a34a;font-weight:800}.price-r{color:#64748b;text-decoration:line-through;font-size:12px}
.toggle{display:flex;background:#e2e8f0;border-radius:100px;padding:4px;width:fit-content}
.toggle div{padding:8px 18px;border-radius:100px;cursor:pointer;font-weight:800;font-size:12px}
.toggle.active{background:#0f4da8;color:white}
.cart-bar{position:fixed;bottom:0;left:0;right:0;background:#0f172a;color:white;padding:12px 18px;display:flex;justify-content:space-between;align-items:center;z-index:100}
</style>
</head>
<body>
<div class="header">
<div class="logo"><i class="fa-solid fa-bolt" style="color:#facc15"></i> MAA ARANAYA<br><span>ENTERPRISES</span></div>
<div style="display:flex;gap:8px;align-items:center"><span style="font-size:12px" id="modeLabel">Retail Mode</span><div class="toggle" onclick="toggleMode()"><div id="tR" class="active">Retail</div><div id="tW">Wholesale</div></div><button class="btn btn-y" onclick="document.getElementById('contact').scrollIntoView()">Get Quote</button></div>
</div>
<div class="hero">
<div>
<div style="background:#facc15;color:#000;display:inline-block;padding:4px 12px;border-radius:20px;font-size:11px;font-weight:800">GST INVOICED • BIS CERTIFIED • 10,000+ Electricians</div>
<h1 style="font-size:32px;margin-top:12px;line-height:1.1">Powering India's<br>Electrical Needs</h1>
<p style="opacity:.8;margin-top:10px;font-size:13px">Wholesale pricing for electricians, contractors & retailers. Retail for home owners. Bulk discounts up to 25% + Same day delivery.</p>
<div style="margin-top:16px;display:flex;gap:10px"><button class="btn btn-y" onclick="document.getElementById('products').scrollIntoView()">Shop Now →</button><button class="btn" style="background:rgba(255,255,255,.15);color:white;border:1px solid rgba(255,255,255,.3)">Download Catalogue</button></div>
</div>
<div class="card" style="background:#fff;color:#000"><h3><i class="fa-solid fa-calculator"></i> Bulk Price Calculator</h3><p style="font-size:12px;color:#64748b;margin-top:4px">Enter qty to see wholesale saving</p><select id="calcProd" style="width:100%;margin-top:10px;padding:10px;border-radius:10px"><option value="485|620">Havells MCB 32A - W ₹485 / R ₹620</option><option value="2250|2750">Finolex Cable 2.5mm - W ₹2250 / R ₹2750</option><option value="72|95">LED Bulb 12W - W ₹72 / R ₹95</option></select><input id="calcQty" type="number" value="50" style="width:100%;margin-top:8px;padding:10px;border-radius:10px;border:1px solid #e2e8f0"><div id="calcOut" style="margin-top:10px;background:#f0fdf4;padding:12px;border-radius:12px;font-weight:800"></div></div>
</div>
<div style="padding:18px">
<h2 style="margin-bottom:12px">Shop by Category</h2>
<div class="cat-grid">
<div class="card" style="text-align:center"><i class="fa-solid fa-bolt" style="font-size:28px;color:#0f4da8"></i><div style="font-weight:800;margin-top:6px">MCBs</div><small>Min 15% Off Wholesale</small></div>
<div class="card" style="text-align:center"><i class="fa-solid fa-plug" style="font-size:28px;color:#0f4da8"></i><div style="font-weight:800;margin-top:6px">Cables & Wires</div><small>Copper • Aluminium</small></div>
<div class="card" style="text-align:center"><i class="fa-solid fa-lightbulb" style="font-size:28px;color:#0f4da8"></i><div style="font-weight:800;margin-top:6px">LED Lighting</div><small>Bulbs • Panels</small></div>
<div class="card" style="text-align:center"><i class="fa-solid fa-table-cells-large" style="font-size:28px;color:#0f4da8"></i><div style="font-weight:800;margin-top:6px">Distribution Boards</div><small>SPN • TPN • IP65</small></div>
</div>
<h2 id="products" style="margin:20px 0 12px">Featured Products — <span id="priceTitle">Retail Pricing</span></h2>
<div class="prod-grid" id="prodGrid"></div>
<div id="contact" class="card" style="margin-top:20px;background:#0f172a;color:white">
<h2 style="color:#facc15">Contact MAA ARANAYA ENTERPRISES</h2>
<p style="font-size:13px;margin-top:8px">📍 Surajgarha, Bihar + Howrah, West Bengal<br>📧 support@maaranaya.com<br>📞 +91 98765 43210<br>GSTIN: 19AABCM1224F125 | Mon-Sat 9AM-8PM</p>
<div style="margin-top:12px;display:flex;gap:10px"><button class="btn btn-y" onclick="whatsapp()">WhatsApp Order</button><button class="btn" style="background:white;color:black">Call Now</button></div>
</div>
<div style="height:80px"></div>
</div>
<div class="cart-bar"><div><span id="cartCount">0</span> items • <span id="cartTotal">₹0</span> <small id="saving" style="color:#22c55e"></small></div><button class="btn btn-y" onclick="whatsapp()">Order on WhatsApp <i class="fa-brands fa-whatsapp"></i></button></div>
<script>
let mode='retail';let cart=[];
let products=[
{name:"Havells 32A Four Pole MCB",w:485,r:620,unit:"/pc",img:"⚡"},
{name:"Finolex 2.5sqmm Copper Cable 90m",w:2250,r:2750,unit:"/roll",img:"🔌"},
{name:"12W LED Bulb Cool White",w:72,r:95,unit:"/pc",img:"💡"},
{name:"8 Way SPN Distribution Board",w:1150,r:1450,unit:"/pc",img:"📦"},
{name:"Anchor Penta Switch 10A",w:38,r:55,unit:"/pc",img:"🔘"},
{name:"PVC Conduit Pipe 25mm",w:120,r:165,unit:"/3m",img:"🛠️"}
];
function render(){
let grid=document.getElementById('prodGrid');grid.innerHTML='';
products.forEach((p,i)=>{
let price = mode=='wholesale'?p.w:p.r;
let mrp = mode=='wholesale'?p.r:p.w;
let save = mode=='wholesale'?`Save ₹${p.r-p.w}`:`Retail`;
grid.innerHTML+=`<div class="card"><div style="font-size:36px">${p.img}</div><div style="font-weight:800;margin-top:6px">${p.name}</div><div style="margin-top:6px"><span class="price-w">₹${price}${p.unit}</span> <span class="price-r">₹${mrp}${p.unit}</span> <span style="background:#dcfce7;color:#16a34a;font-size:10px;padding:2px 8px;border-radius:20px">${save}</span></div><button class="btn btn-b" style="width:100%;margin-top:10px" onclick="add(${i})">Add to Cart</button></div>`;
});
document.getElementById('priceTitle').innerText = mode=='wholesale'?'Wholesale Pricing - Up to 25% OFF':'Retail Pricing';
}
function toggleMode(){mode=mode=='retail'?'wholesale':'retail';document.getElementById('tR').className=mode=='retail'?'active':'';document.getElementById('tW').className=mode=='wholesale'?'active':'';document.getElementById('modeLabel').innerText=mode=='retail'?'Retail Mode':'Wholesale Mode';render();calc();}
function add(i){cart.push(products[i]);let total=cart.reduce((s,p)=>s+(mode=='wholesale'?p.w:p.r),0);let saving=cart.reduce((s,p)=>s+(p.r-p.w),0);document.getElementById('cartCount').innerText=cart.length;document.getElementById('cartTotal').innerText='₹'+total;document.getElementById('saving').innerText=mode=='wholesale'?`(You save ₹${saving})`:'';}
function calc(){let v=document.getElementById('calcProd').value.split('|');let w=parseInt(v[0]),r=parseInt(v[1]);let q=parseInt(document.getElementById('calcQty').value||0);let totalW=w*q, totalR=r*q;document.getElementById('calcOut').innerHTML=`Wholesale Total: ₹${totalW}<br>Retail Total: ₹${totalR}<br><span style="color:#16a34a">You Save: ₹${totalR-totalW} on ${q} pcs</span>`;}
document.getElementById('calcProd').onchange=calc;document.getElementById('calcQty').oninput=calc;
function whatsapp(){if(cart.length==0){alert('Cart empty - add products first');return;}let msg=`Hello MAA ARANAYA ENTERPRISES,%0A%0AI want to order (%0A Mode: ${mode}%0A`+cart.map(p=>`- ${p.name} ₹${mode=='wholesale'?p.w:p.r}`).join('%0A')+`%0A%0ATotal: ${document.getElementById('cartTotal').innerText}`;window.open(`https://wa.me/919876543210?text=${msg}`,'_blank');}
render();calc();
</script>
</body>
</html>
