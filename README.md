<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Birthday Matt</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet" />
  <style>
    body {
      font-family: 'Quicksand', sans-serif;
      margin: 0;
      background: linear-gradient(to bottom right, #fff5f8, #ffe4ec);
      color: #3a3a3a;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 30px 20px;
      animation: fadeIn 1.5s ease-in;
      overflow-x: hidden;
    }
    h1 {
      font-family: 'Pacifico', cursive;
      font-size: 3em;
      color: #e75480;
      text-align: center;
      margin-bottom: 0.5em;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
    }
    .letter {
      max-width: 700px;
      background: #fff0f5;
      border-radius: 20px;
      padding: 25px;
      margin: 20px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      font-size: 1.1em;
      line-height: 1.7;
      color: #6c3a4c;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      margin: 30px 0;
      max-width: 1000px;
      width: 100%;
      animation: slideUp 1s ease-out;
    }
    .gallery img {
      width: 100%;
      border-radius: 18px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
      transition: transform 0.3s, box-shadow 0.3s;
      object-fit: cover;
      height: 340px;
      background: #e8e8e8;
    }
    .gallery img:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 20px rgba(0, 0, 0, 0.2);
    }
    .music {
      margin-top: 50px;
      text-align: center;
      animation: fadeIn 2s ease-in;
      background: #ffffffaa;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 6px 14px rgba(0,0,0,0.1);
      max-width: 600px;
    }
    .music h2 {
      font-size: 1.8em;
      margin-bottom: 10px;
      color: #d14f7b;
    }
    .music p {
      font-size: 1em;
      margin-bottom: 20px;
      color: #7a4c61;
    }
    audio {
      margin: 10px;
      width: 100%;
    }
    .gif {
      margin: 40px 0 10px;
      text-align: center;
    }
    .gif img {
      width: 220px;
      border-radius: 12px;
    }
    .hearts {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      pointer-events: none;
      overflow: hidden;
      z-index: 1;
    }
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: #ff6fa5;
      clip-path: polygon(50% 0%, 100% 35%, 75% 100%, 25% 100%, 0% 35%);
      opacity: 0.7;
      animation: drop 5s infinite;
    }
    @keyframes drop {
      to {
        transform: translateY(100vh);
        opacity: 0;
      }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes slideUp {
      from { transform: translateY(40px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>
<body>
  <h1>Happy birthday my bby Matt &lt;3</h1>

  <div class="letter">
    <p>My dearest Matt,</p>
    <p>Happy birthday to the most wonderful person in my life. You make my world brighter with your laughter, your kindness, and the music that flows from your soul. I’m endlessly grateful for every moment we share every look that says more than words.</p>
    <p>You are the calm to my chaos, the melody to my lyrics, and the best part of every day. I hope this little website reminds you how much you're loved and cherished. Here's to more memories, more songs, more kisses, and a life as beautiful as your heart.</p>
    <p>Love forever,<br />Nook ♡</p>
  </div>

  <div class="gallery">
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_1076.JPEG" alt="Memory 1" />
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_1152.JPEG" alt="Memory 2" />
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_1168.JPEG" alt="Memory 3" />
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_1176.JPEG" alt="Memory 4" />
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_1538.JPEG" alt="Memory 5" />
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_1919.JPEG" alt="Memory 6" />
    <img src="https://github.com/nnoookp/Mattbd/blob/ad90192a66c1550128adc1358245a0d9b23989de/IMG_9725.JPEGG" alt="Memory 7" />
  </div>

  <div class="music">
    <h2>Your Birthday Song 🎵</h2>
    <p>(Just one, but it's from the heart 💗)</p>
    <audio controls>
      <source src="2025-05-19-20-55-22.m4a" type="audio/mp4" />
      Your browser does not support the audio element.
    </audio>
  </div>

  <div class="hearts" id="hearts"></div>

  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (2 + Math.random() * 3) + 's';
      document.getElementById('hearts').appendChild(heart);
      setTimeout(() => heart.remove(), 5000);
    }
    setInterval(createHeart, 300);
  </script>
</body>
</html>
