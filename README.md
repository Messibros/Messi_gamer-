

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Messi Gamer - Pura Nostalgia</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-image: url('background-image.jpg');
            background-size: cover;
            background-position: center;
            color: #fff;
            font-family: 'Press Start 2P', cursive;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding-bottom: 20px;
        }

        header {
            background-color: rgba(0, 0, 0, 0.7);
            padding: 20px;
            position: relative;
        }

        header::before {
            content: '';
            background-image: url('header-background.jpg');
            background-size: cover;
            background-position: center;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.5;
            z-index: 0;
        }

        header h1,
        header h2 {
            position: relative;
            z-index: 1;
        }

        header h1 {
            color: #00BFFF;
            font-size: 5em;
        }

        header h2 {
            color: #FFD700;
            font-size: 2.5em;
            margin-top: 10px;
        }

        .content {
            padding: 20px;
            flex-grow: 1;
        }

        .carousel-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin: 0 auto;
            overflow: hidden;
            margin-top: 20px;
        }

        .carousel {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .carousel img {
            width: 100%;
            flex-shrink: 0;
            object-fit: cover;
        }

        .carousel-button {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(0, 0, 0, 0.5);
            border: none;
            color: white;
            padding: 10px;
            cursor: pointer;
            font-size: 18px;
            z-index: 10;
        }

        .prev-button {
            left: 10px;
        }

        .next-button {
            right: 10px;
        }

        .games-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            list-style-type: none;
            padding: 0;
            margin-top: 20px;
        }

        .games-list li {
            background-color: rgba(0, 0, 0, 0.5);
            border: 2px solid #FFD700;
            border-radius: 10px;
            display: inline-block;
            margin: 10px;
            padding: 15px;
            width: 200px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .games-list li:hover {
            transform: scale(1.05);
        }

        .games-list img {
            height: 50px;
            margin-bottom: 10px;
        }

        video {
            border: 3px solid #00BFFF;
            border-radius: 10px;
            margin-top: 30px;
            max-width: 100%;
            width: 640px;
        }

        .buttons-container {
            margin-top: 40px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        footer {
            background-color: rgba(0, 0, 0, 0.8);
            padding: 20px;
            width: 100%;
            text-align: center;
            position: relative;
            bottom: 0;
            left: 0;
            margin-top: 20px;
        }

        footer p {
            margin-top: 10px;
        }

        footer button {
            background-color: #00BFFF;
            border: none;
            border-radius: 10px;
            color: #fff;
            cursor: pointer;
            font-family: 'Press Start 2P', cursive;
            font-size: 1em;
            margin: 5px;
            padding: 10px;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        footer button:hover {
            background-color: #FFD700;
            transform: translateY(-3px);
        }

        @media screen and (max-width: 768px) {
            header h1 {
                font-size: 3em;
            }

            header h2 {
                font-size: 1.8em;
            }

            .games-list li {
                width: 150px;
            }

            video {
                width: 100%;
            }
        }

        @media screen and (max-width: 480px) {
            header h1 {
                font-size: 2em;
            }

            header h2 {
                font-size: 1.2em;
            }

            .games-list li {
                width: 120px;
                padding: 10px;
            }

            footer {
                font-size: 0.8em;
            }

            footer button {
                font-size: 0.8em;
                padding: 8px;
            }

            .buttons-container {
                flex-direction: column;
                gap: 10px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Messi Gamer</h1>
        <h2>Pura Nostalgia</h2>
    </header>

    <div class="content">
        <h3>Melhores Games Retrô</h3>

        <div class="carousel-container">
            <button class="carousel-button prev-button" onclick="changeSlide(-1)">&#10094;</button>
            <div class="carousel" id="carousel">
                <img src="game1.jpg" alt="Game 1">
                <img src="game2.jpg" alt="Game 2">
                <img src="game3.jpg" alt="Game 3">
                <img src="game4.jpg" alt="Game 4">
                <img src="game5.jpg" alt="Game 5">
                <img src="game6.jpg" alt="Game 6">
                <img src="game7.jpg" alt="Game 7">
                <img src="game8.jpg" alt="Game 8">
                <img src="game9.jpg" alt="Game 9">
                <img src="game10.jpg" alt="Game 10">
                <img src="game11.jpg" alt="Game 11">
                <img src="game12.jpg" alt="Game 12">
                <img src="game13.jpg" alt="Game 13">
                <img src="game14.jpg" alt="Game 14">
                <img src="game15.jpg" alt="Game 15">
            </div>
            <button class="carousel-button next-button" onclick="changeSlide(1)">&#10095;</button>
        </div>

        <ul class="games-list">
            <li>
                <a href="mario.html"><img src="mario-image.png" alt="Mario"></a>
                Super Mario World
            </li>
            <li>
                <a href="sonic.html"><img src="sonic-image.png" alt="Sonic"></a>
                Sonic the Hedgehog
            </li>
            <li>
                <a href="pacman.html"><img src="pacman-image.png" alt="Pac-Man"></a>
                Pac-Man
            </li>
            <li>
                <a href="donkeykong.html"><img src="donkeykong-image.png" alt="Donkey Kong"></a>
                Donkey Kong Country
            </li>
        </ul>

        <video controls>
            <source src="gameplay.mp4" type="video/mp4">
            Seu navegador não suporta o elemento de vídeo.
        </video>
    </div>

    <footer>
        
            <button onclick="window.location.href='https://www.youtube.com/@MESSI_GAMER';">🔗 YouTube</button>
        </div>
        <p>&copy; 2024 Messi Gamer. Todos os direitos reservados.</p>
    </footer>

    <script>
        let currentSlide = 0;
        const carousel = document.getElementById('carousel');
        const totalSlides = carousel.children.length;
        let startX = 0;
        let audioPlayer;

        function showSlide(index) {
            if (index < 0) {
                currentSlide = totalSlides - 1;
            } else if (index >= totalSlides) {
                currentSlide = 0;
            } else {
                currentSlide = index;
            }
            carousel.style.transform = `translateX(-${currentSlide * 100}%)`;
        }

        function changeSlide(direction) {
            showSlide(currentSlide + direction);
        }

        function playMusic() {
            if (!audioPlayer) {
                audioPlayer = new Audio('background-music.mp3');
                audioPlayer.loop = true;
            }
            
            if (audioPlayer.paused) {
                audioPlayer.play();
            } else {
                audioPlayer.pause();
            }
        }

        carousel.addEventListener('touchstart', (e) => {
            startX = e.touches[0].clientX;
        });

        carousel.addEventListener('touchend', (e) => {
            const endX = e.changedTouches[0].clientX;
            const diffX = startX - endX;

            if (Math.abs(diffX) > 50) {
                if (diffX > 0) {
                    changeSlide(1);
                } else {
                    changeSlide(-1);
                }
            }
        });

        setInterval(() => changeSlide(1), 5000);
    </script>
</body>
</html>
