<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anipat Jaiworn - Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, #0ea5e9 0%, #3b82f6 100%);
            border-radius: 20px;
            margin-bottom: 40px;
            box-shadow: 0 20px 60px rgba(14, 165, 233, 0.3);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInDown 1s ease;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .typing-text {
            font-size: 1.5em;
            margin: 20px 0;
            min-height: 40px;
            color: #fff;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .social-badge {
            display: inline-block;
            padding: 12px 24px;
            background: rgba(255,255,255,0.2);
            border-radius: 25px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .social-badge:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        /* About Section */
        .about-section {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 40px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
        }

        .code-block {
            background: #0f172a;
            border-radius: 10px;
            padding: 25px;
            font-family: 'Courier New', monospace;
            overflow-x: auto;
            border-left: 4px solid #0ea5e9;
            margin: 20px 0;
        }

        .code-block code {
            color: #22d3ee;
        }

        /* Skills Section */
        .skills-section {
            margin-bottom: 40px;
        }

        .skill-category {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 25px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(14, 165, 233, 0.2);
        }

        .skill-category h3 {
            color: #0ea5e9;
            margin-bottom: 20px;
            font-size: 1.8em;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #0ea5e9 0%, #3b82f6 100%);
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(14, 165, 233, 0.3);
        }

        .skill-tag:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 20px rgba(14, 165, 233, 0.5);
        }

        /* Stats Section */
        .stats-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .stat-card {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(14, 165, 233, 0.3);
        }

        .stat-number {
            font-size: 3em;
            font-weight: bold;
            color: #0ea5e9;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1.1em;
            color: #94a3b8;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 20px;
            background: rgba(30, 41, 59, 0.6);
            border-radius: 20px;
            margin-top: 40px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
        }

        .footer-emoji {
            font-size: 2em;
            margin-bottom: 15px;
        }

        /* Animations */
        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        .floating {
            animation: float 3s ease-in-out infinite;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }

            .typing-text {
                font-size: 1.2em;
            }

            .skill-category {
                padding: 20px;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 12px;
        }

        ::-webkit-scrollbar-track {
            background: #0f172a;
        }

        ::-webkit-scrollbar-thumb {
            background: #0ea5e9;
            border-radius: 6px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: #3b82f6;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="header-content">
                <div class="floating">
                    <h1>👨‍💻 Anipat Jaiworn</h1>
                </div>
                <div class="typing-text" id="typing-text"></div>
                <p>📍 Based in Chiang Rai, Thailand</p>
                
                <div class="social-links">
                    <a href="mailto:Anipat5556666@gmail.com" class="social-badge">📧 Email</a>
                    <a href="https://github.com/FlukAnipat" class="social-badge">💻 GitHub</a>
                    <a href="https://gitlab.com/FlukAnipat" class="social-badge">🦊 GitLab</a>
                    <a href="https://www.instagram.com/fluk__anipat____" class="social-badge">📷 Instagram</a>
                    <a href="https://facebook.com/Fluk.Anipat5556666" class="social-badge">📘 Facebook</a>
                    <a href="https://discord.com/users/fluk_donovan" class="social-badge">💬 Discord</a>
                </div>
            </div>
        </div>

        <!-- About Section -->
        <div class="about-section">
            <h2 style="color: #0ea5e9; margin-bottom: 25px; font-size: 2.5em;">🚀 About Me</h2>
            <div class="code-block">
                <code>
const anipat = {<br>
&nbsp;&nbsp;location: <span style="color: #fbbf24;">"Chiang Rai, Thailand 🇹🇭"</span>,<br>
&nbsp;&nbsp;role: <span style="color: #fbbf24;">"Full Stack Developer & Web Dev Teacher"</span>,<br>
&nbsp;&nbsp;passion: [<span style="color: #fbbf24;">"Coding"</span>, <span style="color: #fbbf24;">"Teaching"</span>, <span style="color: #fbbf24;">"Open Source"</span>],<br>
&nbsp;&nbsp;currentFocus: <span style="color: #fbbf24;">"Building scalable web applications"</span>,<br>
&nbsp;&nbsp;learning: [<span style="color: #fbbf24;">"NestJS"</span>, <span style="color: #fbbf24;">"Nuxt.js"</span>, <span style="color: #fbbf24;">"Cloud Architecture"</span>],<br>
&nbsp;&nbsp;funFact: <span style="color: #fbbf24;">"I debug code faster than I drink coffee ☕"</span><br>
};
                </code>
            </div>
            <p style="text-align: center; margin-top: 20px; font-size: 1.2em;">
                🎓 <strong>University Account:</strong> 
                <a href="https://github.com/651998013" style="color: #0ea5e9; text-decoration: none;">@651998013</a>
            </p>
        </div>

        <!-- Stats Section -->
        <h2 style="color: #0ea5e9; margin-bottom: 25px; font-size: 2.5em; text-align: center;">📊 My Journey</h2>
        <div class="stats-section">
            <div class="stat-card">
                <div class="stat-number">5+</div>
                <div class="stat-label">Years of Coding</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">20+</div>
                <div class="stat-label">Technologies</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">∞</div>
                <div class="stat-label">Passion for Learning</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">100%</div>
                <div class="stat-label">Dedication</div>
            </div>
        </div>

        <!-- Skills Section -->
        <h2 style="color: #0ea5e9; margin-bottom: 25px; font-size: 2.5em; text-align: center;">💻 Tech Stack</h2>
        <div class="skills-section">
            <div class="skill-category">
                <h3>🧩 Core Languages</h3>
                <div class="skill-tags">
                    <span class="skill-tag">C</span>
                    <span class="skill-tag">C++</span>
                    <span class="skill-tag">C#</span>
                    <span class="skill-tag">Java</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">TypeScript</span>
                    <span class="skill-tag">PHP</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>🎨 Frontend Development</h3>
                <div class="skill-tags">
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">Bootstrap</span>
                    <span class="skill-tag">Tailwind CSS</span>
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Next.js</span>
                    <span class="skill-tag">Vue.js</span>
                    <span class="skill-tag">Nuxt.js</span>
                    <span class="skill-tag">Vuetify 2</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>⚙️ Backend Development</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Express.js</span>
                    <span class="skill-tag">NestJS</span>
                    <span class="skill-tag">Spring Boot</span>
                    <span class="skill-tag">.NET</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>🗄️ Database & Cloud</h3>
                <div class="skill-tags">
                    <span class="skill-tag">MySQL</span>
                    <span class="skill-tag">Google Cloud Platform</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>🛠️ Tools & Design</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Git</span>
                    <span class="skill-tag">VS Code</span>
                    <span class="skill-tag">Figma</span>
                    <span class="skill-tag">Photoshop</span>
                    <span class="skill-tag">Illustrator</span>
                    <span class="skill-tag">Premiere Pro</span>
                    <span class="skill-tag">Blender</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>☁️ Cloud & IoT</h3>
                <div class="skill-tags">
                    <span class="skill-tag">GCP</span>
                    <span class="skill-tag">Arduino</span>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="footer-emoji">💙</div>
            <h3 style="color: #0ea5e9; margin-bottom: 15px;">Let's Connect!</h3>
            <p style="margin-bottom: 20px;">
                I'm always interested in collaborating on exciting projects or just chatting about tech!
            </p>
            <p style="color: #94a3b8;">
                💬 Looking for collaboration opportunities in:<br>
                Open Source Projects • Web Development • Teaching & Mentoring • IoT & Embedded Systems
            </p>
            <div style="margin-top: 30px; padding-top: 30px; border-top: 1px solid rgba(255,255,255,0.1);">
                <p style="color: #64748b;">⭐ Made with Love by Anipat Jaiworn</p>
                <p style="color: #64748b; margin-top: 10px;">© 2024 • Open Source 💚</p>
            </div>
        </div>
    </div>

    <script>
        // Typing Animation
        const texts = [
            "Full Stack Developer 💻",
            "Web Development Teacher 📘",
            "Open Source Enthusiast 🌟",
            "Based in Chiang Rai, Thailand 🇹🇭",
            "Let's Build Something Amazing! 🚀"
        ];
        
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        let typingSpeed = 100;

        function typeText() {
            const currentText = texts[textIndex];
            const displayText = isDeleting 
                ? currentText.substring(0, charIndex - 1)
                : currentText.substring(0, charIndex + 1);
            
            document.getElementById('typing-text').textContent = displayText;

            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }

            charIndex = isDeleting ? charIndex - 1 : charIndex + 1;
            
            const speed = isDeleting ? 50 : 100;
            setTimeout(typeText, speed);
        }

        // Start typing animation
        typeText();

        // Add scroll animation
        window.addEventListener('scroll', () => {
            const elements = document.querySelectorAll('.skill-category, .stat-card');
            elements.forEach(element => {
                const position = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (position < screenPosition) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        });

        // Initial setup for scroll animation
        document.querySelectorAll('.skill-category, .stat-card').forEach(element => {
            element.style.opacity = '0';
            element.style.transform = 'translateY(50px)';
            element.style.transition = 'all 0.6s ease';
        });
    </script>
</body>
</html>
