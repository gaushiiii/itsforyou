<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Will You Be My Boyfriend?</title>
  <style>
    body {
  font-family: Arial, sans-serif;
  background-color: #f9f9f9;
}

header {
  background-color: #ff69b4;
  color: #fff;
  padding: 20px;
  text-align: center;
}

main {
  max-width: 800px;
  margin: 40px auto;
  padding: 20px;
  background-color: #fff;
  border: 1px solid #ddd;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.message {
  padding: 20px;
  text-align: center;
}

.message h2 {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 3rem;
  line-height: 1.2;
}

.message p {
  margin-bottom: 20px;
  font-size: 1.2rem;
  line-height: 1.5;
}

#proposal-btn {
  background-color: #ff69b4;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1.2rem;
  transition: background-color 0.3s ease;
}

#proposal-btn:hover {
  background-color: #ff7eb9;
}

.response {
  display: none;
  padding: 20px;
  background-color: #fff;
  border: 1px solid #ddd;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.response h2 {
  font-weight: bold;
  color: #00698f;
  font-size: 3rem;
  line-height: 1.2;
}

.heart-eyes {
  width: 50px;
  height: 50px;
  margin: 20px auto;
}

.confetti {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  pointer-events: none;
  overflow: hidden;
}

.confetti__piece {
  position: absolute;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #ff69b4;
  animation: confetti-animation 10s linear infinite;
}

@keyframes confetti-animation {
  0% {
    transform: translateY(-100%) rotate(0);
    opacity: 1;
  }
  100% {
    transform: translateY(100%) rotate(360deg);
    opacity: 0;
  }
}
  </style>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Will You Be My Boyfriend?</h1>
  </header>
  <main>
    <section class="message">
      <h2>Dear [Boyfriend's Name],</h2>
      <p>You're the cream cheese to my bagel, the Merlot to my pizza night, and the Netflix to my binge-watching habits.</p>
      <p>I was thinking, maybe we could take our relationship to the next level? I'd love to spend the rest of my life making memories with you, laughing at my dad jokes, and stealing the covers at night.</p>
      <button id="proposal-btn">Will you be my boyfriend?</button>
    </section>
    <section class="response">
      <h2 id="response-txt"></h2>
      <img src="heart-eyes-emoji.png" alt="Heart eyes emoji" class="heart-eyes">
    </section>
    <div class="confetti"></div>
  </main>
  <script >
    const proposalBtn = document.getElementById('proposal-btn');
const responseTxt = document.getElementById('response-txt');
const responseSection = document.querySelector('.response');
const confettiContainer = document.querySelector('.confetti');

proposalBtn.addEventListener('click', () => {
  responseSection.style.display = 'block';
  responseTxt.textContent = 'YES!';

  // Add confetti animation
  const confettiPieces = 100;
  for (let i = 0; i < confettiPieces; i++) {
    const confettiPiece = document.createElement('div');
    confettiPiece.classList.add('confetti__piece');
    confettiContainer.appendChild(confettiPiece);
  }
});
  </script>
</body>
</html>
