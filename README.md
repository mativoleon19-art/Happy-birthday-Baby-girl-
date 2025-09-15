<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday 💜</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #e0c3fc, #8ec5fc);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }
  .screen {
    display: none;
    text-align: center;
    padding: 25px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 6px 25px rgba(0,0,0,0.15);
    width: 90%;
    max-width: 500px;
    transition: opacity 0.5s ease;
  }
  .screen.active {
    display: block;
    opacity: 1;
  }
  button {
    background-color: #a020f0;
    color: white;
    border: none;
    padding: 12px 25px;
    margin: 10px;
    border-radius: 12px;
    cursor: pointer;
    font-size: 16px;
  }
  button:hover {
    background-color: #8500c0;
  }
</style>
</head>
<body>

<div id="screen1" class="screen active">
  <h1>Happy Birthday, Hope! 💜</h1>
  <p>Hey babe, I made something special just for you ❤️</p>
  <button onclick="nextScreen()">Next</button>
</div>

<div id="screen2" class="screen">
  <h2>Let's start the quiz!</h2>
  <p>Question 1: Do you love me?</p>
  <button onclick="nextQuestion(3)">Yes 😘</button>
  <button onclick="nextQuestion(3)">Of course 💖</button>
</div>

<div id="screen3" class="screen">
  <p>Question 2: Have you ever felt uncomfortable with me?</p>
  <button onclick="nextQuestion(4)">Never 😇</button>
  <button onclick="nextQuestion(4)">Not really 😌</button>
</div>

<div id="screen4" class="screen">
  <p>Question 3: Who is the boss?</p>
  <button onclick="nextQuestion(5)">You 😉</button>
  <button onclick="nextQuestion(5)">Me 😎</button>
</div>

<div id="screen5" class="screen">
  <p>Question 4: Who is always mysterious?</p>
  <button onclick="showFinal()">You 😏</button>
  <button onclick="showFinal()">Me 🤫</button>
</div>

<div id="finalScreen" class="screen">
  <h2>The Best Girlfriend Ever 💗</h2>
  <p>Hope, you’re amazing and I love you so much! Your cute chubby cheeks, sweet smile, and dangerous laughter make my heart melt 😘</p>
</div>

<script>
function nextScreen() {
  document.getElementById('screen1').classList.remove('active');
  document.getElementById('screen2').classList.add('active');
}

function nextQuestion(nextId) {
  const current = document.querySelector('.screen.active');
  current.classList.remove('active');
  const next = document.getElementById('screen' + nextId);
  next.classList.add('active');
}

function showFinal() {
  const current = document.querySelector('.screen.active');
  current.classList.remove('active');
  document.getElementById('finalScreen').classList.add('active');
}
</script>

</body>
</html>
