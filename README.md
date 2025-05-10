
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hakiman - Portofolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }

    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Poppins', sans-serif;
      color: white;
      text-align: center;
      background: black url('alok3.gif') no-repeat center center fixed;
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      max-width: 500px;
      padding: 20px;
    }

    .profile-img {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border-radius: 50%;
      border: 3px solid white;
      margin-bottom: 20px;
    }

    .name-container {
      font-size: 1.8em;
      margin-bottom: 10px;
      min-height: 2em;
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

    p {
      font-size: 14px;
      color: #ccc;
      margin-top: 5px;
      margin-bottom: 20px;
      padding: 0 10px;
    }

    .social-icons {
      margin-top: 20px;
    }

    .social-icons a img {
      width: 100px;
      margin: 0 5px;
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

    @media (max-width: 480px) {
      .container {
        padding: 40px 10px;
      }

      .profile-img {
        width: 100px;
        height: 100px;
      }

      .name-container {
        font-size: 1.5em;
      }

      p {
        font-size: 13px;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <img src="ui11.png" alt="Foto Profil" class="profile-img" />
    <div class="name-container">
      <div id="nameDisplay" class="typing-text">HAKIMAN NURHOLIS</div>
    </div>
    <p>INFORMATICS ENTHUSIAST TECH_GENERALIST | GAME | CYBER | CODE</p>

    <div class="social-icons">
      <a href="https://www.tiktok.com/@hans_.py?_t=ZS-8wFFLQvU5Bf&_r=1" target="_blank"><img src="tiktok1.png" alt="TikTok"></a>
      <a href="https://www.instagram.com/hakiman_nurkholis" target="_blank"><img src="ig.png" alt="Instagram"></a>
      <a href="https://www.youtube.com/@Hans.pyyyyy" target="_blank"><img src="yt.png" alt="YouTube"></a>
      <a href="https://github.com/hans_.pyy/" target="_blank"><img src="gt.png" alt="GitHub"></a>
      <a href="https://t.me/hans_.py" target="_blank"><img src="tl.png" alt="Telegram"></a>
      <a href="https://www.facebook.com/profile.php?id=61576289065160" target="_blank"><img src="fb.png" alt="Facebook"></a>
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
