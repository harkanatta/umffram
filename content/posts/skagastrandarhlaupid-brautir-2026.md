+++
title = "Skagastrandarhlaupið nálgast – brautirnar eru tilbúnar"
date = 2026-06-29T00:00:00Z
draft = false
featured_image = "/images/utanvegahlaupid2.jpg"
description = "Þrjár vikur eru eftir. Brautirnar eru mældar og við gefum ykkur fyrstu sýn á leiðirnar."
+++

Þrjár vikur eru eftir í Skagastrandarhlaupið! Minnum á skráningu á [netskraning.is/skagastrandarhlaupid](https://netskraning.is/skagastrandarhlaupid).
Nú hafa allar brautir verið mældar og birtum við hér kort af leiðunum svo hægt sé að kynna sér þær, eða prófa þær, áður en keppnin hefst 19. júlí. Fjórar vegalengdir eru í boði:

- Götuhlaup: 5 og 10 km
- AtWork Megatrail: 18 km
- Útbæjarhlaupið: Tæpur kílómetri, ætlað fyrir börn og fullorðna

<!--more-->

Vegalengdirnar eru nokkuð almennar, 5 km hlaupið geta margir hlaupið, 10 km hlaupið er hugsað fyrir aðeins reyndari hlaupara. Utanvegahlaupið verður hátt í 18 km með um 400 m hækkun og 18 ára (2008) aldurstakmark er í það. Öll börn og fullorðin eru hvött til að hlaupa Útbæjarhlaupið. Það verður ekki ræst fyrr en eftir að keppendur eru komnir í mark úr götuhlaupunum og AtWork Megatrail svo að fullorðnir keppendur geti líka hlaupið 1 km með börnunum eftir á.

## AtWork Megatrail – 18 km utanvegahlaup

<img src="/images/hlaup-utanvegahlaup.png" alt="Utanvegahlaupið – 13,5 km" class="hlaup-map" data-index="0" style="width:100%;height:auto;cursor:zoom-in;">

## Götuhlaupið – 5 km og 10 km

<img src="/images/hlaup-vidavangshlaup.png" alt="Götuhlaupið – 5 km og 10 km" class="hlaup-map" data-index="1" style="width:100%;height:auto;cursor:zoom-in;">

## Útbæjarhlaupið – 1 km

<img src="/images/hlaup-barnaskokk.png" alt="Útbæjarhlaupið – 1 km" class="hlaup-map" data-index="2" style="width:100%;height:auto;cursor:zoom-in;">

<style>
#lb-overlay { display:none; position:fixed; inset:0; background:rgba(0,0,0,.92); z-index:9999; align-items:center; justify-content:center; }
#lb-overlay.open { display:flex; }
#lb-img { max-height:90vh; max-width:90vw; object-fit:contain; box-shadow:0 0 40px rgba(0,0,0,.8); }
#lb-close { position:absolute; top:1rem; right:1.5rem; color:#fff; font-size:2.5rem; cursor:pointer; line-height:1; user-select:none; }
#lb-prev, #lb-next { position:absolute; top:50%; transform:translateY(-50%); color:#fff; font-size:2.5rem; cursor:pointer; user-select:none; padding:1rem; background:rgba(0,0,0,.3); border-radius:4px; }
#lb-prev { left:.5rem; } #lb-next { right:.5rem; }
#lb-counter { position:absolute; bottom:1rem; left:50%; transform:translateX(-50%); color:#ccc; font-size:.9rem; }
</style>

<div id="lb-overlay">
  <span id="lb-close">&times;</span>
  <span id="lb-prev">&#8249;</span>
  <img id="lb-img" src="" alt="">
  <span id="lb-next">&#8250;</span>
  <span id="lb-counter"></span>
</div>

<script>
(function(){
  var imgs = Array.from(document.querySelectorAll('img.hlaup-map'));
  var overlay = document.getElementById('lb-overlay');
  var lbImg   = document.getElementById('lb-img');
  var counter = document.getElementById('lb-counter');
  var current = 0;
  function show(idx) {
    current = (idx + imgs.length) % imgs.length;
    lbImg.src = imgs[current].src;
    lbImg.alt = imgs[current].alt;
    counter.textContent = (current + 1) + ' / ' + imgs.length;
    overlay.classList.add('open');
  }
  function close() { overlay.classList.remove('open'); lbImg.src = ''; }
  imgs.forEach(function(img, i) { img.addEventListener('click', function() { show(i); }); });
  document.getElementById('lb-close').addEventListener('click', close);
  document.getElementById('lb-prev').addEventListener('click', function(e) { e.stopPropagation(); show(current - 1); });
  document.getElementById('lb-next').addEventListener('click', function(e) { e.stopPropagation(); show(current + 1); });
  overlay.addEventListener('click', function(e) { if (e.target === overlay) close(); });
  document.addEventListener('keydown', function(e) {
    if (!overlay.classList.contains('open')) return;
    if (e.key === 'Escape') close();
    if (e.key === 'ArrowLeft') show(current - 1);
    if (e.key === 'ArrowRight') show(current + 1);
  });
})();
</script>

## Við þurfum á aðstoð að halda

Ungmennafélagið ásamt björgunarsveitinni Strönd og kvenfélaginu Einingu eru að leita að fólki til að gæta brautanna meðan keppnin fer fram. Þetta felst í því að standa við ákveðin beygjur eða vegamót og sjá til þess að hlauparar fari réttar leiðir og að leiðbeina umferð. Ef þú getur gefið nokkra klukkutíma sunnudaginn 19. júlí, skráðu þig hér:

<style>
#gaesla-form { background:#f5f5f5; border-radius:12px; padding:20px; margin:1.5rem 0; max-width:480px; }
#gaesla-form .fg { display:flex; flex-direction:column; margin-bottom:12px; }
#gaesla-form label { font-size:11px; font-weight:800; letter-spacing:2px; text-transform:uppercase; opacity:0.6; margin-bottom:5px; }
#gaesla-form input { padding:10px 12px; border:2px solid #ccc; border-radius:8px; font-size:15px; font-family:inherit; outline:none; transition:border-color .12s; }
#gaesla-form input:focus { border-color:#002c98; }
#gaesla-btn { width:100%; padding:12px; background:#002c98; color:#fff; border:none; border-radius:8px; font-size:15px; font-weight:800; font-family:inherit; cursor:pointer; transition:background .12s; }
#gaesla-btn:hover:not(:disabled) { background:#be0000; }
#gaesla-btn:disabled { background:#999; cursor:default; }
#gaesla-msg { margin-top:10px; padding:10px 14px; border-radius:8px; font-size:14px; font-weight:700; display:none; }
#gaesla-msg.success { background:#d4edda; color:#155724; display:block; }
#gaesla-msg.error   { background:#f8d7da; color:#721c24; display:block; }
</style>

<div id="gaesla-form">
  <div class="fg"><label for="g-nafn">Nafn</label><input type="text" id="g-nafn" placeholder="Fullt nafn"></div>
  <div class="fg"><label for="g-simi">Símanúmer</label><input type="tel" id="g-simi" placeholder="000-0000"></div>
  <div class="fg"><label for="g-netfang">Netfang</label><input type="email" id="g-netfang" placeholder="netfang@dæmi.is"></div>
  <button id="gaesla-btn" onclick="gaeslaSubmit()">Skrá mig</button>
  <div id="gaesla-msg"></div>
</div>

<script type="module">
import { initializeApp, getApps, getApp } from "https://www.gstatic.com/firebasejs/11.8.1/firebase-app.js";
import { getFirestore, collection, addDoc, serverTimestamp } from "https://www.gstatic.com/firebasejs/11.8.1/firebase-firestore.js";

const cfg = {
  apiKey: "AIzaSyCo-G3s8R84yb_MsgA8xdDrUVegonX2ouM",
  authDomain: "verkefnalisti-umhverfi.firebaseapp.com",
  projectId: "verkefnalisti-umhverfi",
  storageBucket: "verkefnalisti-umhverfi.firebasestorage.app",
  messagingSenderId: "479888787576",
  appId: "1:479888787576:web:3bba7432b794738b41c58d"
};
const app = getApps().length ? getApp() : initializeApp(cfg);
const db = getFirestore(app);

window.gaeslaSubmit = async function() {
  const nafn    = document.getElementById('g-nafn').value.trim();
  const simi    = document.getElementById('g-simi').value.trim();
  const netfang = document.getElementById('g-netfang').value.trim();
  const msg     = document.getElementById('gaesla-msg');
  const btn     = document.getElementById('gaesla-btn');
  msg.className = 'gaesla-msg';

  if (!nafn)    { msg.className='gaesla-msg error'; msg.textContent='Vinsamlegast skráðu nafn.'; return; }
  if (!simi)    { msg.className='gaesla-msg error'; msg.textContent='Vinsamlegast skráðu símanúmer.'; return; }
  if (!netfang) { msg.className='gaesla-msg error'; msg.textContent='Vinsamlegast skráðu netfang.'; return; }

  btn.disabled = true; btn.textContent = 'Skrái...';
  try {
    await addDoc(collection(db, 'brautargaesla2026'), { nafn, simi, netfang, skrad: serverTimestamp() });
    msg.className = 'gaesla-msg success';
    msg.textContent = 'Takk, ' + nafn + '! Við munum hafa samband.';
    btn.textContent = 'Skráð!';
  } catch(e) {
    console.error('Firestore error:', e);
    msg.className = 'gaesla-msg error';
    msg.textContent = 'Villa kom upp: ' + e.message;
    btn.disabled = false; btn.textContent = 'Skrá mig';
  }
};
</script>

## Skráning

Hlaupið verður haldið 19. júlí og fer skráning fram hjá Netskráningu.is. Þar eru einnig allar nauðsynlegar upplýsingar um hlaupið: [netskraning.is/skagastrandarhlaupid](https://netskraning.is/skagastrandarhlaupid/)
