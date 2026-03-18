<!DOCTYPE html>
<html lang="zh">
<head>
<meta charset="UTF-8">
<title>Music</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:Arial,sans-serif;overflow-x:hidden;background:#0b0f1a;color:#fff;transition:background 0.5s}

body.dark{background:#0f172a;color:#e5e7eb}

.header{position:fixed;top:0;width:100%;height:70px;display:flex;justify-content:space-between;align-items:center;padding:0 60px;background:rgba(0,0,0,.4);backdrop-filter:blur(10px);z-index:100}
.header nav a{margin:0 15px;color:#fff;text-decoration:none;opacity:.9}
.header nav a:hover{color:#00d4ff}
.header .toggle{cursor:pointer;border:1px solid #fff;padding:5px 10px;border-radius:20px}

/* Banner 轮播 */
.banner{width:100%;height:100vh;overflow:hidden;position:relative}
.slider{position:relative;height:100%}
.slide{position:absolute;width:100%;height:100%;opacity:0;transition:1s}
.slide.active{opacity:1;transform:scale(1)}
.slide img{width:100%;height:100%;object-fit:cover}
.slide::after{content:'';position:absolute;inset:0;background:rgba(0,20,80,.55)}

.banner-text{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);color:#fff;text-align:center}
.banner-text h1{font-size:60px}

.section{min-height:100vh;display:flex;align-items:center;justify-content:center;position:relative}
.split{display:flex;width:100%;min-height:80vh}
.split .left,.split .right{flex:1;display:flex;align-items:center;justify-content:center;padding:60px}
.split .left{flex-direction:column;align-items:flex-start}
.split .right{flex-direction:column;align-items:flex-start}

.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:20px;margin-top:20px}
.card{background:rgba(255,255,255,0.1);padding:20px;border-radius:15px;transition:0.3s;cursor:pointer}
.card:hover{transform:scale(1.05)}

.video-container{width:100%;display:flex;flex-direction:column;align-items:center;}
.video-main{width:80%;height:450px;margin-bottom:20px;}
.video-thumbnails{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;}
.video-thumbnails img{width:150px;height:100px;object-fit:cover;cursor:pointer;border:2px solid transparent;border-radius:8px}
.video-thumbnails img.active{border-color:#00d4ff}
</style>
</head>
<body>
<header class="header">
  <div class="logo">Music</div>
  <nav>
    <a href="#intro">Introduction</a>
    <a href="#singer">Singer</a>
    <a href="#video">Video</a>
    <a href="#teaching">Teaching</a>
  </nav>
  <div class="toggle" onclick="toggleDark()">🌙</div>
</header>

<!-- Banner 轮播 -->
<div class="banner">
  <div class="slider" id="slider">
    <div class="slide active"><img src="img3.jpg"></div>
    <div class="slide"><img src="https://tse3.mm.bing.net/th/id/OIP.TANRU2UeqTJ7rgieGBBgogHaEo?rs=1&pid=ImgDetMain&o=7&rm=3"></div>
    <div class="slide"><img src="https://www.shuomingshu.cn/wp-content/uploads/images/2022/11/10/a641b00397ad46c684388b426b38898e_xkcrqx2uen4.jpg"></div>
    <div class="slide"><img src="https://img.phb123.com/uploads/allimg/210702/801-210F2144Z15B.jpg"></div>
    <div class="slide"><img src="img1.jpg"></div>
  </div>
  <div class="banner-text">
    <h1>Feel The Music</h1>
  </div>
</div>

<!-- 分屏 sections -->
<section class="section split" id="intro">
  <div class="left"><h2>🎵 音乐介绍</h2></div>
  <div class="right">
    <p>音乐是一种通过声音来表达情感和思想的艺术形式。它可以通过旋律、节奏和和声带给人们不同的感受，如快乐、悲伤、激动或宁静。</p>
    <p>从古典音乐到流行音乐，从摇滚到电子音乐，每一种风格都有其独特的魅力。音乐不仅是一种娱乐方式，更是一种文化的体现。</p>
    <p>音乐有诸多要素，包括旋律、节奏、和声、音色和形式，这些要素共同构成了音乐的丰富表现力。</p>
    <p>音乐在世界各地有不同的形式和流派，是人类文化的重要组成部分，也是社会活动和娱乐的重要内容。</p>
  </div>
</section>

<section class="section split" id="singer">
  <div class="left"><h2>🎤 歌手推荐</h2></div>
  <div class="right cards">
    <div class="card" data-audio="song1.mp3">Taylor Swift</div>
    <div class="card" data-audio="song2.mp3">BTS</div>
    <div class="card" data-audio="song3.mp3">周杰伦</div>
    <div class="card" data-audio="song4.mp3">Adele</div>
    <div class="card" data-audio="song5.mp3">Ed Sheeran</div>
  </div>
</section>

<section class="section split" id="video">
  <div class="left video-container">
    <iframe class="video-main" src="https://www.youtube.com/embed/3JZ_D3ELwOQ" frameborder="0" allowfullscreen></iframe>
    <div class="video-thumbnails">
      <img src="https://picsum.photos/id/1011/200/120" class="active" data-src="https://www.youtube.com/embed/3JZ_D3ELwOQ">
      <img src="https://picsum.photos/id/1012/200/120" data-src="https://www.youtube.com/embed/2Vv-BfVoq4g">
      <img src="https://picsum.photos/id/1013/200/120" data-src="https://www.youtube.com/embed/5qap5aO4i9A">
    </div>
  </div>
</section>

<section class="section split" id="teaching">
  <div class="left"><h2>📚 音乐教学</h2></div>
  <div class="right">
    <iframe width="100%" height="300" src="https://www.youtube.com/embed/Zi_XLOBDo_Y" frameborder="0" allowfullscreen></iframe>
  </div>
</section>

<audio id="audio-player" controls style="position:fixed;bottom:20px;left:50%;transform:translateX(-50%);width:80%;border-radius:10px;background:#111"></audio>

<script>
function toggleDark(){document.body.classList.toggle('dark')}

// Banner 轮播
let slides=document.querySelectorAll('.slide');
let i=0;
setInterval(()=>{
  slides[i].classList.remove('active');
  i=(i+1)%slides.length;
  slides[i].classList.add('active');
},4000);

// 图片逐帧放大 + 滚动控制
window.addEventListener('scroll',()=>{
  const bannerImg=document.querySelector('.slide.active img');
  let scrollY=window.scrollY;
  if(bannerImg) bannerImg.style.transform=`scale(${1+scrollY/2000})`;
});

// 点击歌手播放音乐
const cards=document.querySelectorAll('.card[data-audio]');
const audio=document.getElementById('audio-player');
cards.forEach(card=>{
  card.addEventListener('click',()=>{
    audio.src=card.dataset.audio;
    audio.play();
  });
});

// 视频切换
const videoMain=document.querySelector('.video-main');
const thumbs=document.querySelectorAll('.video-thumbnails img');
thumbs.forEach(thumb=>{
  thumb.addEventListener('click',()=>{
    videoMain.src=thumb.dataset.src;
    thumbs.forEach(t=>t.classList.remove('active'));
    thumb.classList.add('active');
  });
});
</script>
</body>
</html>
