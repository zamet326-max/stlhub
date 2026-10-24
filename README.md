
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>STLHub | 3D Model Kütüphanesi</title>
<style>
:root{--bg:#10111b;--panel:#1b1d2c;--line:#303249;--text:#f6f5ff;--muted:#a6a8c0;--purple:#9675ff;--cyan:#5ee7df}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font-family:Arial,Helvetica,sans-serif}
a{color:inherit;text-decoration:none}
.wrap{width:min(1120px,92%);margin:auto}
header{border-bottom:1px solid var(--line);background:#141522}
nav{min-height:72px;display:flex;align-items:center;justify-content:space-between;gap:16px}
.logo{font-size:27px;font-weight:900;letter-spacing:-1px}.logo span{color:var(--cyan)}
nav a:not(.logo){color:var(--muted);font-size:14px}
button{cursor:pointer;font:inherit}
.btn{border:0;border-radius:11px;padding:12px 17px;background:var(--purple);color:white;font-weight:bold}
.hero{text-align:center;padding:72px 0 48px}
.pill{display:inline-block;border:1px solid #504276;background:#272039;color:#d5c9ff;padding:8px 13px;border-radius:30px;font-size:13px}
h1{font-size:clamp(38px,7vw,68px);line-height:1.08;letter-spacing:-2px;margin:23px 0 15px}
.gradient{background:linear-gradient(90deg,#b09aff,var(--cyan));background-clip:text;color:transparent}
.hero p{max-width:640px;margin:0 auto 25px;color:var(--muted);line-height:1.8}
.search{display:flex;max-width:640px;margin:auto;padding:7px;gap:8px;background:var(--panel);border:1px solid var(--line);border-radius:15px}
.search input{min-width:0;flex:1;padding:12px;background:transparent;color:white;border:0;outline:none}
.stats{display:flex;justify-content:center;gap:35px;flex-wrap:wrap;margin-top:28px;color:var(--muted);font-size:13px}
.stats strong{display:block;color:white;font-size:19px;margin-bottom:5px}
section.content{padding:28px 0 42px}
.heading{display:flex;justify-content:space-between;align-items:end;gap:12px;margin-bottom:20px}
h2{margin:0;font-size:27px}.muted{color:var(--muted);font-size:14px;margin-top:7px}
.filters{display:flex;gap:9px;flex-wrap:wrap;margin-bottom:22px}
.chip{padding:10px 15px;border-radius:24px;border:1px solid var(--line);background:var(--panel);color:var(--muted)}
.chip.active{border-color:var(--purple);background:#302849;color:white}
.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:18px}
.card{background:var(--panel);border:1px solid var(--line);border-radius:17px;overflow:hidden;transition:transform .2s}
.card:hover{transform:translateY(-4px);border-color:#65588c}
.art{height:180px;display:grid;place-items:center;background:radial-gradient(ellipse,#39344f,#202131);position:relative}
.emoji{font-size:75px;filter:drop-shadow(0 10px 15px #0007)}
.tag{position:absolute;top:12px;left:12px;background:#11121c;color:#ddd3ff;padding:6px 9px;border-radius:8px;font-size:12px}
.cardbody{padding:16px}.card h3{margin:0 0 8px;font-size:18px}
.card p{color:var(--muted);font-size:13px;line-height:1.6;min-height:40px;margin:0}
.meta{display:flex;justify-content:space-between;gap:8px;color:var(--muted);font-size:11px;margin:14px 0}
.cardfoot{display:flex;align-items:center;justify-content:space-between;gap:8px}
.smallbtn{background:#302849;border:1px solid #504276;color:white;border-radius:9px;padding:9px 12px}
.banner{margin:20px 0 55px;padding:30px;border:1px solid #504276;border-radius:20px;background:linear-gradient(120deg,#27203e,#192f39)}
.banner p{color:var(--muted);line-height:1.7}
footer{border-top:1px solid var(--line);padding:26px 0;color:var(--muted);font-size:13px}
.footerrow{display:flex;justify-content:space-between;gap:15px;flex-wrap:wrap}
@media(max-width:760px){.grid{grid-template-columns:repeat(2,minmax(0,1fr))}nav a:not(.logo){display:none}.hero{padding-top:48px}}
@media(max-width:500px){.grid{grid-template-columns:1fr}.hero{padding-top:40px}h1{letter-spacing:-1px}.search{flex-wrap:wrap}.search input{flex-basis:100%}.search .btn{width:100%}.heading{align-items:flex-start;flex-direction:column}.stats{gap:20px}}
</style>
</head>
<body>
<header>
<div class="wrap"><nav>
<a href="#" class="logo">STL<span>Hub</span></a>
<a href="#models">Modelleri keşfet</a>
<a href="#categories">Kategoriler</a>
<a href="#about">Hakkımızda</a>
<button class="btn" id="login">Giriş yap</button>
</nav></div>
</header>
<main>
<div class="wrap hero">
<div class="pill">✦ 3D baskı tutkunlarının buluşma noktası</div>
<h1>Hayal et. Tasarla.<br><span class="gradient">3D olarak üret.</span></h1>
<p>3D yazıcın için yeni fikirler keşfet. Dekorasyondan masaüstü aksesuarlara kadar modelleri tek yerde bul.</p>
<form class="search" id="searchForm">
<input id="search" placeholder="Model, kategori veya anahtar kelime ara..." aria-label="Model ara">
<button class="btn" type="submit">⌕ Ara</button>
</form>
<div class="stats">
<div><strong id="count">6</strong>Örnek model</div>
<div><strong>STL</strong>3D baskı odaklı</div>
<div><strong>Keşfet</strong>Yeni fikirler</div>
</div>
</div>
<section class="wrap content" id="models">
<div class="heading"><div><h2>Öne çıkan modeller</h2><div class="muted">Bir sonraki baskı projen için ilham al.</div></div><button class="smallbtn" id="all">Tüm modeller</button></div>
<div class="filters" id="categories">
<button class="chip active" data-cat="Tümü">Tümü</button>
<button class="chip" data-cat="Dekorasyon">🏠 Dekorasyon</button>
<button class="chip" data-cat="Masaüstü">🖥️ Masaüstü</button>
<button class="chip" data-cat="Oyuncak">🧩 Oyuncak</button>
<button class="chip" data-cat="Aksesuar">✨ Aksesuar</button>
<button class="chip" data-cat="Pratik">🛠️ Pratik</button>
</div>
<div class="grid" id="grid"></div>
<p class="muted">Kartlar şimdilik örnektir; gerçek STL dosyaları henüz bağlanmadı.</p>
</section>
<section class="wrap banner" id="about">
<h2>Senin fikrin, senin tasarımın.</h2>
<p>STLHub, 3D baskı modellerini keşfetmek ve lisans koşullarına dikkat ederek paylaşmak için tasarlanıyor.</p>
<button class="btn" id="upload">Model ekleme hakkında</button>
</section>
</main>
<footer><div class="wrap footerrow"><div class="logo">STL<span>Hub</span></div><div>© <span id="year"></span> STLHub</div></div></footer>
<script>
const models=[
{title:"Modern saksı",cat:"Dekorasyon",emoji:"🪴",desc:"Masa ve raflar için modern saksı tasarımı."},
{title:"Masaüstü düzenleyici",cat:"Masaüstü",emoji:"🗂️",desc:"Kalem ve küçük eşyalar için düzenleyici."},
{title:"Geometrik vazo",cat:"Dekorasyon",emoji:"🏺",desc:"Evin için dekoratif bir baskı fikri."},
{title:"Fidget oyuncak",cat:"Oyuncak",emoji:"🌀",desc:"Masa başında kullanabileceğin hareketli oyuncak."},
{title:"Kulaklık askısı",cat:"Aksesuar",emoji:"🎧",desc:"Kulaklığını düzenli şekilde sakla."},
{title:"Kablo tutucu",cat:"Pratik",emoji:"🔌",desc:"Kabloları düzenlemek için pratik tasarım."}
];
let cat="Tümü",q="";
const grid=document.getElementById("grid");
function safe(s){return String(s).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]));}
function render(){
const found=models.filter(m=>(cat==="Tümü"||m.cat===cat)&&(m.title+" "+m.cat+" "+m.desc).toLocaleLowerCase("tr").includes(q.toLocaleLowerCase("tr")));
document.getElementById("count").textContent=found.length;
grid.innerHTML=found.length?found.map(m=>`<article class="card"><div class="art"><span class="tag">${safe(m.cat)}</span><span class="emoji">${m.emoji}</span></div><div class="cardbody"><h3>${safe(m.title)}</h3><p>${safe(m.desc)}</p><div class="meta"><span>STLHub örnek</span><span>Lisans kontrol edilmeli</span></div><div class="cardfoot"><span class="muted">STL modeli</span><button class="smallbtn download">İndir</button></div></div></article>`).join(""):'<div style="grid-column:1/-1;text-align:center;padding:35px;color:#a6a8c0">Model bulunamadı. Başka bir kelime dene.</div>';
grid.querySelectorAll(".download").forEach(b=>b.onclick=()=>alert("Bu örnek kart için gerçek STL dosyası henüz eklenmedi."));
}
document.querySelectorAll("[data-cat]").forEach(b=>b.onclick=()=>{cat=b.dataset.cat;document.querySelectorAll("[data-cat]").forEach(x=>x.classList.toggle("active",x===b));render();});
document.getElementById("searchForm").onsubmit=e=>{e.preventDefault();q=document.getElementById("search").value.trim();render();};
document.getElementById("all").onclick=()=>{cat="Tümü";q="";document.getElementById("search").value="";document.querySelectorAll("[data-cat]").forEach(b=>b.classList.toggle("active",b.dataset.cat==="Tümü"));render();};
document.getElementById("login").onclick=()=>alert("Üyelik sistemi sonraki adımda Supabase ile bağlanacak.");
document.getElementById("upload").onclick=()=>alert("Model ekleme sistemi henüz etkin değil.");
document.getElementById("year").textContent=new Date().getFullYear();
render();
</script>
</body>
</html>
