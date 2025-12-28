<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snehal's 17th Birthday 💖</title>
<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ffe6f0, #f3e8ff);
  color: #333;
  text-align: center;
  padding: 20px;
}
.container {
  max-width: 650px;
  margin: 0 auto;
  text-align: left;
  background: #fff0f6;
  border-radius: 20px;
  padding: 25px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}
h1 {
  text-align: center;
  color: #ff4d88;
  margin-bottom: 20px;
}
.countdown {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.box {
  background: #ffe6f0;
  border-radius: 12px;
  padding: 10px;
  width: 22%;
}
.number {
  font-size: 24px;
  font-weight: 600;
  color: #ff3366;
}
.label {
  font-size: 12px;
  color: #555;
}
p {
  margin: 12px 0;
  line-height: 1.6;
  opacity: 0;
  transform: translateY(15px);
  animation: fadeIn 1s forwards;
}
strong.nick { color: #ff3366; font-weight:600; }
@keyframes fadeIn { to {opacity:1; transform:translateY(0);} }
.questions { margin-top:20px; }
input[type="text"] { padding:8px 12px; border-radius:8px; border:1px solid #ccc; width:80%; margin-bottom:10px; }
button { padding:8px 16px; border-radius:8px; border:none; background-color:#ff4d88; color:white; cursor:pointer; }
.final-message { display:none; margin-top:20px; background:#fff0f6; padding:20px; border-radius:15px; }
</style>
</head>
<body>

<div class="container">
  <h1>Snehal 💖</h1>

  <div class="countdown" id="countdown">
    <div class="box"><div class="number" id="days">0</div><div class="label">Days</div></div>
    <div class="box"><div class="number" id="hours">0</div><div class="label">Hours</div></div>
    <div class="box"><div class="number" id="minutes">0</div><div class="label">Minutes</div></div>
    <div class="box"><div class="number" id="seconds">0</div><div class="label">Seconds</div></div>
  </div>

  <div class="letter" id="letter">
    <p><strong>Snehal,</strong></p>
    <p>Today is not just any day… it’s the day you turn 17, the day the world was blessed with <em>you</em>. I feel so lucky that I’ve known you since 6th standard — all the laughter, all the small moments, all the memories we’ve created together… I wouldn’t trade any of them for anything.</p>
    <p>I still remember that day in <strong>10th grade</strong>, your birthday, when I first held your hand on the bus while returning home. That tiny moment felt like the world had paused for <strong>uss</strong>, and it’s etched in my heart forever. And the <strong>first hug on 16th September 2024</strong>… I’ll never forget how perfect that felt.</p>
    <p>Since <strong>25th February 2024</strong>, we’ve been creating countless memories together. My <strong class="nick">sakhi</strong>, you’ve been my constant companion, my comfort, and the person who understands me like no one else. <strong>Uss</strong> journey with you has been the most beautiful adventure.</p>
    <p>My <strong class="nick">rasmalai</strong>, every time I see your smile, it feels like sunlight breaking through the clouds. You light up every space you’re in, and every moment with you becomes a memory I want to hold forever.</p>
    <p>My <strong class="nick">ladoo</strong>, your kindness, patience, and strength inspire me every day. You have this magical ability to make the world feel soft and safe.</p>
    <p>My <strong class="nick">dudu</strong>, being with you has taught me so much about love, friendship, and trust. You are my partner in every sense.</p>
    <p>And my <strong class="nick">raanisaheb</strong>, you are my queen in every little way — ruling my heart completely. Every memory we’ve made is engraved in my soul.</p>
    <p>Snehal, 17 is a beautiful age. It’s a time to dream bigger, laugh louder, love deeper, and embrace every part of yourself.</p>
    <p>Today, I want to remind you to <strong>take care of yourself</strong>, to cherish your happiness, and to know that I, <strong>Aashay</strong>, am always here. Every day with you is a gift, and I can’t wait for all the memories <strong>uss</strong> have yet to create.</p>
    <p>Happy 17th Birthday, my love. 💖</p>
    <p>With all my heart,<br><strong>Aashay</strong></p>
  </div>

  <div class="questions" id="questions">
    <p>Answer these questions before the final message:</p>
    <p>1. What do you wish for your 17th year?</p>
    <input type="text" id="q1"><br>
    <p>2. One thing you want to protect this year?</p>
    <input type="text" id="q2"><br>
    <p>3. What makes you feel happy and calm?</p>
    <input type="text" id="q3"><br>
    <button onclick="showFinal()">Submit Answers</button>
  </div>

  <div class="final-message" id="finalMessage">
    <h2>🎉 Happy 17th Birthday, Snehal 💖</h2>
    <p>May this year be gentle, joyful, and full of love. You deserve the world and more.</p>
  </div>
</div>

<script>
// Countdown logic
const birthday = new Date(2026,0,3,0,0,0);
function updateCountdown(){
  const now = new Date();
  const diff = birthday - now;
  const days = Math.floor(diff/(1000*60*60*24));
  const hours = Math.floor((diff/(1000*60*60))%24);
  const minutes = Math.floor((diff/(1000*60))%60);
  const seconds = Math.floor((diff/1000)%60);
  document.getElementById('days').innerText=days>=0?days:0;
  document.getElementById('hours').innerText=hours>=0?hours:0;
  document.getElementById('minutes').innerText=minutes>=0?minutes:0;
  document.getElementById('seconds').innerText=seconds>=0?seconds:0;
}
setInterval(updateCountdown,1000);
updateCountdown();

// Show final message after answering questions
function showFinal(){
  document.getElementById('questions').style.display='none';
  document.getElementById('finalMessage').style.display='block';
}
</script>

</body>
</html>
