<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snehal's 17th Birthday</title>
<style>
body {
  font-family: Arial, sans-serif;
  background: #ffe6f0;
  color: #333;
  text-align: center;
  padding: 20px;
}
.container {
  max-width: 700px;
  margin: 0 auto;
  background: #fff0f6;
  padding: 20px;
  border-radius: 15px;
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
}
section { display: none; }
</style>
</head>
<body>

<div class="container">

<!-- 1. Birthday Message -->
<section id="intro" style="display:block;">
<h1>Happy 17th Birthday, Snehal! 💖</h1>
<p>Dear Snehal, wishing you a day filled with love, laughter, and all the happiness in the world. You are my sakhi, rasmalai, ladoo, dudu, raanisaheb, and my most precious person.</p>
<button onclick="nextSection('letter')">Read Letter 💌</button>
</section>

<!-- 2. Letter -->
<section id="letter">
<p><strong>Snehal,</strong></p>
<p>Today is the day you turn 17, the day the world was blessed with <em>you</em>. I feel so lucky knowing you since 6th standard — all the laughter, moments, and memories we've created together.</p>
<p>I remember holding your hand for the first time in 10th grade, your birthday. That tiny moment felt magical. And the first hug on 16th September 2024 — unforgettable.</p>
<p>Since 25th February 2024, we've been making countless memories. My sakhi, rasmalai, ladoo, dudu, raanisaheb — you are my partner, my soul, my everything.</p>
<p>Take care of yourself and know that I, Aashay, am always here. Happy 17th Birthday, my love 💖</p>
<button onclick="nextSection('questions')">Next ➡️</button>
</section>

<!-- 3. Questions -->
<section id="questions">
<p>Answer these questions:</p>

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

<button onclick="submitAnswers()">Submit Answers</button>
</section>

<!-- 4. Final Message -->
<section id="final">
<h1>🎉 Happy 17th Birthday, Snehal 💖</h1>
<p>May this year be full of love, joy, and unforgettable memories. You deserve the world!</p>
</section>

</div>

<script>
function nextSection(id) {
  document.querySelectorAll('section').forEach(s => s.style.display='none');
  document.getElementById(id).style.display='block';
}

function submitAnswers() {
  const q1 = document.querySelector('input[name="q1"]:checked');
  const q2 = document.querySelector('input[name="q2"]:checked');
  const q3 = document.querySelector('input[name="q3"]:checked');
  
  if (!q1 || !q2 || !q3) {
    alert("Please answer all questions!");
    return;
  }
  nextSection('final');
}
</script>

</body>
</html>
