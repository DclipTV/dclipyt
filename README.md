<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DclipTV - Gaming Universe</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background:rgb(0, 0, 0);
      color: #00ffcc;
      overflow-x: hidden;
    }
    header {
      background: #111;
      text-align: center;
      padding: 2rem 1rem;
    }
    header h1 {
      font-size: 3rem;
      color: #00ffcc;
      margin: 0;
    }
    nav {
      text-align: center;
      margin-top: 1rem;
    }
    nav a {
      color: #00ffcc;
      text-decoration: none;
      margin: 0 1rem;
      font-size: 1.2rem;
    }
    nav a:hover {
      text-decoration: underline;
    }
    .container {
      text-align: center;
      padding: 4rem 2rem;
    }
    .video-wrapper iframe {
      width: 90%;
      max-width: 800px;
      height: 450px;
      border: none;
      margin-top: 2rem;
    }
    footer {
      text-align: center;
      padding: 2rem;
      background: #111;
      color: #00ffcc;
      font-size: 0.9rem;
    }
    .social-links a {
      margin: 0 0.5rem;
      color: #00ffcc;
      font-size: 1.5rem;
      text-decoration: none;
    }
    .mascotte {
      margin-top: 3rem;
      max-width: 250px;
      width: 80%;
      border-radius: 1rem;
      box-shadow: 0 0 20pxhsl(168, 100.00%, 50.00%);
    }
    .mascotte {
      max-width: 300px;
      transition: transform 0.3s ease;
    }
    .mascotte:hover {
      transform: scale(1.05);
    }
    #musicControl {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background:rgb(29, 29, 29);
      padding: 10px;
      border-radius: 10px;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <header>
    <h1>Bienvenue sur DclipTV</h1>
    <nav>
      <a href="#youtube">YouTube</a>
      <a href="#twitch">Twitch</a>
      <a href="#tiktok">TikTok</a>
    </nav>
  </header>

  <div class="container">
    <p>Le monde de DclipTV vous ouvre ses portes !</p>
    <div class="video-wrapper" id="youtube">
      <h2>YouTube</h2>
      <iframe src="https://www.youtube.com/embed/videoseries?list=PLQXtqMH6TzOEbhtOJkmCUD7iyMRVdIdlX" allowfullscreen></iframe>
    </div>

<div class="video-wrapper" id="twitch">
  <h2>Twitch Live</h2>
  <iframe
    src="https://player.twitch.tv/?channel=dclipyt&parent=dcliptv.github.io"
    height="480"
    width="720"
    frameborder="0"
    allowfullscreen>
  </iframe>
</div>

<div class="video-wrapper" id="tiktok">
  <h2>TikTok</h2>
  <p>
    <a href="https://www.tiktok.com/@dclipyt" target="_blank">
      Voir mes TikToks
    </a>
  </p>
</div>

<img src="mascotte-pixelia.png" alt="Mascotte IA Vtuber Pixelia" class="mascotte">

<p id="mascotteMessage">Passe ta souris sur moi !</p>
</div>
<div id="musicControl">Musique : ON</div>
  <audio id="bgMusic" loop>
    <source src="/musique.mp3" type="audio/mpeg">
    Votre navigateur ne supporte pas l'audio.
  </audio>

  <script>
    const music = document.getElementById('bgMusic');
    const control = document.getElementById('musicControl');
    let playing = false;
    control.onclick = () => {
      playing = !playing;
      if (playing) {
        music.play();
        control.textContent = 'Musique : OFF';
      } else {
        music.pause();
        control.textContent = 'Musique : ON';
      }
    };

    const mascotte = document.getElementById('mascotte');
    const message = document.getElementById('mascotteMessage');
    mascotte.addEventListener('mouseover', () => {
      const phrases = [
        "Salut joueur légendaire !",
        "Tu veux un tuto OP ? Suis-moi !",
        "N'oublie pas de t'abonner !",
        "Team kawaii gamer !"
      ];
      const phrase = phrases[Math.floor(Math.random() * phrases.length)];
      message.textContent = phrase;
    });
    mascotte.addEventListener('mouseout', () => {
      message.textContent = 'Passe ta souris sur moi !';
    });
    const mascotte = document.getElementById('mascotte');
    const message = document.getElementById('mascotteMessage');
    mascotte.addEventListener('mouseover', () => {
      const phrases = [
        "Salut joueur légendaire !",
        "Tu veux un tuto OP ? Suis-moi !",
        "N'oublie pas de t'abonner !",
        "Team kawaii gamer !"
      ];
      const phrase = phrases[Math.floor(Math.random() * phrases.length)];
      message.textContent = phrase;
    });
    mascotte.addEventListener('mouseout', () => {
      message.textContent = 'Passe ta souris sur moi !';
    });
    </script>

<div class="section" id="about">
    <h2>À propos</h2>
    <p>Je suis Dclip, passionné(e) de gaming ! Ici tu trouveras mes lives, tutos et une ambiance chill !</p>
  </div>










 <footer>
    <p>DclipTV © 2025 - Tous droits réservés</p>
    <div class="social-links">
      <a href="https://www.youtube.com/channel/UCWW5K2obNOiRlcD7f469GgA" target="_blank">YouTube</a>
      <a href="https://www.twitch.tv/dclipyt" target="_blank">Twitch</a>
      <a href="https://www.tiktok.com/@dclipyt" target="_blank">TikTok</a>
    </div>
  </footer>
</body>
</html>