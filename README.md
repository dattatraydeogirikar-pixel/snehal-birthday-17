# snehal-birthday-17
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Snehal's 17th Birthday 💖</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
  body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ffe6f0, #f3e8ff);
    color: #333;
    text-align: center;
    overflow-x: hidden;
  }
  .container {
    max-width: 500px;
    margin: 0 auto;
    padding: 20px;
  }
  .countdown {
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
    opacity: 0;
    transform: translateY(20px);
    transition: all 1s ease;
  }
  .countdown.show {
    opacity: 1;
    transform: translateY(0);
  }
  .box {
    background: #fff0f6;
    border-radius: 12px;
    padding: 12px;
    width: 22%;
  }
  .number {
    font-size: 24px;
    font-weight: 600;
    color: #ff4d88;
  }
  .label {
    font-size: 12px;
    color: #555;
  }
  .message, .final-message {
    margin-top: 20px;
    font-size: 14px;
    color: #555;
    opacity: 0;
    transform: translateY(20px);
    transition: all 1s ease;
  }
  .message.show, .final-message.show {
    opacity: 1;
    transform: translateY(0);
  }
  .photo {
    margin-top: 25px;
    border-radius: 20px;
    width: 80%;
    max-width: 300px;
    opacity: 0;
    transform: scale(0.9);
    transition: all 1s ease;
  }
  .photo.show {
    opacity: 1;
    transform: scale(1);
  }
  .password-section {
    margin-top: 25px;
    display: none;
    flex-direction: column;
    align-items: center;
    opacity: 0;
    transform: translateY(20px);
    transition: all 1s ease;
  }
  .password-section.show {
    display: flex;
    opacity: 1;
    transform: translateY(0);
  }
  input[type="password"] {
    padding: 8px 12px;
    border-radius: 8px;
    border: 1px solid #ccc;
    margin-top: 10px;
    width: 60%;
    font-size: 14px;
  }
  button {
    padding: 8px 16px;
    margin-top: 10px;
    border-radius: 8px;
    border: none;
    background-color: #ff4d88;
    color: white;
    font-size: 14px;
    cursor: pointer;
  }
  .letter, .questions, .final-birthday {
    display: none;
    margin-top: 25px;
    text-align: left;
    background: #fff0f6;
    padding: 20px;
    border-radius: 15px;
    font-size: 15px;
    color: #333;
  }
  .letter.show, .questions.show, .final-birthday.show {
    display: block;
    animation: fadeIn 1s ease;
  }
  .question {
    margin-top: 10px;
  }
  .question input {
    width: 95%;
    padding: 6px;
    margin-top: 4px;
    border-radius: 6px;
    border: 1px solid #ccc;
  }
  @keyframes fadeIn {
    from {opacity:0; transform: translateY(15px);}
    to {opacity:1; transform: translateY(0);}
  }
</style>
</head>
<body>

