<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>İyi Geceler Birtanemmmmm 🌙</title>
  <style>
  .menu {
  width: 100%;
  background-color: #66bb6a; /* Menü rengi */
  padding: 10px 0;
  display: flex;
  justify-content: center;
  gap: 30px;
  position: fixed; /* Menü sabit kalsın */
  top: 0;
  left: 0;
  z-index: 1000; /* Her şeyin üstünde olsun */
}

.menu a {
  text-decoration: none;
  color: white;
  font-weight: bold;
  font-size: 1.2rem;
  transition: color 0.3s;
}

.menu a:hover {
  color: #2e7d32; /* Üzerine gelince renk değişsin */
}

    body {
	
       margin: 0;
  padding: 80px 0 0 0; /* üst boşluk eklendi */
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(to bottom, #a8e6cf, #dcedc1);
  color: #2e7d32;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  text-align: center;
  overflow: hidden;
    }

    .photo-frame {
      border: 5px solid #66bb6a;
      border-radius: 20px;
      overflow: hidden;
      width: 300px;
      height: 400px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
      margin-bottom: 20px;
    }

    .photo-frame img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    p {
      font-size: 1.2rem;
      max-width: 500px;
      margin: 0 auto;
    }

    .heart {
      font-size: 2rem;
      color: #c62828;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    /* Kalpler için */
    .hearts-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
    }

    .falling-heart {
      position: absolute;
      top: -50px;
      color: #ff1744;
      font-size: 1.5rem;
      animation: fall linear infinite;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

<nav class="menu">
  <a href="#">Ana Sayfa</a>
<a href="hakkımda.html">Hakkımda</a>
  <a href="#">Galeri</a>
  <a href="#">İletişim</a>
</nav>

  <!-- Kalp efektleri konteyneri -->
  <div class="hearts-container" id="hearts"></div>

  <div class="photo-frame">
    <img src="sevgilim.jpg" alt="Sevgilim">
  </div>

  <h1>İyi Geceler Aşkım 🌙</h1>
  <p>Gülüşün gönlümü o kadar ısıtıyor ki sönmeyen ateşe inanmaya başladım 💚💚💚💚💚💚</p>
  <div class="heart">❤</div>

  <script>
    const heartsContainer = document.getElementById("hearts");

    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("falling-heart");
      heart.innerText = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (2 + Math.random() * 2) + "s";
      heart.style.fontSize = (4+ Math.random() * 3) + "rem"; // daha büyük kalpler
      heartsContainer.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }

    // Kalpler artık her 100ms'de bir gelecek (daha sık)
    setInterval(createHeart, 100);
  </script>


</body>
</html>
