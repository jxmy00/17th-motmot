# 17th-motmot
17th monthsarry
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Motmot Scrapbook</title>
<link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap" rel="stylesheet">
<style>
  body { display:flex; justify-content:center; align-items:center; height:100vh; background:#fef6f6; font-family:'Patrick Hand', cursive; margin:0; }
  .book { width:95%; max-width:600px; height:80vh; perspective:2000px; position:relative; }
  .page { width:100%; height:100%; background:white; position:absolute; transform-style: preserve-3d; box-shadow:0 5px 15px rgba(0,0,0,0.2); border-radius:10px; padding:15px; transition: transform 1s; overflow:hidden; display:flex; flex-direction:column; }
  .cover { border: 5px dashed pink; display:flex; align-items:center; justify-content:center; flex-direction:column; position:relative; background:linear-gradient(135deg,#ffe6f0,#fff0f5); }
  .cover h1 { font-size:24px; color:#ff5c8d; text-align:center; margin:0; }
  .cover .hearts { position:absolute; top:10px; right:10px; font-size:24px; }
  .sticker { position:absolute; font-size:20px; }
  .top-left { top:10px; left:10px; }
  .top-right { top:10px; right:10px; }
  .bottom-left { bottom:10px; left:10px; }
  .bottom-right { bottom:10px; right:10px; }
  .editable { flex:1; width:100%; height:100%; outline:none; border:none; font-size:16px; background:transparent; resize:none; padding:10px; }
  .texture1 { background: #fffaf0; } .texture2 { background: #fff0f5; } .texture3 { background: #f0fff0; }
  .texture4 { background: #f0f8ff; } .texture5 { background: #fff5ee; } .texture6 { background: #fdf5e6; }
  .texture7 { background: #f5f5dc; } .texture8 { background: #ffe4e1; } .texture9 { background: #f0ffff; }
</style>
</head>
<body>
<div class="book">
  <!-- Cover Page -->
  <div class="page cover" style="z-index:10;">
    <div class="hearts">💖💕🌸</div>
    <h1>Happy 17th Motmot Love</h1>
  </div>

  <!-- Pages 2 to 10 with stickers -->
  <div class="page texture1" style="transform: rotateY(180deg); z-index:9;">
    <span class="sticker top-left">🌸</span>
    <span class="sticker top-right">💛</span>
    <span class="sticker bottom-left">✨</span>
    <span class="sticker bottom-right">💖</span>
    <textarea class="editable" data-page="1" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture2" style="transform: rotateY(180deg); z-index:8;">
    <span class="sticker top-left">🌟</span>
    <span class="sticker top-right">💜</span>
    <span class="sticker bottom-left">🌷</span>
    <span class="sticker bottom-right">💗</span>
    <textarea class="editable" data-page="2" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture3" style="transform: rotateY(180deg); z-index:7;">
    <span class="sticker top-left">🌸</span>
    <span class="sticker top-right">💖</span>
    <span class="sticker bottom-left">🌼</span>
    <span class="sticker bottom-right">💛</span>
    <textarea class="editable" data-page="3" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture4" style="transform: rotateY(180deg); z-index:6;">
    <span class="sticker top-left">💌</span>
    <span class="sticker top-right">💗</span>
    <span class="sticker bottom-left">✨</span>
    <span class="sticker bottom-right">🌸</span>
    <textarea class="editable" data-page="4" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture5" style="transform: rotateY(180deg); z-index:5;">
    <span class="sticker top-left">🌈</span>
    <span class="sticker top-right">💖</span>
    <span class="sticker bottom-left">💛</span>
    <span class="sticker bottom-right">🌷</span>
    <textarea class="editable" data-page="5" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture6" style="transform: rotateY(180deg); z-index:4;">
    <span class="sticker top-left">🌸</span>
    <span class="sticker top-right">💌</span>
    <span class="sticker bottom-left">✨</span>
    <span class="sticker bottom-right">💖</span>
    <textarea class="editable" data-page="6" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture7" style="transform: rotateY(180deg); z-index:3;">
    <span class="sticker top-left">💛</span>
    <span class="sticker top-right">🌟</span>
    <span class="sticker bottom-left">🌸</span>
    <span class="sticker bottom-right">💜</span>
    <textarea class="editable" data-page="7" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture8" style="transform: rotateY(180deg); z-index:2;">
    <span class="sticker top-left">💖</span>
    <span class="sticker top-right">🌸</span>
    <span class="sticker bottom-left">💗</span>
    <span class="sticker bottom-right">✨</span>
    <textarea class="editable" data-page="8" placeholder="Write your letter here..."></textarea>
  </div>

  <div class="page texture9" style="transform: rotateY(180deg); z-index:1;">
    <span class="sticker top-left">🌷</span>
    <span class="sticker top-right">💛</span>
    <span class="sticker bottom-left">💖</span>
    <span class="sticker bottom-right">💌</span>
    <textarea class="editable" data-page="9" placeholder="Write your letter here..."></textarea>
  </div>
</div>

<script>
const pages = document.querySelectorAll('.page');
let current = 0;

// Page flip
pages.forEach(page => {
  page.addEventListener('click', () => {
    if(current < pages.length) {
      pages[current].style.transform = 'rotateY(-180deg)';
      current++;
    } else {
      pages.forEach((p,i)=>p.style.transform = i===0?'rotateY(0deg)':'rotateY(180deg)');
      current=0;
    }
  });
});

// Auto-save text
const textareas = document.querySelectorAll('.editable');
textareas.forEach(area => {
  const key = 'scrapbook_page_' + area.dataset.page;
  // Load saved text
  area.value = localStorage.getItem(key) || '';
  // Save on input
  area.addEventListener('input', ()=> {
    localStorage.setItem(key, area.value);
  });
});
</script>
</body>
</html>