<div class="container">
  <h1>Snehal 💖</h1>
  <div class="message" id="initialMessage">
    Snehal, you’re turning 17! Take care of yourself and cherish every moment.
  </div>

  <div class="countdown" id="countdown">
    <div class="box"><div class="number" id="days">0</div><div class="label">Days</div></div>
    <div class="box"><div class="number" id="hours">0</div><div class="label">Hours</div></div>
    <div class="box"><div class="number" id="minutes">0</div><div class="label">Minutes</div></div>
    <div class="box"><div class="number" id="seconds">0</div><div class="label">Seconds</div></div>
  </div>

  <img src="<<YourPhotoFileName>>" alt="Snehal" class="photo" id="photo">

  <div class="password-section" id="passwordSection">
    <p>Enter the password to read your letter 💌</p>
    <input type="password" id="passwordInput" placeholder="Password">
    <button onclick="checkPassword()">Unlock Letter</button>
    <p id="passwordMsg" style="color:red;margin-top:5px;"></p>
  </div>

  <div class="letter" id="letter">
    <p><strong>Snehal,</strong></p>
    <p>Today is not just any day… it’s the day you turn 17, the day the world was blessed with <em>you</em>. I feel so lucky that I’ve known you since 6th standard — all the laughter, all the small moments, all the memories we’ve created together… I wouldn’t trade any of them for anything.</p>
    <p>I still remember that day in <strong>10th grade</strong>, your birthday, when I first held your hand on the bus while returning home. That tiny moment felt like the world had paused for <strong>uss</strong>, and it’s etched in my heart forever. And the <strong>first hug on 16th September 2024</strong>… I’ll never forget how perfect that felt. Each of these moments made me realize how truly special you are.</p>
    <p>Since <strong>25th February 2024</strong>, we’ve been creating countless memories together — laughter, silly jokes, quiet talks, teasing each other, sharing dreams, and supporting one another. My <strong>sakhi</strong>, you’ve been my constant companion, my comfort, and the person who understands me like no one else. <strong>Uss</strong> journey with you has been the most beautiful adventure.</p>
    <p>My <strong>rasmalai</strong>, every time I see your smile, it feels like sunlight breaking through the clouds. You light up every space you’re in, and every moment with you becomes a memory I want to hold forever. I love how naturally we can laugh together, how we can be goofy, serious, and romantic all at once.</p>
    <p>My <strong>ladoo</strong>, your kindness, patience, and strength inspire me every day. You have this magical ability to make the world feel soft and safe, and I hope you always remember to treat yourself with the same love and care that you give to everyone else.</p>
    <p>My <strong>dudu</strong>, being with you has taught me so much about love, friendship, and trust. You are my partner in every sense — the one who stands by me, who celebrates my highs and comforts me during lows, who makes ordinary days extraordinary.</p>
    <p>And my <strong>raanisaheb</strong>, you are my queen in every little way — ruling my heart completely. Every memory we’ve made, every moment we’ve shared, and every laugh, hug, and hand-hold is engraved in my soul. I feel so blessed to have you as my girlfriend, my best friend, my soulmate — my everything.</p>
    <p>Snehal, 17 is a beautiful age. It’s a time to dream bigger, laugh louder, love deeper, and embrace every part of yourself. I hope you never forget your worth, your strength, and your beauty — not just outside, but inside, where your soul shines brighter than anyone I’ve ever known.</p>
    <p>Today, I want to remind you to <strong>take care of yourself</strong>, to cherish your happiness, and to know that I, <strong>Aashay</strong>, am always here — not just as your boyfriend, but as your friend, your partner, your soul. Every day with you is a gift, and I can’t wait for all the memories <strong>uss</strong> have yet to create.</p>
  </div>

  <div class="questions" id="questions">
    <p>Before the final message, answer a few questions:</p>
    <div class="question">
      <label>1. What do you wish for your 17th year?</label>
      <input type="text" id="q1">
    </div>
    <div class="question">
      <label>2. One thing you want to protect this year?</label>
      <input type="text" id="q2">
    </div>
    <div class="question">
      <label>3. What makes you feel happy and calm?</label>
      <input type="text" id="q3">
    </div>
    <button onclick="showFinal()">Submit Answers</button>
  </div>

  <div class="final-birthday" id="finalBirthday">
    <h2>🎉 Happy 17th Birthday, Snehal 💖</h2>
    <p>May this year be gentle, joyful, and full of love. You deserve the world and more.</p>
  </div>
</div>

<audio id="bgMusic" loop autoplay>
  <source src="https://www.bensound.com/bensound-music/bensound-sunny.mp3" type="audio/mpeg">
</audio>

<script>
  const birthday = new Date(2026, 0, 3, 0, 0, 0);
  const password = "snehashay1303";

  const countdownEl = document.getElementById("countdown");
  const messageEl = document.getElementById("initialMessage");
  const photoEl = document.getElementById("photo");
  const passwordSection = document.getElementById("passwordSection");
  const letter = document.getElementById("letter");
  const questions = document.getElementById("questions");
  const finalBirthday = document.getElementById("finalBirthday");

  function updateCountdown() {
    const now = new Date();
    const diff = birthday - now;

    if (diff <= 0) {
      countdownEl.style.display = "none";
      messageEl.classList.add("show");
      photoEl.classList.add("show");
      passwordSection.classList.add("show");
      clearInterval(timer);
      return;
    }

    const days = Math.floor(diff / (1000*60*60*24));
    const hours = Math.floor((diff / (1000*60*60)) % 24);
    const minutes = Math.floor((diff / (1000*60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    document.getElementById("days").innerText = days;
    document.getElementById("hours").innerText = hours;
    document.getElementById("minutes").innerText = minutes;
    document.getElementById("seconds").innerText = seconds;
  }

  const timer = setInterval(updateCountdown, 1000);
  updateCountdown();
  countdownEl.classList.add("show");
  messageEl.classList.add("show");
  photoEl.classList.add("show");

  function checkPassword() {
    const input = document.getElementById("passwordInput").value;
    const msg = document.getElementById("passwordMsg");
    if(input === password) {
      passwordSection.style.display = "none";
      letter.classList.add("show");
      questions.classList.add("show");
    } else {
      msg.innerText = "Incorrect password. Try again!";
    }
  }

  function showFinal() {
    questions.style.display = "none";
    finalBirthday.classList.add("show");
  }
</script>

</body>
</html>
