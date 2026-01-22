<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Best Madam Tribute by Somaksh</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #ffe4e1, #ffb6c1); /* Soft pink gradient */
            color: #333;
            line-height: 1.6;
            overflow-x: hidden; /* Prevent horizontal scroll */
            position: relative;
        }
        /* Floating bubbles background animation */
        .bubble {
            position: absolute;
            bottom: -100px;
            width: 20px;
            height: 20px;
            background-color: rgba(255, 105, 180, 0.3);
            border-radius: 50%;
            animation: floatUp 10s infinite linear;
        }
        .bubble:nth-child(odd) { left: 10%; animation-delay: 0s; }
        .bubble:nth-child(even) { left: 20%; animation-delay: 2s; }
        .bubble:nth-child(3n) { left: 30%; animation-delay: 4s; }
        .bubble:nth-child(4n) { left: 40%; animation-delay: 6s; }
        .bubble:nth-child(5n) { left: 50%; animation-delay: 8s; }
        @keyframes floatUp {
            0% { transform: translateY(0) scale(1); opacity: 0.5; }
            100% { transform: translateY(-100vh) scale(1.5); opacity: 0; }
        }
        header {
            background-color: #ff69b4;
            color: white;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            animation: headerGlow 2s infinite alternate;
        }
        @keyframes headerGlow {
            0% { box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
            100% { box-shadow: 0 2px 20px rgba(255, 105, 180, 0.5); }
        }
        nav {
            background-color: #fff;
            padding: 10px;
            text-align: center;
            border-bottom: 1px solid #ddd;
        }
        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: #ff69b4;
            font-weight: bold;
            transition: color 0.3s;
        }
        nav a:hover { color: #ff1493; }
        main {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1, h2 {
            color: #ff69b4;
        }
        form {
            margin-bottom: 20px;
        }
        input[type="text"] {
            padding: 10px;
            width: 70%;
            border: 1px solid #ccc;
            border-radius: 5px;
            transition: border-color 0.3s;
        }
        input[type="text"]:focus { border-color: #ff69b4; }
        button {
            padding: 10px 20px;
            background-color: #ff69b4;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s, transform 0.2s;
        }
        button:hover {
            background-color: #ff1493;
            transform: scale(1.05);
        }
        .message {
            display: none;
            font-size: 36px;
            color: #ff69b4;
            font-weight: bold;
            text-align: center;
            position: relative;
            animation: fadeIn 1s ease-in-out, shake 0.5s ease-in-out 1s;
            margin-top: 20px;
            z-index: 20; /* Text always on top */
            border: 2px solid #ff69b4;
            border-radius: 10px;
            padding: 10px;
            background-color: rgba(255, 255, 255, 0.9);
            text-shadow: 0 0 10px rgba(255, 105, 180, 0.5); /* Glow effect */
        }
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }
        .typewriter {
            border-right: 2px solid #ff69b4; /* Blinking cursor */
            animation: blink 1s infinite;
        }
        @keyframes blink {
            0%, 50% { border-color: #ff69b4; }
            51%, 100% { border-color: transparent; }
        }
        .sparkle {
            position: absolute;
            background-color: gold;
            border-radius: 50%;
            animation: sparkle 1.5s infinite ease-in-out;
            z-index: 5;
        }
        .sparkle:nth-child(1) { width: 10px; height: 10px; top: -30px; left: 10px; }
        .sparkle:nth-child(2) { width: 15px; height: 15px; top: 5px; right: 20px; }
        .sparkle:nth-child(3) { width: 12px; height: 12px; bottom: -20px; left: 30px; }
        .sparkle:nth-child(4) { width: 18px; height: 18px; bottom: 10px; right: 30px; }
        .sparkle:nth-child(5) { width: 14px; height: 14px; top: -10px; left: 50px; }
        .sparkle:nth-child(6) { width: 16px; height: 16px; top: 20px; right: 50px; }
        .sparkle:nth-child(7) { width: 11px; height: 11px; bottom: -5px; left: 70px; }
        .sparkle:nth-child(8) { width: 13px; height: 13px; bottom: 25px; right: 70px; }
        @keyframes sparkle {
            0%, 100% { opacity: 0; transform: scale(0) rotate(0deg); }
            50% { opacity: 1; transform: scale(1.2) rotate(360deg); }
        }
        .ribbon {
            position: absolute;
            height: 25px;
            background-color: #ff69b4;
            border-radius: 5px;
            opacity: 0.7; /* Semi-transparent to not hide text */
            animation: flowRibbon 8s infinite linear, colorChange 4s infinite;
            z-index: 1; /* Below text */
        }
        .ribbon:nth-child(1) { width: 100px; top: -100px; left: -100px; animation-delay: 0s; }
        .ribbon:nth-child(2) { width: 120px; top: 100px; right: -120px; animation-delay: 2s; }
        .ribbon:nth-child(3) { width: 80px; bottom: -80px; left: -80px; animation-delay: 4s; }
        .ribbon:nth-child(4) { width: 110px; bottom: 80px; right: -110px; animation-delay: 6s; }
        .ribbon:nth-child(5) { width: 90px; top: -50px; left: 50%; animation-delay: 1s; }
        .ribbon:nth-child(6) { width: 130px; bottom: -50px; right: 50%; animation-delay: 3s; }
        @keyframes flowRibbon {
            0% { transform: translateX(0) translateY(0) rotate(0deg) scale(1); }
            25% { transform: translateX(200px) translateY(-50px) rotate(90deg) scale(1.1); }
            50% { transform: translateX(400px) translateY(0) rotate(180deg) scale(1); }
            75% { transform: translateX(200px) translateY(50px) rotate(270deg) scale(1.1); }
            100% { transform: translateX(0) translateY(0) rotate(360deg) scale(1); }
        }
        @keyframes colorChange {
            0% { background-color: #ff69b4; }
            33% { background-color: #ff1493; }
            66% { background-color: #ffb6c1; }
            100% { background-color: #ff69b4; }
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #ff69b4;
            color: white;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <!-- Floating bubbles for background animation -->
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <header>
        <h1>Welcome to the Best Madam Tribute Site</h1>
        <p>A fun, interactive page to celebrate awesomeness!</p>
    </header>
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>
    <main>
        <section id="home">
            <h2>Enter Your Name to Reveal the Magic</h2>
            <p>This is a realistic website example. Fill in your name below and click "Reveal" to see a special message with sparkles and ribbons!</p>
            <form id="tributeForm">
                <input type="text" id="userName" placeholder="Enter your name" required>
                <button type="submit">Reveal the Message</button>
            </form>
            <div class="message" id="message">
                <span id="personalizedMessage" class="typewriter"></span>
                <!-- More sparkles -->
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <div class="sparkle"></div>
                <!-- Flowing ribbons -->
                <div class="ribbon"></div>
                <div class="ribbon"></div>
                <div class="ribbon"></div>
                <div class="ribbon"></div>
                <div class="ribbon"></div>
                <div class="ribbon"></div>
            </div>
        </section>
        <section id="about">
            <h2>About This Site</h2>
            <p>This is a demo website built with HTML, CSS, and JavaScript. It's designed to be interactive and fun, showcasing animations like sparkles and ribbons. In a real scenario, you could add more content, images, or even backend functionality.</p>
        </section>
        <section id="contact">
            <h2>Contact</h2>
            <p>Feel free to reach out for more web development tips!</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Best Madam Tribute. Made by Somaksh.</p>
    </footer>

    <script>
        document.getElementById('tributeForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent form from reloading the page
            const userName = document.getElementById('userName').value.trim();
            const messageSpan = document.getElementById('personalizedMessage');
            const messageDiv = document.getElementById('message');
            
            let fullMessage = userName ? `${userName}, you are the best Madam!` : 'You are the best Madam!';
            messageSpan.textContent = ''; // Clear previous text
            messageDiv.style.display = 'block';
            
            // Typewriter effect: Type out the message letter by letter
            let i = 0;
            const typeWriter = () => {
                if (i < fullMessage.length) {
                    messageSpan.textContent += fullMessage.charAt(i);
                    i++;
                    setTimeout(typeWriter, 80); // Slightly faster typing
                } else {
                    // Remove cursor after typing is done
                    messageSpan.classList.remove('typewriter');
                }
            };
            typeWriter();
        });
    </script>
</body>
</html>
