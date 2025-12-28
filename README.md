<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snehal’s 17th Birthday 💖</title>

<style>
body{
  margin:0;
  font-family: Arial, sans-serif;
  background:#ffe6f0;
  overflow-x:hidden;
}
.container{
  max-width:750px;
  margin:40px auto;
  background:rgba(255,240,246,0.95);
  padding:25px;
  border-radius:18px;
  position:relative;
  z-index:2;
}
h1{ color:#ff3366; text-align:center; }

button{
  background:#ff3366;
  color:white;
  border:none;
  padding:12px 22px;
  border-radius:10px;
  cursor:pointer;
  font-size:16px;
  transition:0.3s;
}
button:hover{
  background:#ff6699;
  transform:scale(1.1);
}

section{ display:none; }

input[type="password"]{
  padding:10px;
  width:220px;
  border-radius:6px;
  border:1px solid #ccc;
}

/* LETTER ANIMATION */
#letter p{
  opacity:0;
  transform:translateY(12px);
  transition:1s;
}
#letter p.visible{
  opacity:1;
  transform:translateY(0);
}

/* QUESTIONS VISIBILITY */
#questions p,
#questions label{
  opacity:1;
  color:#333;
  font-size:16px;
}

label{
  display:block;
  margin:8px 0;
  cursor:pointer;
}

.nickname-msg{
  margin-top:10px;
  color:#ff3366;
  font-weight:bold;
}

/* BACKGROUND */
canvas{
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  pointer-events:none;
  z-index:1;
}
</style>
</head>

<body>

<canvas id="bg"></canvas>
<canvas id="confetti"></canvas>

<div class="container">

<!-- INTRO -->
<section id="intro" style="display:block;">
<h1>Happy 17th Birthday Snehal 💖</h1>
<p style="opacity:1;">This little journey is made only for you 🌸</p>
<button onclick="go('password')">Read Letter 💌</button>
</section>

<!-- PASSWORD -->
<section id="password">
<h1>Enter Password 💖</h1>
<input type="password" id="pass" placeholder="Password">
<br><br>
<button onclick="checkPass()">Unlock Letter 🔓</button>
</section>

<!-- LETTER -->
<section id="letter">

<p><strong>Snehal,</strong></p>

<p>Today is not just any day… it’s the day you turn 17, the day the world was blessed with you. I feel so lucky that I’ve known you since 6th standard — all the laughter, all the small moments, all the memories we’ve created together… I wouldn’t trade any of them for anything.</p>

<p>I still remember that day in 10th grade, your birthday, when I first held your hand on the bus while returning home. That tiny moment felt like the world had paused for uss, and it’s etched in my heart forever. And the first hug on 16th September 2024… I’ll never forget how perfect that felt. Each of these moments made me realize how truly special you are.</p>

<p>Since 25th February 2024, we’ve been creating countless memories together — laughter, silly jokes, quiet talks, teasing each other, sharing dreams, and supporting one another. My sakhi, you’ve been my constant companion, my comfort, and the person who understands me like no one else. Uss journey with you has been the most beautiful adventure.</p>

<p>My rasmalai, every time I see your smile, it feels like sunlight breaking through the clouds. You light up every space you’re in, and every moment with you becomes a memory I want to hold forever. I love how naturally we can laugh together, how we can be goofy, serious, and romantic all at once.</p>

<p>My ladoo, your kindness, patience, and strength inspire me every day. You have this magical ability to make the world feel soft and safe, and I hope you always remember to treat yourself with the same love and care that you give to everyone else.</p>

<p>My dudu, being with you has taught me so much about love, friendship, and trust. You are my partner in every sense — the one who stands by me, who celebrates my highs and comforts me during lows, who makes ordinary days extraordinary.</p>

<p>And my raanisaheb, you are my queen in every little way — ruling my heart completely. Every memory we’ve made, every moment we’ve shared, and every laugh, hug, and hand-hold is engraved in my soul. I feel so blessed to have you as my girlfriend, my best friend, my soulmate — my everything.</p>

