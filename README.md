<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>for my dearest jesicha my love</title>

<style>
body {
  margin:0;
  font-family:"Georgia", serif;
  color:#4b2c20;
  background: radial-gradient(circle at top, #ffe6ea, #ee9ca7);
  overflow:hidden;
  display:flex;
  justify-content:center;
  align-items:center;
  min-height:100vh;
  text-align:center;
}

/* 🌌 cinematic fade in */
.container {
  animation: fadeIn 2.5s ease-in;
  z-index:2;
}

h1 {
  font-size:3em;
  animation: glow 3s infinite alternate;
}

p {
  max-width:600px;
  font-size:1.2em;
  line-height:1.6;
  animation: fadeIn 3s ease-in;
}

.signature {
  margin-top:2em;
  font-style:italic;
  animation: fadeIn 4s ease-in;
}

.heart {
  font-size:2em;
  animation: beat 1.5s infinite;
}

@keyframes fadeIn {
  from {opacity:0; transform:translateY(20px);}
  to {opacity:1; transform:translateY(0);}
}

@keyframes beat {
  0%,100% {transform:scale(1);}
  50% {transform:scale(1.3);}
}

@keyframes glow {
  from {text-shadow:0 0 10px #fff;}
  to {text-shadow:0 0 25px #ff4d6d;}
}

/* 💖 start screen */
#startScreen {
  position:fixed;
  width:100%;
  height:100%;
  background:#ffdde1;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  z-index:9999;
}

#startScreen button {
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:#e63946;
  color:white;
  font-size:16px;
  cursor:pointer;
  box-shadow:0 0 20px rgba(230,57,70,0.5);
}

/* 💖 floating hearts */
.heartFloat {
  position:absolute;
  color:#ff4d6d;
  animation: floatUp 6s linear infinite;
  opacity:0.8;
}

@keyframes floatUp {
  0% {transform:translateY(100vh) scale(0.5); opacity:0;}
  50% {opacity:1;}
  100% {transform:translateY(-10vh) scale(1.2); opacity:0;}
}

/* ✨ sparkles */
.sparkle {
  position:absolute;
  width:6px;
  height:6px;
  background:white;
  border-radius:50%;
  animation: sparkle 4s linear infinite;
  opacity:0.7;
}

@keyframes sparkle {
  0% {transform:translateY(100vh); opacity:0;}
  50% {opacity:1;}
  100% {transform:translateY(-10vh); opacity:0;}
}

/* 🌌 stars background */
.stars {
  position:fixed;
  width:100%;
  height:100%;
  background:transparent;
  z-index:0;
}
.stars::before {
  content:"";
  position:absolute;
  width:200%;
  height:200%;
  background:radial-gradient(white 1px, transparent 1px);
  background-size:50px 50px;
  animation: moveStars 60s linear infinite;
  opacity:0.3;
}

@keyframes moveStars {
  from {transform:translateY(0);}
  to {transform:translateY(-1000px);}
}

</style>
</head>

<body>

<div class="stars"></div>

<!-- 💖 START -->
<div id="startScreen">
  <h2>💖 Enter My Heart 💖</h2>
  <button onclick="startSite()">Begin</button>
</div>

<!-- 🎵 MUSIC -->
<audio id="bgMusic" loop>
  <source src="music.mp3" type="audio/mpeg">
</audio>

<!-- 💌 CONTENT (UNCHANGED MESSAGE) -->
<div class="container">

<h1>for my dearest jesicha my love 💖</h1>

<p>
My Dearest, They say that distance makes the heart grow fonder, but honestly, it just makes me realize how much of my world is built around you. Even though there are hundreds of miles between us, I find traces of you in everything—in the songs I listen to, the quiet moments of my morning, and every wish I make. You are my home, and no amount of distance can ever change the way my heart beats only for you.
</p>

<div class="signature">
Forever yours,<br> Jeremiah
</div>

<div class="heart">❤️</div>

</div>

<script>
function startSite() {
  document.getElementById("startScreen").style.display="none";
  document.getElementById("bgMusic").play();

  startHearts();
  startSparkles();
}

/* 💖 hearts */
function startHearts() {
  setInterval(() => {
    let h = document.createElement("div");
    h.classList.add("heartFloat");
    h.innerHTML="💖";
    h.style.left=Math.random()*100+"vw";
    h.style.fontSize=(Math.random()*20+10)+"px";
    h.style.animationDuration=(Math.random()*3+3)+"s";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),6000);
  },300);
}

/* ✨ sparkles */
function startSparkles() {
  setInterval(() => {
    let s = document.createElement("div");
    s.classList.add("sparkle");
    s.style.left=Math.random()*100+"vw";
    s.style.animationDuration=(Math.random()*3+2)+"s";
    document.body.appendChild(s);
    setTimeout(()=>s.remove(),4000);
  },200);
}
</script>

</body>
</html>
