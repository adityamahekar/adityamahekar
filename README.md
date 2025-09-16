<h1 align="left">Hey 👋 What's up?</h1>

###

<h2 align="left">👋 Hi, I'm Aditya Mahekar</h2>


<p align="center">
  <img src="./luffy.jpg" alt="Aditya" height="250" style="border-radius: 15px;" />
</p>

# 👋 Hey there! I'm Aditya Mahekar
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aditya Mahekar - GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #f0f0f0;
            min-height: 100vh;
            overflow-x: hidden;
            padding: 20px;
            position: relative;
        }
        
        /* Animated background elements */
        .bg-bubbles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .bg-bubbles li {
            position: absolute;
            list-style: none;
            display: block;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            bottom: -160px;
            border-radius: 50%;
            animation: square 25s infinite;
            transition-timing-function: linear;
        }
        
        .bg-bubbles li:nth-child(1) {
            left: 10%;
            animation-delay: 0s;
            width: 80px;
            height: 80px;
        }
        
        .bg-bubbles li:nth-child(2) {
            left: 20%;
            animation-delay: 2s;
            animation-duration: 17s;
            width: 60px;
            height: 60px;
        }
        
        .bg-bubbles li:nth-child(3) {
            left: 25%;
            animation-delay: 4s;
            width: 120px;
            height: 120px;
        }
        
        .bg-bubbles li:nth-child(4) {
            left: 40%;
            animation-delay: 0s;
            animation-duration: 22s;
            width: 160px;
            height: 160px;
        }
        
        .bg-bubbles li:nth-child(5) {
            left: 70%;
            width: 100px;
            height: 100px;
        }
        
        .bg-bubbles li:nth-child(6) {
            left: 80%;
            animation-delay: 3s;
            width: 120px;
            height: 120px;
        }
        
        .bg-bubbles li:nth-child(7) {
            left: 32%;
            animation-delay: 7s;
            width: 140px;
            height: 140px;
        }
        
        .bg-bubbles li:nth-child(8) {
            left: 55%;
            animation-delay: 15s;
            animation-duration: 40s;
            width: 40px;
            height: 40px;
        }
        
        .bg-bubbles li:nth-child(9) {
            left: 25%;
            animation-delay: 2s;
            animation-duration: 40s;
            width: 20px;
            height: 20px;
        }
        
        .bg-bubbles li:nth-child(10) {
            left: 90%;
            animation-delay: 11s;
            width: 80px;
            height: 80px;
        }
        
        @keyframes square {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
                border-radius: 50%;
            }
            100% {
                transform: translateY(-1000px) rotate(720deg);
                opacity: 0;
                border-radius: 50%;
            }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
            z-index: 1;
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #6FCF97;
            box-shadow: 0 0 25px rgba(111, 207, 151, 0.6);
            margin: 0 auto 20px;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #6FCF97, #56CCF2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from {
                text-shadow: 0 0 10px rgba(111, 207, 151, 0.5);
            }
            to {
                text-shadow: 0 0 20px rgba(111, 207, 151, 0.8), 0 0 30px rgba(111, 207, 151, 0.6);
            }
        }
        
        h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #56CCF2;
        }
        
        .typing-text {
            font-size: 1.5rem;
            margin: 20px 0;
            min-height: 80px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-links a {
            color: #f0f0f0;
            font-size: 2rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            color: #6FCF97;
            transform: translateY(-5px);
        }
        
        .section {
            background: rgba(25, 25, 50, 0.7);
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            transform: translateY(50px);
            opacity: 0;
            transition: all 0.8s ease;
        }
        
        .section.visible {
            transform: translateY(0);
            opacity: 1;
        }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #6FCF97;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 50px;
            height: 3px;
            background: linear-gradient(45deg, #6FCF97, #56CCF2);
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 30px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }
        
        .tech-item:hover {
            background: rgba(111, 207, 151, 0.2);
            transform: translateY(-5px);
        }
        
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            background: rgba(111, 207, 151, 0.2);
            transform: translateY(-5px);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #56CCF2;
            margin-bottom: 10px;
        }
        
        .activity-graph {
            background: rgba(0, 0, 0, 0.2);
            border-radius: 10px;
            padding: 20px;
            margin: 30px 0;
            height: 200px;
            display: flex;
            align-items: flex-end;
            gap: 5px;
        }
        
        .graph-bar {
            background: linear-gradient(to top, #6FCF97, #56CCF2);
            border-radius: 5px 5px 0 0;
            width: 100%;
            transition: height 1s ease;
        }
        
        .fun-fact {
            background: rgba(111, 207, 151, 0.1);
            border-left: 5px solid #6FCF97;
            padding: 20px;
            border-radius: 5px;
            margin: 30px 0;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(111, 207, 151, 0.4);
            }
            70% {
                box-shadow: 0 0 0 10px rgba(111, 207, 151, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(111, 207, 151, 0);
            }
        }
        
        .quote {
            text-align: center;
            font-style: italic;
            margin: 40px 0;
            padding: 20px;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.05);
            position: relative;
        }
        
        .quote::before, .quote::after {
            content: '"';
            font-size: 3rem;
            color: #6FCF97;
            position: absolute;
        }
        
        .quote::before {
            top: 0;
            left: 20px;
        }
        
        .quote::after {
            bottom: 0;
            right: 20px;
        }
        
        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            .stats {
                grid-template-columns: 1fr;
            }
            
            .tech-stack {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <ul class="bg-bubbles">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
    
    <div class="container">
        <header>
            <img src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" alt="Aditya Mahekar" class="profile-img">
            <h1>Aditya Mahekar</h1>
            <h2>Full-Stack Developer & Cloud Enthusiast</h2>
            
            <div class="typing-text">
                <span id="typing"></span><span id="cursor">|</span>
            </div>
            
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
        </header>
        
        <section class="section">
            <h3 class="section-title">About Me</h3>
            <p>🎓 Computer Science Engineering student at BMS Institute of Technology and Management</p>
            <p>💡 Passionate about creating innovative solutions through code</p>
            <p>🌱 Currently exploring Cloud Technologies and DevOps Practices</p>
            <p>🎯 Goal: To become a versatile full-stack developer with cloud expertise</p>
        </section>
        
        <section class="section">
            <h3 class="section-title">Tech Stack</h3>
            <div class="tech-stack">
                <div class="tech-item">
                    <i class="fab fa-html5"></i>
                    <span>HTML5</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-css3-alt"></i>
                    <span>CSS3</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-js-square"></i>
                    <span>JavaScript</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-node-js"></i>
                    <span>Node.js</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-python"></i>
                    <span>Python</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-java"></i>
                    <span>Java</span>
                </div>
                <div class="tech-item">
                    <i class="fas fa-database"></i>
                    <span>MongoDB</span>
                </div>
                <div class="tech-item">
                    <i class="fas fa-database"></i>
                    <span>PostgreSQL</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-git-alt"></i>
                    <span>Git</span>
                </div>
                <div class="tech-item">
                    <i class="fab fa-linux"></i>
                    <span>Linux</span>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h3 class="section-title">GitHub Stats</h3>
            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">150+</div>
                    <div class="stat-label">Contributions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">25</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">15</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">10</div>
                    <div class="stat-label">Technologies</div>
                </div>
            </div>
            
            <h4>Activity Graph</h4>
            <div class="activity-graph">
                <div class="graph-bar" style="height: 30%;"></div>
                <div class="graph-bar" style="height: 60%;"></div>
                <div class="graph-bar" style="height: 80%;"></div>
                <div class="graph-bar" style="height: 40%;"></div>
                <div class="graph-bar" style="height: 70%;"></div>
                <div class="graph-bar" style="height: 90%;"></div>
                <div class="graph-bar" style="height: 50%;"></div>
            </div>
        </section>
        
        <section class="section">
            <h3 class="section-title">Fun Facts</h3>
            <div class="fun-fact">
                <p>⚡ I'm secretly a Straw Hat pirate ☠️ sailing through the seas of code! 🍖</p>
                <p>🔭 I'm currently working on improving my Data Structures & Algorithms skills</p>
                <p>🌱 I'm learning Cloud Computing and System Design</p>
                <p>👯 I'm looking to collaborate on Open Source Projects</p>
            </div>
        </section>
        
        <div class="quote">
            <p>"Don't wait for opportunity. Create it."</p>
            <p>Let's collaborate and build something amazing!</p>
        </div>
        
        <footer>
            <p>⭐️ From <a href="https://github.com/adityamahekar" style="color: #6FCF97;">adityamahekar</a></p>
            <p>Made with ❤️ using HTML, CSS, and JavaScript</p>
        </footer>
    </div>

    <script>
        // Typing animation
        const texts = [
            "Full-Stack Developer",
            "Cloud Enthusiast",
            "Problem Solver",
            "Creative Thinker",
            "Tech Innovator"
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        let typingDelay = 100;
        let erasingDelay = 50;
        let newTextDelay = 2000;
        
        function type() {
            const currentText = texts[textIndex];
            const typingElement = document.getElementById("typing");
            const cursorElement = document.getElementById("cursor");
            
            if (isDeleting) {
                // Remove char
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
                typingDelay = erasingDelay;
            } else {
                // Add char
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
                typingDelay = 100;
            }
            
            // Check if current text is complete
            if (!isDeleting && charIndex === currentText.length) {
                isDeleting = true;
                typingDelay = newTextDelay;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex++;
                if (textIndex === texts.length) textIndex = 0;
                typingDelay = 500;
            }
            
            setTimeout(type, typingDelay);
        }
        
        // Cursor blink animation
        function blinkCursor() {
            const cursor = document.getElementById("cursor");
            cursor.style.opacity = (cursor.style.opacity === '0' ? '1' : '0');
            setTimeout(blinkCursor, 500);
        }
        
        // Scroll animation for sections
        function checkScroll() {
            const sections = document.querySelectorAll('.section');
            const windowHeight = window.innerHeight;
            
            sections.forEach(section => {
                const position = section.getBoundingClientRect().top;
                
                if (position < windowHeight * 0.85) {
                    section.classList.add('visible');
                }
            });
        }
        
        // Animate graph bars
        function animateBars() {
            const bars = document.querySelectorAll('.graph-bar');
            bars.forEach((bar, index) => {
                setTimeout(() => {
                    bar.style.height = bar.style.height;
                }, index * 200);
            });
        }
        
        // Initialize everything
        document.addEventListener('DOMContentLoaded', function() {
            // Start animations
            setTimeout(type, 1000);
            setTimeout(blinkCursor, 600);
            
            // Check scroll position
            window.addEventListener('scroll', checkScroll);
            checkScroll(); // Check initial position
            
            // Animate graph bars after a delay
            setTimeout(animateBars, 1500);
        });
    </script>
</body>
</html>

---

<div align="center">
  
  ⭐️ From [adityamahekar](https://github.com/adityamahekar)
  
</div>