<p>Snehal, 17 is a beautiful age. It’s a time to dream bigger, laugh louder, love deeper, and embrace every part of yourself. I hope you never forget your worth, your strength, and your beauty — not just outside, but inside, where your soul shines brighter than anyone I’ve ever known.</p>

<p>Today, I want to remind you to take care of yourself, to cherish your happiness, and to know that I, Aashay, am always here — not just as your boyfriend, but as your friend, your partner, your soul. Every day with you is a gift, and I can’t wait for all the memories uss have yet to create.</p>

<p><strong>Happy 17th Birthday, my love. 💖</strong></p>

<p>With all my heart,<br><strong>Aashay</strong></p>

<button onclick="go('questions')">Next ➡️</button>
</section>

<!-- QUESTIONS -->
<section id="questions">
<h1>Just One More Step 🎉</h1>

<p>1. Which moment with me makes you smile the most?</p>
<label><input type="radio" name="q1"> First hand-hold</label>
<label><input type="radio" name="q1"> First hug</label>
<label><input type="radio" name="q1"> School memories</label>

<p>2. Which is your favorite nickname?</p>
<label><input type="radio" name="q2" onclick="nick('sakhi')"> sakhi</label>
<label><input type="radio" name="q2" onclick="nick('raanisaheb')"> raanisaheb</label>
<label><input type="radio" name="q2" onclick="nick('mau')"> mau</label>

<div class="nickname-msg" id="nickmsg"></div>

<p>3. What do you want uss to do this year?</p>
<label><input type="radio" name="q3"> Travel</label>
<label><input type="radio" name="q3"> More memories</label>
<label><input type="radio" name="q3"> Everything together</label>

<button onclick="finish()">Submit 🎊</button>
</section>

<!-- FINAL -->
<section id="final">
<h1>🎉 Happy Birthday Snehal 💖</h1>
<p style="opacity:1;">You are loved beyond words 🌸</p>
</section>

</div>

<script>
const PASSWORD="snehashay1303";

function go(id){
 document.querySelectorAll("section").forEach(s=>s.style.display="none");
 document.getElementById(id).style.display="block";

 if(id==="letter"){
  document.querySelectorAll("#letter p").forEach((p,i)=>{
   setTimeout(()=>p.classList.add("visible"), i*500);
  });
 }
}

function checkPass(){
 if(document.getElementById("pass").value===PASSWORD){
  go("letter");
 } else alert("Wrong password 💔");
}

function nick(n){
 const m={
  sakhi:"My forever sakhi 💖",
  raanisaheb:"My queen 👑",
  mau:"My cutest mau 🐣"
 };
 document.getElementById("nickmsg").innerText=m[n];
}

function finish(){
 go("final");
 party();
}

/* CONFETTI */
function party(){
 const c=document.getElementById("confetti");
 const x=c.getContext("2d");
 c.width=innerWidth; c.height=innerHeight;
 let p=[];
 for(let i=0;i<200;i++)p.push({x:Math.random()*c.width,y:Math.random()*c.height,r:Math.random()*6+4});
 function d(){
  x.clearRect(0,0,c.width,c.height);
  p.forEach(o=>{
   x.fillStyle=`hsl(${Math.random()*360},100%,50%)`;
   x.beginPath();
   x.arc(o.x,o.y,o.r,0,Math.PI*2);
   x.fill();
   o.y+=2;
  });
  requestAnimationFrame(d);
 }
 d();
}

/* BALLOONS */
const bg=document.getElementById("bg");
const g=bg.getContext("2d");
bg.width=innerWidth; bg.height=innerHeight;
let b=[];
for(let i=0;i<25;i++)b.push({x:Math.random()*bg.width,y:bg.height+Math.random()*400,s:0.6+Math.random()});
function drawBG(){
 g.clearRect(0,0,bg.width,bg.height);
 b.forEach(o=>{
  g.fillStyle="#ff6699";
  g.beginPath();
  g.ellipse(o.x,o.y,14,20,0,0,Math.PI*2);
  g.fill();
  o.y-=o.s;
  if(o.y<-50)o.y=bg.height+50;
 });
 requestAnimationFrame(drawBG);
}
drawBG();
</script>

</body>
</html>
