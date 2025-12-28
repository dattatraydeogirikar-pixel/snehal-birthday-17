<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snehal's 17th Birthday 💖</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #ffe6f0;
  color: #333;
  text-align: center;
  padding: 20px;
  overflow-x:hidden;
}
.container {
  max-width: 700px;
  margin: 0 auto;
  background: rgba(255,240,246,0.95);
  padding: 20px;
  border-radius: 15px;
  position: relative;
  z-index: 1;
}
h1 { color: #ff3366; }
button {
  padding: 10px 20px;
  margin-top: 15px;
  background: #ff3366;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: transform 0.2s, background 0.2s;
}
button:hover {
  transform: scale(1.1);
  background: #ff6699;
}
section { display: none; text-align:left; }
input[type="password"] { padding:8px; border-radius:5px; border:1px solid #ccc; width:200px; margin-top:10px;}
p { line-height:1.6; margin-bottom:12px; opacity:0; transition: opacity 1s ease-in; }
p.visible { opacity:1; }
strong.nick { color:#ff3366; font-weight:600; }
label { display:block; margin-bottom:8px; cursor:pointer; }
canvas#balloons, canvas#confetti {
  position: fixed;
  top:0; left:0;
  width:100%; height:100%;
  pointer-events:none;
  z-index:0;
}
</style>
</head>
<body>

<canvas id="balloons"></canvas>
<canvas id="confetti"></canvas>

<div class="container">

<!-- 1. Small Birthday Message -->
<section id="intro" style="display:block;">
<h1>Happy 17th Birthday, Snehal! 💖</h1>
<p class="visible">Dear Snehal, wishing you a day filled with love, laughter, and all the happiness in the world. You are my sakhi, rasmalai, ladoo, dudu, raanisaheb, and my most precious person. 💖</p>
<button onclick="nextSection('passwordSection')">Read Letter 💌</button>
</section>

<!-- 2. Password Section -->
<section id="passwordSection">
<h1>Enter Password to Read the Letter 💖</h1>
<p>Please enter the password to unlock your special letter.</p>
<input type="password" id="letterPasswordInput" placeholder="Enter password">
<br>
<button onclick="checkLetterPassword()">Unlock Letter 🎉</button>
</section>

<!-- 3. Full Letter -->
<section id="letter">
<p>Snehal,</p>

<p>Today is not just any day… it’s the day you turn 17, the day the world was blessed with you. I feel so lucky that I’ve known you since 6th standard — all the laughter, all the small moments, all the memories we’ve created together… I wouldn’t trade any of them for anything.</p>

<p>I still remember that day in 10th grade, your birthday, when I first held your hand on the bus while returning home. That tiny moment felt like the world had paused for uss, and it’s etched in my heart forever. And the first hug on 16th September 2024… I’ll never forget how perfect that felt. Each of these moments made me realize how truly special you are.</p>

<p>Since 25th February 2024, we’ve been creating countless memories together — laughter, silly jokes, quiet talks, teasing each other, sharing dreams, and supporting one another. My sakhi, you’ve been my constant companion, my comfort, and the person who understands me like no one else. Uss journey with you has been the most beautiful adventure.</p>

<p>My rasmalai, every time I see your smile, it feels like sunlight breaking through the clouds. You light up every space you’re in, and every moment with you becomes a memory I want to hold forever. I love how naturally we can laugh together, how we can be goofy, serious, and romantic all at once.</p>

<p>My ladoo, your kindness, patience, and strength inspire me every day. You have this magical ability to make the world feel soft and safe, and I hope you always remember to treat yourself with the same love and care that you give to everyone else.</p>

<p>My dudu, being with you has taught me so much about love, friendship, and trust. You are my partner in every sense — the one who stands by me, who celebrates my highs and comforts me during lows, who makes ordinary days extraordinary.</p>

<p>And my raanisaheb, you are my queen in every little way — ruling my heart completely. Every memory we’ve made, every moment we’ve shared, and every laugh, hug, and hand-hold is engraved in my soul. I feel so blessed to have you as my girlfriend, my best friend, my soulmate — my everything.</p>

<p>Snehal, 17 is a beautiful age. It’s a time to dream bigger, laugh louder, love deeper, and embrace every part of yourself. I hope you never forget your worth, your strength, and your beauty — not just outside, but inside, where your soul shines brighter than anyone I’ve ever known.</p>

<p>Today, I want to remind you to take care of yourself, to cherish your happiness, and to know that I, Aashay, am always here — not just as your boyfriend, but as your friend, your partner, your soul. Every day with you is a gift, and I can’t wait for all the memories uss have yet to create.</p>

<p>Happy 17th Birthday, my love. 💖</p>

<p>With all my heart,<br>Aashay</p>

<button onclick="nextSection('questions')">Next ➡️</button>
</section>

<!-- 4. Personal Questions -->
<section id="questions">
<p>Answer these personal questions to unlock your final birthday message:</p>

<p>1. Which moment with me makes you smile the most?</p>
<label><input type="radio" name="q1" value="First Hand Hold"> First Hand Hold</label>
<label><input type="radio" name="q1" value="First Hug"> First Hug</label>
<label><input type="radio" name="q1" value="Fun School Memories"> Fun School Memories</label>

<p>2. Which is your favorite nickname?</p>
<label><input type="radio" name="q2" value="sakhi"> sakhi</label>
<label><input type="radio" name="q2" value="raanisaheb"> raanisaheb</label>
<label><input type="radio" name="q2" value="mau"> mau</label>

<p>3. What would you like us to do together this year?</p>
<label><input type="radio" name="q3" value="Travel"> Travel</label>
<label><input type="radio" name="q3" value="Fun Adventures"> Fun Adventures</label>
<label><input type="radio" name="q3" value="Make More Memories"> Make More Memories</label>

<button onclick="submitAnswers()">Submit Answers</button>
</section>

<!-- 5. Final Message -->
<section id="final">
<h1>🎉 Happy 17th Birthday, Snehal 💖</h1>
<p>May this year be full of love, joy, and unforgettable memories. You deserve the world and more. 💖</p>
<canvas id="confetti"></canvas>
</section>

</div>

<script>
const letterPassword = "snehashay1303"; // Password for letter

function nextSection(id){
  document.querySelectorAll('section').forEach(s => s.style.display='none');
  const section = document.getElementById(id);
  section.style.display = 'block';

  if(id==='letter'){
    const paragraphs = section.querySelectorAll('p');
    paragraphs.forEach((p,i) => {
      setTimeout(() => p.classList.add('visible'), i*500);
    });
  }

  if(id==='final'){
    startConfetti();
  }
}

function checkLetterPassword(){
  const input = document.getElementById('letterPasswordInput').value;
  if(input === letterPassword){
    nextSection('letter');
  } else {
    alert("Incorrect password! Please try again.");
  }
}

function submitAnswers(){
  const q1 = document.querySelector('input[name="q1"]:checked');
  const q2 = document.querySelector('input[name="q2"]:checked');
  const q3 = document.querySelector('input[name="q3"]:checked');

  if(!q1 || !q2 || !q3){
    alert("Please answer all questions!");
    return;
  }

  nextSection('final');
}

// Confetti effect
function startConfetti(){
  const canvas = document.getElementById('confetti');
  const ctx = canvas.getContext('2d');
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;

  const pieces = [];
  for(let i=0;i<200;i++){
    pieces.push({
      x: Math.random()*canvas.width,
      y: Math.random()*canvas.height,
      r: Math.random()*6+4,
      d: Math.random()*100,
      color: `hsl(${Math.random()*360},100%,50%)`,
      tilt: Math.random()*10-10,
      tiltAngleIncrement: Math.random()*0.07+0.05,
      tiltAngle:0
    });
  }

  function draw(){
    ctx.clearRect(0,0,canvas.width,canvas.height);
    pieces.forEach(p=>{
      ctx.beginPath();
      ctx.lineWidth = p.r/2;
      ctx.strokeStyle = p.color;
      ctx.moveTo(p.x+p.tilt+ p.r/4, p.y);
      ctx.lineTo(p.x+p.tilt, p.y+p.tilt+p.r/4);
      ctx.stroke();
      p.tiltAngle += p.tiltAngleIncrement;
      p.y += (Math.cos(p.d)+1+p.r/2)/2;
      p.x += Math.sin(p.tiltAngle);
      if(p.y>canvas.height){ p.y=0; p.x=Math.random()*canvas.width; }
    });
    requestAnimationFrame(draw);
  }
  draw();
}

// Balloons
const canvasB = document.getElementById('balloons');
const ctxB = canvasB.getContext('2d');
canvasB.width = window.innerWidth;
canvasB.height = window.innerHeight;

const balloons = [];
const colors = ['#ff3366','#ff6699','#ff99cc','#ffb3d9','#ff80bf'];

for(let i=0;i<20;i++){
  balloons.push({
    x: Math.random()*canvasB.width,
    y: canvasB.height + Math.random()*200,
    r: 20+Math.random()*15,
    color: colors[Math.floor(Math.random()*colors.length)],
    speed: 0.5 + Math.random()*1
  });
}

function drawBalloons(){
  ctxB.clearRect(0,0,canvasB.width,canvasB.height);
  balloons.forEach(b=>{
    ctxB.beginPath();
    ctxB.fillStyle = b.color;
    ctxB.ellipse(b.x, b.y, b.r*0.6, b.r, 0, 0, 2*Math.PI);
    ctxB.fill();
    ctxB.beginPath();
    ctxB.moveTo(b.x, b.y+b.r);
    ctxB.lineTo(b.x, b.y+b.r+20);
    ctxB.strokeStyle = b.color;
    ctxB.lineWidth=2;
    ctxB.stroke();
    b.y -= b.speed;
    if(b.y < -50) b.y = canvasB.height + 50;
  });
  requestAnimationFrame(drawBalloons);
}
drawBalloons();
</script>

</body>
</html>
