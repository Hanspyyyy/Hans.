
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hakiman - Portofolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap" rel="stylesheet">
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Poppins', sans-serif;
      color: white;
      text-align: center;
      background: black url('https://yourdomain.com/alok3.gif') no-repeat center center fixed;
      background-size: cover;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .container {
      z-index: 3;
      padding: 20px;
    }

    .profile-img {
      width: 100px;
      border-radius: 100%;
      border: 3px solid white;
    }

    .name-container {
      margin-top: 10px;
      font-size: 1.8em;
    }

    .typing-text {
      display: inline-block;
      white-space: nowrap;
      overflow: hidden;
      animation: typing 2s steps(30, end);
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    .fade-out {
      animation: fadeOut 0.5s forwards;
    }

    .fade-in {
      animation: fadeIn 0.5s forwards, typing 2s steps(30, end);
    }

    @keyframes fadeOut {
      from { opacity: 1; transform: translateX(0); }
      to { opacity: 0; transform: translateX(100px); }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateX(-100px); }
      to { opacity: 1; transform: translateX(0); }
    }

    .social-icons {
      margin-top: 15px;
      flex-wrap: wrap;
    }

    .social-icons a img {
      width: 30px;
      margin: 8px;
      filter: brightness(0) invert(1);
      transition: transform 0.3s;
    }

    .social-icons a img:hover {
      transform: scale(1.2);
    }

    .buttons {
      margin-top: 30px;
    }

    .buttons a {
      display: block;
      margin: 10px auto;
      padding: 12px 24px;
      width: 80%;
      max-width: 250px;
      background: white;
      color: black;
      text-decoration: none;
      border-radius: 30px;
      font-weight: bold;
      transition: transform 0.2s;
    }

    .buttons a:hover {
      transform: scale(1.05);
    }
  </style>
</head>
<body>

  <div class="container">
    <img src="https://yourdomain.com/ui11.png" alt="Foto Profil" class="profile-img" />
    <div class="name-container">
      <div id="nameDisplay" class="typing-text">HAKIMAN NURHOLIS</div>
    </div>
    <p>INFORMATICS ENTHUSIAST 
       TECH>_GENERALIS | GAME | CYBER | CODE</p>

    <div class="social-icons">
      <a href="https://www.tiktok.com/@hans_.py" target="_blank"><img src="https://yourdomain.com/tiktok1.png" alt="TikTok"></a>
      <a href="https://www.instagram.com/hakiman_nurkholis" target="_blank"><img src="https://yourdomain.com/ig.png" alt="Instagram"></a>
      <a href="https://www.youtube.com/@Hans.pyyyyy" target="_blank"><img src="https://yourdomain.com/yt.png" alt="YouTube"></a>
      <a href="https://github.com/hans-.pyy" target="_blank"><img src="https://yourdomain.com/gt.png" alt="GitHub"></a>
      <a href="https://t.me/hans_.py" target="_blank"><img src="https://yourdomain.com/tl.png" alt="Telegram"></a>
      <a href="https://www.facebook.com/profile.php?id=61576289065160" target="_blank"><img src="https://yourdomain.com/fb.png" alt="Facebook"></a>
    </div>

    <div class="buttons">
      <a href="https://piandi.vercel.app" target="_blank">Portofolio</a>
      <a href="https://piandi.vercel.app/#achievements" target="_blank">Pencapaian</a>
      <a href="https://piandi.vercel.app/hans-freefire" target="_blank">Game Hans</a>
    </div>
  </div>

  <script>
    const nameElement = document.getElementById("nameDisplay");
    const names = ["HAKIMAN NURHOLIS", "HANS"];
    let currentIndex = 0;

    function switchName() {
      nameElement.classList.remove("fade-in");
      nameElement.classList.add("fade-out");

      setTimeout(() => {
        currentIndex = (currentIndex + 1) % names.length;
        nameElement.textContent = names[currentIndex];
        nameElement.classList.remove("fade-out");
        void nameElement.offsetWidth;
        nameElement.classList.add("fade-in");
      }, 500);
    }

    setInterval(switchName, 5000);
  </script>

</body>
</html>
