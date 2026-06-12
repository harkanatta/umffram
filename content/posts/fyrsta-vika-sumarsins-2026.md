+++
title = "Fyrsta vika sumarsins"
date = 2026-06-09T00:00:00Z
draft = false
featured_image = "/images/gallery/2026/IMG_7164.JPEG"
description = "Fyrsta vikan af sumarnámskeiðum fór vel af stað með knattspyrnu og skólagarðum."
+++

Fyrsta vikan af sumarnámskeiðum fór vel af stað. Tóti mætti með Knattspyrnuakademíu Norðurlands og hélt stuttar tveggja æfinga búðir á sparkvellinum. Hann flutti seinni æfinguna inn í íþróttahús í skjól fyrir rigningunni á þriðjudaginn.

Dagana eftir héldum við skólagarða þar sem gróðurkassar voru gerðir úr úreldum fiskikörum. Skólagarðarnir eru nýtt og spennandi verkefni frá henni Judith. Þeir voru vel sóttir og viljum við þakka þeim Öllu í Ásgarði, Daníel, Ílónu, Sibba og Slavko fyrir efni og aðstoð.

Við megum koma og kíkja á hvernig gróðurinn vex og sjá hvort hann dafnar vel. Það þarf að vöka við og við en athugum að það er verra ef plöntur eru vökvaðar of mikið frekar en of lítið. Hún Judith verður til taks og fylgist með í sumar og við látum alla vita áður en uppskera hefst.

<style>
.lb-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(260px,1fr)); gap:8px; margin-top:2rem; }
.lb-grid img { width:100%; height:220px; object-fit:cover; cursor:pointer; display:block; transition:opacity .2s; }
.lb-grid img:hover { opacity:.85; }
#lb-overlay { display:none; position:fixed; inset:0; background:rgba(0,0,0,.92); z-index:9999; align-items:center; justify-content:center; }
#lb-overlay.open { display:flex; }
#lb-img { max-height:90vh; max-width:90vw; object-fit:contain; box-shadow:0 0 40px rgba(0,0,0,.8); }
#lb-close { position:absolute; top:1rem; right:1.5rem; color:#fff; font-size:2.5rem; cursor:pointer; line-height:1; user-select:none; }
#lb-prev, #lb-next { position:absolute; top:50%; transform:translateY(-50%); color:#fff; font-size:2.5rem; cursor:pointer; user-select:none; padding:1rem; background:rgba(0,0,0,.3); border-radius:4px; }
#lb-prev { left:.5rem; }
#lb-next { right:.5rem; }
#lb-counter { position:absolute; bottom:1rem; left:50%; transform:translateX(-50%); color:#ccc; font-size:.9rem; }
</style>

<div class="lb-grid" id="lb-gallery">
  <img src="/images/gallery/2026/IMG_7123.JPEG" alt="" data-index="0">
  <img src="/images/gallery/2026/IMG_7155.JPEG" alt="" data-index="1">
  <img src="/images/gallery/2026/IMG_7156.JPEG" alt="" data-index="2">
  <img src="/images/gallery/2026/IMG_7164.JPEG" alt="" data-index="3">
  <img src="/images/gallery/2026/IMG_7170.JPEG" alt="" data-index="4">
  <img src="/images/gallery/2026/IMG_7175.JPEG" alt="" data-index="5">
  <img src="/images/gallery/2026/IMG_7199.JPEG" alt="" data-index="6">
  <img src="/images/gallery/2026/IMG_7202.JPEG" alt="" data-index="7">
  <img src="/images/gallery/2026/IMG_7205.JPEG" alt="" data-index="8">
</div>

<div id="lb-overlay">
  <span id="lb-close">&times;</span>
  <span id="lb-prev">&#8249;</span>
  <img id="lb-img" src="" alt="">
  <span id="lb-next">&#8250;</span>
  <span id="lb-counter"></span>
</div>

<script>
(function(){
  var images = Array.from(document.querySelectorAll('#lb-gallery img'));
  var srcs = images.map(function(i){ return i.src; });
  var overlay = document.getElementById('lb-overlay');
  var lbImg = document.getElementById('lb-img');
  var counter = document.getElementById('lb-counter');
  var current = 0;

  function show(idx){
    current = (idx + srcs.length) % srcs.length;
    lbImg.src = srcs[current];
    counter.textContent = (current+1) + ' / ' + srcs.length;
    overlay.classList.add('open');
  }
  function close(){ overlay.classList.remove('open'); lbImg.src=''; }

  images.forEach(function(img, idx){
    img.addEventListener('click', function(){ show(idx); });
  });
  document.getElementById('lb-close').addEventListener('click', close);
  document.getElementById('lb-prev').addEventListener('click', function(e){ e.stopPropagation(); show(current-1); });
  document.getElementById('lb-next').addEventListener('click', function(e){ e.stopPropagation(); show(current+1); });
  overlay.addEventListener('click', function(e){ if(e.target===overlay) close(); });
  document.addEventListener('keydown', function(e){
    if(!overlay.classList.contains('open')) return;
    if(e.key==='Escape') close();
    if(e.key==='ArrowLeft') show(current-1);
    if(e.key==='ArrowRight') show(current+1);
  });
})();
</script>
