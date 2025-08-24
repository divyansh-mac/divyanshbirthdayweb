# divyanshbirthdayweb
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Cutuu</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@300;400;600&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --navy-blue: #0a192f;
            --light-navy: #172a45;
            --pink: #ff6b8b;
            --light-pink: #ffb6c1;
            --accent-pink: #ff4081;
            --gold: #ffd700;
            --text-light: #f8f8f8;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, var(--navy-blue), var(--light-navy));
            color: var(--text-light);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 10;
        }
        
        /* Header Styles */
        header {
            text-align: center;
            padding: 40px 0;
            position: relative;
        }
        
        .title-container {
            perspective: 1000px;
            margin: 30px 0 50px;
        }
        
        .happy-birthday {
            font-size: 4.5rem;
            font-family: 'Dancing Script', cursive;
            color: var(--pink);
            text-shadow: 0 0 15px rgba(255, 107, 139, 0.6);
            animation: glow 2s infinite alternate, float 3s ease-in-out infinite;
            margin-bottom: 10px;
            position: relative;
            display: inline-block;
            transform-style: preserve-3d;
        }
        
        .name {
            font-size: 3.5rem;
            color: var(--light-pink);
            font-weight: 600;
            letter-spacing: 2px;
            animation: fadeIn 1.5s ease-out;
            margin: 20px 0;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
        }
        
        .from {
            font-size: 1.2rem;
            color: var(--light-pink);
            font-style: italic;
            margin-top: 10px;
        }
        
        /* Heart Trees Section */
        .heart-trees-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 40px 0;
            position: relative;
            height: 350px;
        }
        
        .tree {
            position: relative;
            width: 200px;
            height: 300px;
            margin: 0 20px;
        }
        
        .trunk {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 25px;
            height: 110px;
            background: #5d4037;
            border-radius: 10px;
            z-index: 1;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
        }
        
        .tree-top {
            position: absolute;
            bottom: 100px;
            left: 50%;
            transform: translateX(-50%);
            width: 150px;
            height: 180px;
            background: linear-gradient(135deg, #2e7d32, #4caf50);
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            border-radius: 10px 10px 0 0;
            z-index: 2;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
        }
        
        .heart {
            position: absolute;
            width: 30px;
            height: 30px;
            background: var(--pink);
            transform: rotate(-45deg);
            border-radius: 0 0 5px 0;
            animation: pulse 1.5s infinite;
            z-index: 3;
            box-shadow: 0 0 10px rgba(255, 107, 139, 0.5);
        }
        
        .heart:before, .heart:after {
            content: "";
            position: absolute;
            width: 30px;
            height: 30px;
            background: var(--pink);
            border-radius: 50%;
        }
        
        .heart:before {
            top: -15px;
            left: 0;
        }
        
        .heart:after {
            top: 0;
            left: 15px;
        }
        
        /* Cake Section */
        .cake-container {
            text-align: center;
            margin: 50px 0;
            position: relative;
            z-index: 10;
        }
        
        .cake {
            position: relative;
            width: 250px;
            height: 180px;
            margin: 0 auto;
            cursor: pointer;
            transition: transform 0.3s ease;
        }
        
        .cake:hover {
            transform: scale(1.05);
        }
        
        .cake-bottom {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 220px;
            height: 90px;
            background: linear-gradient(to right, #f8c4d0, #f5a8b8, #f8c4d0);
            border-radius: 100px 100px 20px 20px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        
        .cake-top {
            position: absolute;
            bottom: 80px;
            left: 50%;
            transform: translateX(-50%);
            width: 180px;
            height: 70px;
            background: linear-gradient(to right, #ffd1dc, #ffb6c1, #ffd1dc);
            border-radius: 90px 90px 20px 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15);
        }
        
        .decoration {
            position: absolute;
            bottom: 140px;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 10px;
            background: var(--pink);
            border-radius: 10px;
        }
        
        .candles {
            position: absolute;
            bottom: 160px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 25px;
        }
        
        .candle {
            width: 12px;
            height: 45px;
            background: linear-gradient(to bottom, #ffb6c1, #ffffff, #ffb6c1);
            border-radius: 6px;
            position: relative;
            box-shadow: 0 0 10px rgba(255, 182, 193, 0.5);
        }
        
        .candle:nth-child(2) {
            height: 50px;
        }
        
        .candle:nth-child(3) {
            height: 40px;
        }
        
        .flame {
            position: absolute;
            top: -18px;
            left: 50%;
            transform: translateX(-50%);
            width: 14px;
            height: 24px;
            background: var(--gold);
            border-radius: 50% 50% 20% 20%;
            opacity: 0;
            box-shadow: 0 0 15px #ff9900, 0 0 25px #ff5500;
            transition: opacity 0.5s ease;
        }
        
        .lit .flame {
            opacity: 1;
            animation: flicker 0.8s infinite alternate;
        }
        
        .cake-controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        
        .cake-button {
            padding: 12px 30px;
            background: var(--pink);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 107, 139, 0.3);
        }
        
        .cake-button:hover {
            background: var(--accent-pink);
            transform: translateY(-3px);
            box-shadow: 0 7px 20px rgba(255, 107, 139, 0.4);
        }
        
        /* Love Note */
        .love-note {
            background: rgba(23, 42, 69, 0.85);
            max-width: 800px;
            margin: 60px auto;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            position: relative;
            z-index: 10;
            border: 1px solid rgba(255, 182, 193, 0.2);
            overflow: hidden;
        }
        
        .love-note:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--pink), var(--accent-pink));
        }
        
        .note-header {
            text-align: center;
            margin-bottom: 30px;
            color: var(--pink);
        }
        
        .note-content {
            font-size: 1.1rem;
            line-height: 1.8;
            text-align: justify;
            max-height: 300px;
            overflow-y: auto;
            padding: 10px 20px;
            position: relative;
        }
        
        .note-content::-webkit-scrollbar {
            width: 5px;
        }
        
        .note-content::-webkit-scrollbar-thumb {
            background: var(--pink);
            border-radius: 10px;
        }
        
        .signature {
            text-align: right;
            margin-top: 30px;
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: var(--accent-pink);
        }
        
        /* Audio Controls */
        .audio-controls {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 100;
            background: rgba(23, 42, 69, 0.9);
            border-radius: 50px;
            padding: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .audio-controls button {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--pink);
            color: white;
            border: none;
            cursor: pointer;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .audio-controls button:hover {
            background: var(--accent-pink);
            transform: scale(1.1);
        }
        
        .audio-title {
            margin-right: 10px;
            font-size: 0.9rem;
            color: var(--light-pink);
        }
        
        /* Floating Elements */
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .heart-shape {
            position: absolute;
            width: 20px;
            height: 20px;
            background: var(--pink);
            transform: rotate(-45deg);
            opacity: 0.6;
        }
        
        .heart-shape:before, .heart-shape:after {
            content: "";
            position: absolute;
            width: 20px;
            height: 20px;
            background: var(--pink);
            border-radius: 50%;
        }
        
        .heart-shape:before {
            top: -10px;
            left: 0;
        }
        
        .heart-shape:after {
            top: 0;
            left: 10px;
        }
        
        .star {
            position: absolute;
            width: 0;
            height: 0;
            border-right: 10px solid transparent;
            border-bottom: 7px solid var(--gold);
            border-left: 10px solid transparent;
            transform: rotate(35deg);
            opacity: 0.8;
        }
        
        .star:before {
            content: "";
            position: absolute;
            height: 0;
            width: 0;
            top: -4.5px;
            left: -6.5px;
            border-bottom: 8px solid var(--gold);
            border-left: 3px solid transparent;
            border-right: 3px solid transparent;
            transform: rotate(-35deg);
        }
        
        .star:after {
            content: "";
            position: absolute;
            top: 0.75px;
            left: -10.5px;
            width: 0;
            height: 0;
            border-right: 10px solid transparent;
            border-bottom: 7px solid var(--gold);
            border-left: 10px solid transparent;
            transform: rotate(-70deg);
        }
        
        .sparkle {
            position: absolute;
            width: 8px;
            height: 8px;
            background: white;
            border-radius: 50%;
            box-shadow: 0 0 10px white, 0 0 20px white;
            opacity: 0;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .happy-birthday {
                font-size: 3.5rem;
            }
            
            .name {
                font-size: 2.5rem;
            }
            
            .heart-trees-container {
                height: 280px;
                flex-direction: column;
                align-items: center;
            }
            
            .tree {
                margin: 10px 0;
                transform: scale(0.8);
            }
            
            .love-note {
                padding: 25px;
                margin: 40px auto;
            }
            
            .note-content {
                font-size: 1rem;
            }
        }
        
        @media (max-width: 480px) {
            .happy-birthday {
                font-size: 2.8rem;
            }
            
            .name {
                font-size: 2rem;
            }
            
            .cake {
                transform: scale(0.8);
            }
            
            .heart-trees-container {
                height: 230px;
            }
            
            .love-note {
                padding: 20px;
            }
            
            .cake-controls {
                flex-direction: column;
                align-items: center;
            }
        }
        
        /* Animations */
        @keyframes glow {
            0% {
                text-shadow: 0 0 10px rgba(255, 107, 139, 0.6);
            }
            100% {
                text-shadow: 0 0 20px rgba(255, 107, 139, 0.8), 0 0 30px rgba(255, 107, 139, 0.6);
            }
        }
        
        @keyframes float {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
            100% {
                transform: translateY(0);
            }
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0% {
                transform: rotate(-45deg) scale(1);
            }
            50% {
                transform: rotate(-45deg) scale(1.1);
            }
            100% {
                transform: rotate(-45deg) scale(1);
            }
        }
        
        @keyframes flicker {
            0% {
                opacity: 0.8;
                transform: translateX(-50%) scale(1);
            }
            25% {
                opacity: 1;
                transform: translateX(-50%) scale(1.1);
            }
            50% {
                opacity: 0.7;
                transform: translateX(-50%) scale(0.9);
            }
            75% {
                opacity: 1;
                transform: translateX(-50%) scale(1.05);
            }
            100% {
                opacity: 0.8;
                transform: translateX(-50%) scale(1);
            }
        }
        
        @keyframes floatUp {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.6;
            }
            90% {
                opacity: 0.6;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        @keyframes sparkle {
            0% {
                opacity: 0;
                transform: scale(0);
            }
            50% {
                opacity: 1;
                transform: scale(1);
            }
            100% {
                opacity: 0;
                transform: scale(1.5);
            }
        }
        
        @keyframes twinkle {
            0%, 100% {
                opacity: 0.2;
                transform: scale(0.8);
            }
            50% {
                opacity: 1;
                transform: scale(1.2);
            }
        }
        
        @keyframes cutAnimation {
            0% {
                transform: translateX(-50%) scale(1);
            }
            50% {
                transform: translateX(-50%) scale(1.05) rotate(-5deg);
            }
            100% {
                transform: translateX(-50%) scale(1);
            }
        }
        
        .cut {
            animation: cutAnimation 0.5s ease-in-out;
        }
    </style>
</head>
<body>
    <!-- Floating Elements -->
    <div class="floating-elements" id="floatingElements"></div>
    
    <div class="container">
        <!-- Header with Animated Title -->
        <header>
            <div class="title-container">
                <h1 class="happy-birthday">Happy Birthday</h1>
                <h2 class="name">My Cutuu</h2>
                <p class="from">From your Pretty Little Baby with love</p>
            </div>
        </header>
        
        <!-- Heart Trees -->
        <section class="heart-trees-container">
            <div class="tree" id="tree1">
                <div class="trunk"></div>
                <div class="tree-top"></div>
                <!-- Hearts will be generated by JavaScript -->
            </div>
            <div class="tree" id="tree2">
                <div class="trunk"></div>
                <div class="tree-top"></div>
                <!-- Hearts will be generated by JavaScript -->
            </div>
            <div class="tree" id="tree3">
                <div class="trunk"></div>
                <div class="tree-top"></div>
                <!-- Hearts will be generated by JavaScript -->
            </div>
        </section>
        
        <!-- Birthday Cake -->
        <section class="cake-container">
            <div class="cake" id="birthdayCake">
                <div class="cake-bottom"></div>
                <div class="cake-top"></div>
                <div class="decoration"></div>
                <div class="candles">
                    <div class="candle">
                        <div class="flame"></div>
                    </div>
                    <div class="candle">
                        <div class="flame"></div>
                    </div>
                    <div class="candle">
                        <div class="flame"></div>
                    </div>
                </div>
            </div>
            <div class="cake-controls">
                <button class="cake-button" id="lightButton">Light the Candles</button>
                <button class="cake-button" id="cutButton">Cut the Cake</button>
                <button class="cake-button" id="blowButton">Blow Out Candles</button>
            </div>
        </section>
        
        <!-- Romantic Note -->
        <section class="love-note">
            <div class="note-header">
                <h2><i class="fas fa-heart"></i> My Dearest Cutuu <i class="fas fa-heart"></i></h2>
            </div>
            <div class="note-content">
                <p>My beautiful Cutuu, on this special day, I want you to know how incredibly precious you are to me. Your smile lights up my world, your laughter is my favorite melody, and your presence makes every moment magical.</p>

                <p>Even though our journey has taken different paths, the memories we've shared will always hold a special place in my heart. You've taught me so much about love, kindness, and what truly matters in life.</p>

                <p>Today, I celebrate you - the amazing person you are and the wonderful person you're becoming. Your strength inspires me, your compassion moves me, and your spirit dazzles everyone around you.</p>

                <p>I hope this birthday brings you as much joy as you've brought into my life. May your day be filled with laughter, love, and beautiful moments that become cherished memories.</p>

                <p>No matter where life takes us, please always remember that you are loved, you are valued, and you deserve all the happiness in the world.</p>

                <p>Happy Birthday, my sweet Cutuu. May this year be your best one yet, filled with dreams coming true and beautiful new beginnings.</p>
            </div>
            <div class="signature">Always, Your Pretty Little Baby</div>
        </section>
    </div>
    
    <!-- Audio Controls -->
    <div class="audio-controls">
        <span class="audio-title">Birthday Song:</span>
        <button id="audioToggle"><i class="fas fa-music"></i></button>
        <button id="volumeUp"><i class="fas fa-volume-up"></i></button>
        <button id="volumeDown"><i class="fas fa-volume-down"></i></button>
    </div>
    
    <script>
        // Create heart trees
        function createHeartTrees() {
            const trees = [document.getElementById('tree1'), document.getElementById('tree2'), document.getElementById('tree3')];
            const heartCount = 15;
            
            trees.forEach(tree => {
                for (let i = 0; i < heartCount; i++) {
                    const heart = document.createElement('div');
                    heart.classList.add('heart');
                    
                    // Position hearts on the tree
                    const size = 20 + Math.random() * 15;
                    const left = 40 + Math.random() * 120;
                    const top = 60 + Math.random() * 160;
                    const delay = Math.random() * 2;
                    const hue = 330 + Math.random() * 30;
                    
                    heart.style.width = `${size}px`;
                    heart.style.height = `${size}px`;
                    heart.style.left = `${left}px`;
                    heart.style.top = `${top}px`;
                    heart.style.animationDelay = `${delay}s`;
                    heart.style.backgroundColor = `hsl(${hue}, 80%, 70%)`;
                    
                    tree.appendChild(heart);
                }
            });
        }
        
        // Create floating elements (hearts and stars)
        function createFloatingElements() {
            const container = document.getElementById('floatingElements');
            
            // Create hearts
            setInterval(() => {
                const heart = document.createElement('div');
                heart.classList.add('heart-shape');
                
                const size = 10 + Math.random() * 20;
                const left = Math.random() * 100;
                const duration = 10 + Math.random() * 20;
                const delay = Math.random() * 5;
                const hue = 330 + Math.random() * 30;
                
                heart.style.width = `${size}px`;
                heart.style.height = `${size}px`;
                heart.style.left = `${left}vw`;
                heart.style.animation = `floatUp ${duration}s linear ${delay}s infinite`;
                heart.style.backgroundColor = `hsl(${hue}, 80%, 75%)`;
                
                container.appendChild(heart);
                
                // Remove hearts after animation completes
                setTimeout(() => {
                    heart.remove();
                }, (duration + delay) * 1000);
            }, 300);
            
            // Create stars
            setInterval(() => {
                const star = document.createElement('div');
                star.classList.add('star');
                
                const size = 5 + Math.random() * 10;
                const left = Math.random() * 100;
                const duration = 5 + Math.random() * 10;
                const delay = Math.random() * 3;
                
                star.style.width = `${size}px`;
                star.style.height = `${size}px`;
                star.style.left = `${left}vw`;
                star.style.animation = `floatUp ${duration}s linear ${delay}s infinite, twinkle ${2 + Math.random() * 2}s ease-in-out ${delay}s infinite`;
                
                container.appendChild(star);
                
                // Remove stars after animation completes
                setTimeout(() => {
                    star.remove();
                }, (duration + delay) * 1000);
            }, 500);
        }
        
        // Create sparkle effects
        function createSparkles() {
            const container = document.getElementById('floatingElements');
            
            setInterval(() => {
                const sparkle = document.createElement('div');
                sparkle.classList.add('sparkle');
                
                const left = Math.random() * 100;
                const top = Math.random() * 100;
                const duration = 0.8 + Math.random() * 1.2;
                const size = 3 + Math.random() * 5;
                
                sparkle.style.left = `${left}vw`;
                sparkle.style.top = `${top}vh`;
                sparkle.style.width = `${size}px`;
                sparkle.style.height = `${size}px`;
                sparkle.style.animation = `sparkle ${duration}s ease-out`;
                
                container.appendChild(sparkle);
                
                // Remove sparkle after animation
                setTimeout(() => {
                    sparkle.remove();
                }, duration * 1000);
            }, 200);
        }
        
        // Light candles function
        function lightCandles() {
            const flames = document.querySelectorAll('.flame');
            const button = document.getElementById('lightButton');
            
            flames.forEach(flame => {
                flame.parentElement.classList.add('lit');
            });
            
            button.textContent = "Candles Lit!";
            button.disabled = true;
            
            // Create floating hearts above the cake
            for (let i = 0; i < 20; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.classList.add('heart-shape');
                    
                    heart.style.position = 'absolute';
                    heart.style.bottom = '200px';
                    heart.style.left = '50%';
                    heart.style.transform = 'translateX(-50%) rotate(-45deg)';
                    heart.style.animation = `floatUp ${5 + Math.random() * 3}s ease-in-out forwards`;
                    heart.style.width = '15px';
                    heart.style.height = '15px';
                    heart.style.backgroundColor = '#ff4081';
                    heart.style.zIndex = '20';
                    
                    document.querySelector('.cake-container').appendChild(heart);
                    
                    setTimeout(() => {
                        heart.remove();
                    }, 6000);
                }, i * 150);
            }
        }
        
        // Cut cake function
        function cutCake() {
            const cake = document.getElementById('birthdayCake');
            cake.classList.add('cut');
            
            // Create cake cutting effect
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    const sparkle = document.createElement('div');
                    sparkle.classList.add('sparkle');
                    
                    sparkle.style.position = 'absolute';
                    sparkle.style.bottom = '90px';
                    sparkle.style.left = `${50 + (Math.random() * 40 - 20)}%`;
                    sparkle.style.animation = `sparkle ${0.5 + Math.random() * 0.5}s ease-out`;
                    sparkle.style.width = '8px';
                    sparkle.style.height = '8px';
                    
                    cake.appendChild(sparkle);
                    
                    setTimeout(() => {
                        sparkle.remove();
                    }, 1000);
                }, i * 50);
            }
            
            setTimeout(() => {
                cake.classList.remove('cut');
            }, 500);
        }
        
        // Blow out candles function
        function blowCandles() {
            const flames = document.querySelectorAll('.flame');
            const lightButton = document.getElementById('lightButton');
            
            flames.forEach(flame => {
                flame.parentElement.classList.remove('lit');
            });
            
            lightButton.textContent = "Light the Candles";
            lightButton.disabled = false;
            
            // Create smoke effect
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const smoke = document.createElement('div');
                    smoke.style.position = 'absolute';
                    smoke.style.bottom = '160px';
                    smoke.style.left = '50%';
                    smoke.style.marginLeft = `${(i % 3) * 25 - 25}px`;
                    smoke.style.width = '10px';
                    smoke.style.height = '10px';
                    smoke.style.backgroundColor = '#ccc';
                    smoke.style.borderRadius = '50%';
                    smoke.style.opacity = '0.7';
                    smoke.style.zIndex = '20';
                    smoke.style.animation = `floatUp ${2 + Math.random() * 2}s ease-out forwards`;
                    
                    document.querySelector('.cake').appendChild(smoke);
                    
                    setTimeout(() => {
                        smoke.remove();
                    }, 3000);
                }, i * 100);
            }
        }
        
        // Audio control
        function setupAudio() {
            const audioToggle = document.getElementById('audioToggle');
            const volumeUp = document.getElementById('volumeUp');
            const volumeDown = document.getElementById('volumeDown');
            let audio;
            
            // Create audio element
            try {
                audio = new Audio('https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3');
                audio.loop = true;
                audio.volume = 0.7;
                
                // Attempt to autoplay with user interaction
                document.body.addEventListener('click', function initAudio() {
                    if (audio) {
                        audio.play().catch(e => console.log("Autoplay prevented:", e));
                    }
                    document.body.removeEventListener('click', initAudio);
                });
                
                audioToggle.addEventListener('click', () => {
                    if (audio.paused) {
                        audio.play();
                        audioToggle.innerHTML = '<i class="fas fa-pause"></i>';
                    } else {
                        audio.pause();
                        audioToggle.innerHTML = '<i class="fas fa-music"></i>';
                    }
                });
                
                volumeUp.addEventListener('click', () => {
                    if (audio.volume < 0.9) {
                        audio.volume += 0.1;
                    }
                });
                
                volumeDown.addEventListener('click', () => {
                    if (audio.volume > 0.1) {
                        audio.volume -= 0.1;
                    }
                });
            } catch (e) {
                console.log("Audio error:", e);
                audioToggle.style.display = 'none';
                volumeUp.style.display = 'none';
                volumeDown.style.display = 'none';
            }
        }
        
        // Initialize all effects
        document.addEventListener('DOMContentLoaded', () => {
            createHeartTrees();
            createFloatingElements();
            createSparkles();
            setupAudio();
            
            // Setup candle lighting
            document.getElementById('lightButton').addEventListener('click', lightCandles);
            
            // Setup cake cutting
            document.getElementById('cutButton').addEventListener('click', cutCake);
            
            // Setup blow out candles
            document.getElementById('blowButton').addEventListener('click', blowCandles);
        });
    </script>
</body>
</html>
