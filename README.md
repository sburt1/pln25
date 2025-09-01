<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paris Adventure 2025</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #1e3a8a 0%, #ffffff 50%, #dc2626 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            border: 3px solid #1e3a8a;
        }

        .header {
            background: linear-gradient(135deg, #dc2626 0%, #1e3a8a 100%);
            color: white;
            padding: 60px 30px;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 4px solid #ffffff;
        }

        .header::before {
            content: '🗼';
            position: absolute;
            top: -20px;
            right: -20px;
            font-size: 120px;
            opacity: 0.2;
            transform: rotate(15deg);
        }

        .header::after {
            content: '🇫🇷';
            position: absolute;
            top: -10px;
            left: -20px;
            font-size: 100px;
            opacity: 0.3;
            transform: rotate(-15deg);
        }

        .header h1 {
            font-size: 3.5em;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .header .subtitle {
            font-size: 1.6em;
            opacity: 0.9;
            font-weight: 300;
            margin-bottom: 10px;
        }

        .header .dates {
            font-size: 1.2em;
            opacity: 0.8;
            font-style: italic;
        }

        .content {
            padding: 50px 30px;
        }

        .intro-section {
            background: linear-gradient(135deg, #1e3a8a, #3b82f6);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 40px;
            text-align: center;
            border: 2px solid #dc2626;
            box-shadow: 0 8px 20px rgba(30, 58, 138, 0.3);
        }

        .intro-section h2 {
            font-size: 2em;
            margin-bottom: 15px;
        }

        .intro-section p {
            font-size: 1.2em;
            line-height: 1.6;
            opacity: 0.95;
        }

        .days-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .day-card {
            background: linear-gradient(135deg, #f8faff, #eff6ff);
            border: 2px solid #dc2626;
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(220, 38, 38, 0.1);
            position: relative;
            overflow: hidden;
        }

        .day-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(30, 58, 138, 0.2);
            border-color: #1e3a8a;
        }

        .day-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #dc2626, #1e3a8a);
        }

        .day-number {
            background: linear-gradient(135deg, #dc2626, #ef4444);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 1em;
            font-weight: bold;
            margin-bottom: 15px;
            display: inline-block;
            border: 2px solid #1e3a8a;
        }

        .day-title {
            color: #1e3a8a;
            font-size: 1.3em;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .day-description {
            color: #374151;
            font-size: 0.95em;
            line-height: 1.5;
            margin-bottom: 20px;
        }

        .day-button {
            display: inline-block;
            background: linear-gradient(135deg, #1e3a8a, #3b82f6);
            color: white;
            text-decoration: none;
            padding: 12px 25px;
            border-radius: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
            border: 2px solid #dc2626;
            font-size: 0.9em;
        }

        .day-button:hover {
            background: linear-gradient(135deg, #dc2626, #ef4444);
            border-color: #1e3a8a;
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .footer-section {
            background: linear-gradient(135deg, #dc2626, #1e3a8a);
            color: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            border: 3px solid #ffffff;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }

        .footer-section h3 {
            font-size: 1.5em;
            margin-bottom: 15px;
        }

        .footer-section p {
            font-size: 1.1em;
            line-height: 1.6;
            opacity: 0.95;
        }

        .emoji-large {
            font-size: 2em;
            margin-right: 10px;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5em;
            }
            
            .header .subtitle {
                font-size: 1.3em;
            }
            
            .content {
                padding: 30px 20px;
            }
            
            .days-grid {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            
            .day-card {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Paris Adventure</h1>
            <div class="subtitle">September 2025</div>
            <div class="dates">9 Days in the City of Light</div>
        </div>
        
        <div class="content">
            <div class="intro-section">
                <h2>🇫🇷 Bienvenue à Paris!</h2>
                <p>Your complete 9-day journey through the most beautiful city in the world. From historic neighborhoods to iconic landmarks, culinary adventures to cultural treasures - every day is perfectly planned for an unforgettable Parisian experience.</p>
            </div>

            <div class="days-grid">
                <div class="day-card">
                    <div class="day-number">Day 1</div>
                    <div class="day-title">Wednesday, September 3</div>
                    <div class="day-description">Arrival & First Impressions: Parc Monceau, Le Petit Vendome, Ritz Comptoir, Petit Palais & Arc de Triomphe</div>
                    <a href="/d1/index.html" class="day-button">View Day 1 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 2</div>
                    <div class="day-title">Thursday, September 4</div>
                    <div class="day-description">Le Marais Discovery: Place des Vosges, Victor Hugo House, boutique shopping, and historic covered passages</div>
                    <a href="/d2/index.html" class="day-button">View Day 2 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 3</div>
                    <div class="day-title">Friday, September 5</div>
                    <div class="day-description">Left Bank Adventures: Latin Quarter exploration, bookshops, and intellectual Paris</div>
                    <a href="/d3/index.html" class="day-button">View Day 3 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 4</div>
                    <div class="day-title">Saturday, September 6</div>
                    <div class="day-description">Iconic Landmarks: Eiffel Tower, Seine River cruise, and Parisian monuments</div>
                    <a href="/d4/index.html" class="day-button">View Day 4 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 5</div>
                    <div class="day-title">Sunday, September 7</div>
                    <div class="day-description">Art & Culture: Louvre Museum, Tuileries Gardens, and world-class masterpieces</div>
                    <a href="/d5/index.html" class="day-button">View Day 5 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 6</div>
                    <div class="day-title">Monday, September 8</div>
                    <div class="day-description">Montmartre Magic: Sacré-Cœur, artist squares, and bohemian neighborhoods</div>
                    <a href="/d6/index.html" class="day-button">View Day 6 →</a>
                </div>

                <div class="day-card">
                    <div class="day-title">Tuesday, September 9</div>
                    <div class="day-number">Day 7</div>
                    <div class="day-description">Royal Splendor: Palace of Versailles day trip and magnificent gardens</div>
                    <a href="/d7/index.html" class="day-button">View Day 7 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 8</div>
                    <div class="day-title">Wednesday, September 10</div>
                    <div class="day-description">Final Discoveries: Last-minute shopping, favorite café revisits, and hidden gems</div>
                    <a href="/d8/index.html" class="day-button">View Day 8 →</a>
                </div>

                <div class="day-card">
                    <div class="day-number">Day 9</div>
                    <div class="day-title">Thursday, September 11</div>
                    <div class="day-description">Au Revoir Paris: Departure day with final morning stroll and memories</div>
                    <a href="/d9/index.html" class="day-button">View Day 9 →</a>
                </div>
            </div>

            <div class="footer-section">
                <h3><span class="emoji-large">✨</span>Bon Voyage!</h3>
                <p>Each day is carefully crafted to give you the perfect balance of must-see attractions, local experiences, and spontaneous discoveries. Your Parisian adventure awaits!</p>
            </div>
        </div>
    </div>
</body>
</html>
