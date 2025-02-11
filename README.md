<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - Alekesi</title>
    <!-- Importer les polices Google -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&family=Roboto+Slab:wght@700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Open Sans', sans-serif;
            background: #0a0a1a;
            color: white;
            text-align: center;
            overflow-y: auto;
            position: relative;
        }

        /* Etoiles scintillantes */
        .stars {
            width: 100%;
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            background-color: #000;
            z-index: 0;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background-color: #ffffff;
            border-radius: 50%;
            animation: twinkle 1.5s infinite alternate;
        }

        @keyframes twinkle {
            0% {
                opacity: 0.5;
            }
            100% {
                opacity: 1;
            }
        }

        .nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.7);
            padding: 10px 0;
            display: flex;
            justify-content: center;
            gap: 20px;
            z-index: 1000;
            font-family: 'Roboto', sans-serif;
        }

        .nav a {
            color: white;
            text-decoration: none;
            font-size: 1.2em;
            font-weight: 500;
            padding: 10px 15px;
            transition: color 0.3s ease;
        }

        .nav a:hover {
            color: #ff9800;
        }

        .container {
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 100px 20px 50px;
            z-index: 1;
        }

        h1 {
            font-size: 3em;
            background: linear-gradient(90deg, #ff9800, #ff5722);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 10px rgba(255, 152, 0, 0.5);
            text-transform: uppercase;
            white-space: nowrap;
            overflow: hidden;
            border-right: 3px solid #ff9800;
            animation: typing 2.5s steps(15) 1, blink 0.75s step-end infinite;
        }

        @keyframes typing {
            0% {
                width: 0;
            }
            100% {
                width: 100%;
            }
        }

        @keyframes blink {
            0% {
                border-color: transparent;
            }
            50% {
                border-color: #ff9800;
            }
            100% {
                border-color: transparent;
            }
        }

        .section {
            margin: 50px 0;
            font-family: 'Roboto Slab', serif;
            padding: 30px;
            width: 80%;
            max-width: 800px;
            margin: 30px auto;
        }

        h2 {
            font-size: 2em;
            font-weight: 700;
            color: #ff9800;
            margin-bottom: 20px;
        }

        /* Cadre fin orange pour la section "À propos" */
        #about {
            border: 2px solid #ff9800;
            padding: 30px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(255, 152, 0, 0.4);
        }

        /* Barres de progression */
        .progress-bar {
    width: 100%;  /* 100% de la largeur de son parent (skills) */
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 10px;
    overflow: hidden;
    margin: 10px 0;
    height: 20px;
}

        .progress {
    height: 100%;
    background: linear-gradient(90deg, #ff9800, #ff5722); 
    transition: width 1s ease-in-out;
}

.skills {
    width: 80%;  /* Limiter la largeur des compétences */
    max-width: 600px;  /* Limiter à 600px de largeur maximale */
    text-align: left;
    margin: 0 auto;  /* Centrer les compétences */
}


        .contact-btn {
            background-color: #ff9800;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.2em;
            transition: 0.3s;
            box-shadow: 0 4px 10px rgba(255, 152, 0, 0.5);
        }

        .contact-btn:hover {
            background-color: #ff5722;
            box-shadow: 0 6px 20px rgba(255, 152, 0, 0.7);
        }

        .project-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .project-item {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 15px;
            width: 250px;
            text-align: center;
            box-shadow: 0 0 10px rgba(255, 152, 0, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 0 20px rgba(255, 152, 0, 0.5);
        }

        .project-item img {
            width: 100%;
            border-radius: 10px;
        }

        /* Style des icônes des réseaux sociaux */
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 2em;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .social-icons a:hover {
            color: #ff5722;
        }

        .social-icons img {
            width: 40px;
        }
    </style>
</head>
<body>
    <div class="stars"></div>
    <div class="nav">
        <a href="#about">À propos</a>
        <a href="#skills">Compétences</a>
        <a href="#projects">Projets</a>
        <a href="#contact">Contact</a>
    </div>
    <div class="container">
        <h1>ALEKESI</h1>
        <p>Jeune passionné d'informatique hardware & software !</p>
        
        <div id="about" class="section">
            <h2>À propos</h2>
            <p>Je suis actuellement en train d'envisager des études en informatique. Ce qui me passionne particulièrement, c'est l'informatique sous toutes ses formes, que ce soit le hardware, le software, les réseaux, ou encore la cybersécurité. Mon objectif est d'explorer chaque facette de ce domaine en constante évolution.</p>
        </div>
        
        <div id="skills" class="section skills">
            <h2>Compétences</h2>
            <p>Réseau & Serveur</p>
            <div class="progress-bar">
                <div class="progress" style="width: 80%;"></div>
            </div>
            
            <p>OS (Linux, Windows)</p>
            <div class="progress-bar">
                <div class="progress" style="width: 85%;"></div>
            </div>
        
            <p>HTML & CSS</p>
            <div class="progress-bar">
                <div class="progress" style="width: 99%;"></div>
            </div>
        
            <p>JavaScript</p>
            <div class="progress-bar">
                <div class="progress" style="width: 90%;"></div>
            </div>
        
            <p>Java</p>
            <div class="progress-bar">
                <div class="progress" style="width: 85%;"></div>
            </div>
        
            <p>Python</p>
            <div class="progress-bar">
                <div class="progress" style="width: 80%;"></div>
            </div>
        
            <p>Rust</p>
            <div class="progress-bar">
                <div class="progress" style="width: 40%;"></div>
            </div>
        </div>
        
        
        <div id="projects" class="section projects">
            <h2>Mes Projets</h2>
            <div class="project-container">
                <div class="project-item">
                    <img src="./src/disocrd.png" alt="Biome Minecraft">
                    <p>Bot discord (js/phyton)</p>
                </div>
                <div class="project-item">
                    <img src="./src/minecraft.png" alt="Plugin Spigot">
                    <p>Plugin Spigot (java)</p>
                </div>
                <div class="project-item">
                    <img src="./src/portefolio.png" alt="Portfolio dynamique">
                    <p>Portfolio dynamique (html/css/js)</p>
                </div>
                <div class="project-item">
                    <img src="./src/github.png" alt="Github">
                    <p>Projets divers sur Github (java/rust/js)</p>
                </div>
            </div>
        </div>
        
        <div id="contact" class="section contact">
            <h2>Contact</h2>
            <p>Email: <a href="mailto:contact@alekesi.fr" style="color: #ff9800;">contact@alekesi.fr</a></p>
            <p>GitHub: <a href="https://github.com/alekesii" target="_blank" style="color: #ff9800;">github.com/alekesii</a></p>
            <div class="social-icons">
                <a href="https://www.instagram.com/alexis.jny" target="_blank">
                    <img src="./src/instagram.png" alt="Instagram">
                </a>
                <a href="https://discord.com/users/alekesi" target="_blank">
                    <img src="./src/disocrd.png" alt="Discord">
                </a>
            </div>
        </div>
    </div>

    <!-- Générer des étoiles scintillantes -->
    <script>
        const starsContainer = document.querySelector('.stars');
        for (let i = 0; i < 100; i++) {
            const star = document.createElement('div');
            star.classList.add('star');
            star.style.top = `${Math.random() * 100}vh`;
            star.style.left = `${Math.random() * 100}vw`;
            star.style.animationDuration = `${Math.random() * 2 + 1}s`;
            starsContainer.appendChild(star);
        }
    </script>
</body>
</html>
