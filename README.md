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
  transform:translateY(10px);
  transition:1s;
}
#letter p.visible{
  opacity:1;
  transform:translateY(0);
}

/* QUESTIONS MUST BE VISIBLE */
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

/* BALLOONS + HEARTS */
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
<p style="opacity:1;">Today is all about you — your smile, your heart, your soul.  
This little journey is made just for you 🌸</p>
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
<p>Snehal,</p>

<p>Today is not just any day… it’s the day you turn 17, the day the world was blessed with you. I feel so lucky that I’ve known you since 6th standard.</p>

<p>I still remember that 10th standard bus moment — holding your hand on your birthday. That pause… that feeling… uss moment changed everything.</p>

<p>Then came the first hug on 16th September 2024 — pure warmth, comfort, and love.</p>

<p>Since 25th February 2024, uss have created countless memories. My sakhi, you’ve been my peace, my laughter, my strength.</p>

<p>My rasmalai, ladoo, dudu — you make life sweeter just by being in it.</p>

<p>My raanisaheb, you rule my heart effortlessly.</p>

<p>Take care of yourself always. Remember, Aashay is always here — your partner, your best friend, your soul.</p>

<p>Happy 17th Birthday 💖</p>

<p>— Aashay</p>

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
<label><input type="radio" name="q2" onclick="nickname('sakhi')"> sakhi</label>
<label><input type="radio" name="q2" onclick="nickname('raanisaheb')"> raanisaheb</label>
<label><input type="radio" name="q2" onclick="nickname('mau')"> mau</label>

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
<p style="opacity:1;">You are loved more than words can ever say 🌸</p>
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

function nickname(name){
 const map={
  sakhi:"My forever sakhi 💖",
  raanisaheb:"My queen 👑",
  mau:"My cutest mau 🐥"
 };
 document.getElementById("nickmsg").innerText=map[name];
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

/* BALLOONS + HEARTS */
const bg=document.getElementById("bg");
const g=bg.getContext("2d");
bg.width=innerWidth; bg.height=innerHeight;
let b=[];
for(let i=0;i<25;i++)b.push({x:Math.random()*bg.width,y:bg.height+Math.random()*500,s:0.5+Math.random()});
function drawBG(){
 g.clearRect(0,0,bg.width,bg.height);
 b.forEach(o=>{
  g.fillStyle="#ff6699";
  g.beginPath();
  g.ellipse(o.x,o.y,15,22,0,0,Math.PI*2);
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
