<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snehal's 17th Birthday 💖</title>
<style>
body {
  margin:0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ffe6f0, #f3e8ff);
  color: #333;
  text-align: center;
  padding:20px;
}
.container {
  max-width:700px;
  margin:0 auto;
  background:#fff0f6;
  border-radius:20px;
  padding:25px;
  box-shadow:0 8px 25px rgba(0,0,0,0.15);
}
h1 {
  color:#ff4d88;
  margin-bottom:20px;
}
p {
  margin:12px 0;
  line-height:1.6;
}
strong.nick { color:#ff3366; font-weight:600; }
button { padding:10px 18px; border-radius:8px; border:none; background-color:#ff4d88; color:white; cursor:pointer; margin-top:15px; font-size:16px; }
</style>
</head>
<body>

<div class="container" id="mainContainer">

<!-- 1. Small Birthday Message -->
<div id="introSection">
<h1>Happy 17th Birthday, Snehal! 💖</h1>
<p>Dear Snehal, wishing you a day filled with love, laughter, and all the happiness in the world. You are my sakhi, rasmalai, ladoo, dudu, raanisaheb, and my most precious person. 💖</p>
<button onclick="showLetter()">Read Letter 💌</button>
</div>

<!-- 2. Full Letter -->
<div id="letterSection" style="display:none;">
<p><strong>Snehal,</strong></p>
<p>Today is not just any day… it’s the day you turn 17, the day the world was blessed with <em>you</em>. I feel so lucky that I’ve known you since 6th standard — all the laughter, all the small moments, all the memories we’ve created together… I wouldn’t trade any of them for anything.</p>
<p>I still remember that day in <strong>10th grade</strong>, your birthday, when I first held your hand on the bus while returning home. That tiny moment felt like the world had paused for <strong>uss</strong>, and it’s etched in my heart forever. And the <strong>first hug on 16th September 2024</strong>… I’ll never forget how perfect that felt.</p>
<p>Since <strong>25th February 2024</strong>, we’ve been creating countless memories together. My <strong class="nick">sakhi</strong>, you’ve been my constant companion, my comfort, and the person who understands me like no one else. <strong>Uss</strong> journey has been the most beautiful adventure.</p>
<p>My <strong class="nick">rasmalai</strong>, every time I see your smile, it feels like sunlight breaking through the clouds. You light up every space you’re in, and every moment with you becomes a memory I want to hold forever.</p>
<p>My <strong class="nick">ladoo</strong>, your kindness, patience, and strength inspire me every day. You have this magical ability to make the world feel soft and safe.</p>
<p>My <strong class="nick">dudu</strong>, being with you has taught me so much about love, friendship, and trust. You are my partner in every sense.</p>
<p>And my <strong class="nick">raanisaheb</strong>, you are my queen in every little way — ruling my heart completely. Every memory we’ve made is engraved in my soul.</p>
<p>Snehal, 17 is a beautiful age. It’s a time to dream bigger, laugh louder, love deeper, and embrace every part of yourself.</p>
<p>Today, I want to remind you to <strong>take care of yourself</strong>, to cherish your happiness, and to know that I, <strong>Aashay</strong>, am always here. Every day with you is a gift, and I can’t wait for all the memories <strong>uss</strong> have yet to create.</p>
<p>Happy 17th Birthday, my love. 💖</p>
<button onclick="showQuestions()">Next ➡️</button>
</div>

<!-- 3. Questions -->
<div id="questionsSection" style="display:none;">
<p>Answer these questions before the final birthday message:</p>

<p>1. What do you wish for your 17th year?</p>
<label><input type="radio" name="q1" value="Happiness"> Happiness</label>
<label><input type="radio" name="q1" value="Success"> Success</label>
<label><input type="radio" name="q1" value="Adventure"> Adventure</label>

<p>2. One thing you want to protect this year?</p>
<label><input type="radio" name="q2" value="Friendship"> Friendship</label>
<label><input type="radio" name="q2" value="Love"> Love</label>
<label><input type="radio" name="q2" value="Health"> Health</label>

<p>3. What makes you feel happy and calm?</p>
<label><input type="radio" name="q3" value="Music"> Music</label>
<label><input type="radio" name="q3" value="Reading"> Reading</label>
<label><input type="radio" name="q3" value="Nature"> Nature</label>

<button onclick="showFinal()">Submit Answers</button>
</div>

<!-- 4. Final Message -->
<div id="finalMessage" style="display:none;">
<h2>🎉 Happy 17th Birthday, Snehal 💖</h2>
<p>May this year be gentle, joyful, and full of love. You deserve the world and more.</p>
</div>

</div>

<script>
function showLetter(){
  document.getElementById('introSection').style.display='none';
  document.getElementById('letterSection').style.display='block';
}
function showQuestions(){
  document.getElementById('letterSection').style.display='none';
  document.getElementById('questionsSection').style.display='block';
}
function showFinal(){
  const q1 = document.querySelector('input[name="q1"]:checked');
  const q2 = document.querySelector('input[name="q2"]:checked');
  const q3 = document.querySelector('input[name="q3"]:checked');

  if(!q1 || !q2 || !q3){
    alert("Please answer all questions before submitting!");
    return;
  }

  document.getElementById('questionsSection').style.display='none';
  document.getElementById('finalMessage').style.display='block';
}
</script>

</body>
</html>
