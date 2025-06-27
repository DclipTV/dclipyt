<!DOCTYPE html>
<html lang="fr">
<head>
    <base target="_self">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaming Portal - GitHub Version</title>
    <meta name="description" content="Portail gaming compatible GitHub Pages">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Roboto:wght@400;700&display=swap');
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #0f0e17;
            color: #fffffe;
        }
        .vtuber-container {
            transition:transform 0.3s ease;
        }
        .vtuber-container:hover {
            transform: scale(1.05);
        }
    </style>
</head>
<body class="min-h-screen relative">
    <!-- Audio Player -->
    <audio id="bgMusic" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Votre navigateur ne supporte pas l'audio.
    </audio>
    <!-- Bouton Musique -->
    <button id="musicToggle" class="fixed bottom-6 right-6 bg-pink-600 hover:bg-pink-700 text-white px-4 py-2 rounded-full z-50 shadow-lg">
        <i class="fas fa-music"></i> Musique : ON
    </button>
    <!-- Dialogue de la mascotte -->
    <div id="vtuberDialog" class="fixed bottom-32 right-6 bg-pink-700 text-white p-4 rounded-lg shadow-lg max-w-xs hidden z-40">
        <p id="dialogText">Salut ! Je suis ta mascotte kawaii !</p>
    </div>
    <header class="bg-gradient-to-r from-purple-900 to-indigo-800 py-4 shadow-lg">
        <div class="container mx-auto px-4 flex flex-col md:flex-row justify-between items-center">
            <h1 class="text-2xl md:text-3xl font-bold mb-4 md:mb-0" style="font-family: 'Press Start 2P', cursive;">
                <span class="text-pink-400">Gaming</span>Portal
            </h1>
            <nav>
                <ul class="flex space-x-4 md:space-x-6 flex-wrap justify-center">
                    <li><a href="#home" class="hover:text-pink-400 transition">Accueil</a></li>
                    <li><a href="#twitch" class="hover:text-pink-400 transition">Twitch</a></li>
                    <li><a href="#youtube" class="hover:text-pink-400 transition">YouTube</a></li>
                    <li><a href="#about" class="hover:text-pink-400 transition">À propos</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <main class="container mx-auto px-4 py-8">
        <section id="home" class="mb-12">
            <div class="text-center mb-8">
                <h2 class="text-3xl font-bold mb-4 text-pink-400">Bienvenue sur mon portail gaming !</h2>
                <p class="text-xl">Retrouvez tous mes contenus gaming au même endroit</p>
            </div>
            <!-- Mascotte Vtuber interactive -->
            <div class="flex justify-center mb-12">
                <div class="vtuber-container text-center"
                     onmouseenter="showRandomMessage()"
                     onclick="showMessage('Tu veux jouer avec moi ? 🎮')">
                    <img src="https://i.imgur.com/JQ9w0VK.png"
                         alt="AI Vtuber Kawaii"
                         class="w-48 md:w-64 h-auto mx-auto"
                         id="vtuberImage">
                    <p class="mt-4 text-pink-300 font-bold">Salut ! Je suis ta mascotte Vtuber !</p>
                </div>
            </div>
        </section>
        <section id="twitch" class="mb-12">
            <h2 class="text-2xl font-bold mb-6 text-pink-400">Ma chaîne Twitch</h2>
            <div class="bg-gray-800 rounded-lg p-4 shadow-lg">
                <div class="aspect-w-16 aspect-h-9 bg-black rounded-lg overflow-hidden mb-4 flex items-center justify-center">
                    <a href="https://www.twitch.tv/votre_chaine" target="_blank" rel="noopener" class="text-center p-8">
                        <i class="fab fa-twitch text-6xl text-purple-500 mb-4"></i>
                        <p class="text-xl">Regardez mon live sur Twitch</p>
                        <p class="text-pink-400 mt-2">Cliquez ici pour accéder à ma chaîne</p>
                    </a>
                </div>
                <div class="p-4">
                    <h3 class="text-xl font-bold mb-2">Horaires de stream</h3>
                    <ul class="space-y-2">
                        <li class="flex justify-between"><span>Lundi</span><span>18h - 22h</span></li>
                        <li class="flex justify-between"><span>Mercredi</span><span>18h - 22h</span></li>
                        <li class="flex justify-between"><span>Samedi</span><span>15h - 20h</span></li>
                    </ul>
                </div>
            </div>
        </section>
        <section id="youtube" class="mb-12">
            <h2 class="text-2xl font-bold mb-6 text-pink-400">Mes vidéos YouTube</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-gray-800 rounded-lg overflow-hidden shadow-lg">
                    <a href="https://youtu.be/video_id_1" target="_blank" rel="noopener">
                        <div class="relative">
                            <img src="https://i.imgur.com/placeholder.jpg" alt="Miniature YouTube" class="w-full h-48 object-cover">
                            <div class="absolute inset-0 flex items-center justify-center">
                                <i class="fab fa-youtube text-6xl text-red-500 opacity-80"></i>
                            </div>
                        </div>
                        <div class="p-4">
                            <h3 class="font-bold">Let's Play Minecraft</h3>
                            <p class="text-sm text-gray-400 mt-2">Cliquez pour regarder sur YouTube</p>
                        </div>
                    </a>
                </div>
                <div class="bg-gray-800 rounded-lg overflow-hidden shadow-lg">
                    <a href="https://youtu.be/video_id_2" target="_blank" rel="noopener">
                        <div class="relative">
                            <img src="https://i.imgur.com/placeholder.jpg" alt="Miniature YouTube" class="w-full h-48 object-cover">
                            <div class="absolute inset-0 flex items-center justify-center">
                                <i class="fab fa-youtube text-6xl text-red-500 opacity-80"></i>
                            </div>
                        </div>
                        <div class="p-4">
                            <h3 class="font-bold">Tournoi Fortnite</h3>
                            <p class="text-sm text-gray-400 mt-2">Cliquez pour regarder sur YouTube</p>
                        </div>
                    </a>
                </div>
            </div>
        </section>
    </main>
    <footer class="bg-gray-900 py-8 mt-12">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h2 class="text-xl font-bold text-pink-400">GamingPortal</h2>
                    <p class="text-gray-400">Votre portail gaming préféré</p>
                </div>
                <div class="flex space-x-4">
                    <a href="https://twitch.tv/votre_chaine" class="text-gray-400 hover:text-purple-400 transition" target="_blank" rel="noopener">
                        <i class="fab fa-twitch fa-lg"></i>
                    </a>
                    <a href="https://youtube.com/votre_chaine" class="text-gray-400 hover:text-red-400 transition" target="_blank" rel="noopener">
                        <i class="fab fa-youtube fa-lg"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-blue-400 transition">
                        <i class="fab fa-twitter fa-lg"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-indigo-400 transition">
                        <i class="fab fa-discord fa-lg"></i>
                    </a>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-6 pt-6 text-center text-gray-500 text-sm">
                <p>© 2023 GamingPortal. Tous droits réservés.</p>
            </div>
        </div>
    </footer>
    <script>
        const musicPlayer = document.getElementById('bgMusic');
        const toggleBtn = document.getElementById('musicToggle');
        let isPlaying = false;
        toggleBtn.addEventListener('click', () => {
            if (isPlaying) {
                musicPlayer.pause();
                toggleBtn.innerHTML = '<i class="fas fa-music"></i> Musique : ON';
            } else {
                musicPlayer.play();
                toggleBtn.innerHTML = '<i class="fas fa-pause"></i> Musique : OFF'; }
            isPlaying = !isPlaying;
        });
        const vtuberDialog = document.getElementById('vtuberDialog');
        const dialogText = document.getElementById('dialogText');
        const vtuberPhrases = [
            "Coucou ! Je suis ta mascotte kawaii 🎀",
            "Abonne-toi à la chaîne YouTube !",
            "Viens me voir en live sur Twitch !",
            "On joue ensemble ce soir ? UwU",
            "Tu es mon viewer préféré ❤️"
        ];
function showMessage(text) {
            dialogText.textContent = text;
            vtuberDialog.classList.remove('hidden');
            setTimeout(() => {
                vtuberDialog.classList.add('hidden');
            }, 3000);
        }
function showRandomMessage() {
            const phrase = vtuberPhrases[Math.floor(Math.random() * vtuberPhrases.length)];
            showMessage(phrase);
        }
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>