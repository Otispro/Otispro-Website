<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Otispro - Die Ultimative YouTube-Website</title>
    <style>
        /* Resetting some default styles for a clean slate */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Main body styling */
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #1d1d1d, #313131);
            color: #f2f2f2;
            padding: 0;
            margin: 0;
            overflow-x: hidden;
            animation: fadeIn 1s ease-in-out;
            transition: background 0.5s ease, color 0.5s ease;
        }

        body.light-mode {
            background: #f7f7f7;
            color: #333;
        }

        /* Smooth fade-in animation */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Logo */
        #logo {
            font-size: 48px;
            color: #ff6600;
            text-shadow: 0 0 20px rgba(255, 102, 0, 0.5);
            text-align: center;
            padding-top: 50px;
            font-weight: bold;
        }

        /* Navigation bar styling */
        .navbar {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            position: sticky;
            top: 0;
            width: 100%;
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.5);
        }

        .navbar .button {
            padding: 15px 25px;
            background: linear-gradient(45deg, #007bff, #00c6ff);
            border: none;
            border-radius: 30px;
            color: white;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            text-transform: uppercase;
            box-shadow: 0 5px 15px rgba(0, 174, 255, 0.5);
            transition: transform 0.3s ease, background 0.3s ease, box-shadow 0.3s ease;
        }

        .navbar .button:hover {
            background: linear-gradient(45deg, #00c6ff, #007bff);
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 174, 255, 0.8);
        }

        .navbar .button:focus {
            outline: none;
        }

        /* Content styling */
        .content {
            display: none;
            padding: 40px 20px;
            margin: 50px auto;
            max-width: 900px;
            background: rgba(18, 18, 18, 0.9);
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0, 174, 255, 0.7);
            animation: fadeIn 0.8s ease-in-out;
        }

        .content.active {
            display: block;
        }

        h1 {
            font-size: 36px;
            color: #ffcc00;
            text-shadow: 2px 2px 10px rgba(255, 102, 0, 0.7);
            margin-bottom: 20px;
        }

        p {
            font-size: 18px;
            line-height: 1.6;
            text-align: justify;
        }

        /* Dark Mode Button */
        .dark-mode-toggle, .light-mode-toggle {
            background: #333;
            color: #fff;
            padding: 12px 20px;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s ease;
        }

        .dark-mode-toggle:hover {
            background: #ff6600;
        }

        .light-mode-toggle:hover {
            background: #007bff;
        }

        /* Footer Styling */
        footer {
            text-align: center;
            padding: 20px;
            background: #1c1c1c;
            color: #f1f1f1;
            position: fixed;
            bottom: 0;
            width: 100%;
            box-shadow: 0 -10px 15px rgba(0, 0, 0, 0.5);
        }

        footer p {
            font-size: 14px;
        }

        /* Button adjustments for mobile */
        @media (max-width: 768px) {
            #logo {
                font-size: 36px;
            }

            .navbar {
                flex-direction: column;
                padding: 15px;
            }

            .navbar .button {
                width: 100%;
                margin-bottom: 10px;
            }

            h1 {
                font-size: 28px;
            }

            p {
                font-size: 16px;
            }
        }
    </style>
    <script>
        function showContent(section) {
            var contents = document.querySelectorAll('.content');
            contents.forEach(content => content.classList.remove('active'));
            document.getElementById(section).classList.add('active');
        }

        function toggleDarkMode() {
            document.body.classList.remove('light-mode');
            document.body.classList.add('dark-mode');
        }

        function toggleLightMode() {
            document.body.classList.remove('dark-mode');
            document.body.classList.add('light-mode');
        }
    </script>
</head>
<body>
    <div id="logo">OTISPRO</div>
    <div class="navbar">
        <button class="button" onclick="showContent('home')">Startseite</button>
        <button class="button" onclick="showContent('about')">Über mich</button>
        <button class="button" onclick="showContent('videos')">Meine Videos</button>
        <button class="button" onclick="showContent('events')">Events</button>
        <button class="button" onclick="showContent('giveaways')">Verlosungen</button>
        <button class="button" onclick="showContent('brawlstars')">Brawl Stars News</button>
        <button class="button" onclick="showContent('settings')">Einstellungen</button>
    </div>

    <!-- Home Section -->
    <div id="home" class="content active">
        <h1>Willkommen auf Otispro's Website!</h1>
        <p>Willkommen auf meiner Website! Hier findest du alles, was du über meinen YouTube-Kanal wissen musst. Klicke auf die verschiedenen Bereiche oben, um mehr über meine Videos, Events, und vieles mehr zu erfahren.</p>
    </div>

    <!-- About Section -->
    <div id="about" class="content">
        <h1>Über mich</h1>
        <p>Ich bin Otispro, ein leidenschaftlicher YouTuber, der sich auf Brawl Stars konzentriert. Auf meinem Kanal findest du spannende Videos, Updates und Tipps zu diesem fantastischen Spiel. Ich liebe es, meine Zuschauer zu unterhalten und zu informieren!</p>
    </div>

    <!-- Videos Section -->
    <div id="videos" class="content">
        <h1>Meine Videos</h1>
        <p>Ich lade regelmäßig neue Videos hoch, die tiefere Einblicke in die Welt von Brawl Stars geben. Egal, ob du an Brawler-Strategien, neuen Updates oder den besten Spielmethoden interessiert bist, auf meinem Kanal wirst du fündig!</p>
    </div>

    <!-- Events Section -->
    <div id="events" class="content">
        <h1>Events</h1>
        <p>Hier findest du alle Infos zu meinen kommenden Events. Sei es ein Live-Stream oder ein besonderes Turnier, verpass kein Highlight!</p>
    </div>

    <!-- Giveaways Section -->
    <div id="giveaways" class="content">
        <h1>Verlosungen</h1>
        <p>In diesem Bereich findest du alle Details zu meinen zukünftigen Verlosungen. Gewinne exklusive Preise, indem du an meinen Events teilnimmst!</p>
    </div>

    <!-- Brawl Stars News Section -->
    <div id="brawlstars" class="content">
        <h1>Brawl Stars News</h1>
        <p>Bleib immer auf dem Laufenden mit den neuesten Nachrichten und Updates zu Brawl Stars! Schau dir die neuesten Ankündigungen an und verpasse keine neuen Infos.</p>
    </div>

    <!-- Settings Section -->
    <div id="settings" class="content">
        <h1>Einstellungen</h1>
        <button class="dark-mode-toggle" onclick="toggleDarkMode()">Dark Mode umschalten</button>
        <button class="light-mode-toggle" onclick="toggleLightMode()">Light Mode umschalten</button>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Otispro | Alle Rechte vorbehalten.</p>
    </footer>
</body>
</html>
