<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammad Zaqeem - AI Researcher</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #f0f0f0;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
            overflow: hidden;
        }
        
        .header-gif {
            width: 100%;
            max-width: 800px;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            margin: 0 auto;
            display: block;
        }
        
        .profile-title {
            margin: 25px 0 15px;
            font-size: 3.5rem;
            background: linear-gradient(45deg, #2ff7fc, #6a11cb);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: titleGlow 3s infinite alternate;
        }
        
        .profile-subtitle {
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: #b0e0e6;
            font-weight: 400;
        }
        
        .typing-container {
            background: rgba(16, 42, 67, 0.7);
            border-radius: 50px;
            padding: 15px 30px;
            display: inline-block;
            margin: 20px auto;
            border: 1px solid rgba(47, 247, 252, 0.3);
            backdrop-filter: blur(5px);
        }
        
        .typing-text {
            font-family: 'Fira Code', monospace;
            font-size: 1.4rem;
            color: #2ff7fc;
            text-align: center;
        }
        
        /* Profile Image */
        .profile-container {
            margin: 30px auto;
            width: 220px;
            height: 220px;
            border-radius: 50%;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: pulse 2s infinite;
        }
        
        .profile-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 5px solid #2ff7fc;
            object-fit: cover;
            box-shadow: 0 0 25px rgba(47, 247, 252, 0.6);
            transition: transform 0.5s ease;
        }
        
        .profile-image:hover {
            transform: scale(1.05);
        }
        
        /* Sections */
        section {
            background: rgba(16, 42, 67, 0.5);
            border-radius: 20px;
            padding: 30px;
            margin: 30px 0;
            border: 1px solid rgba(47, 247, 252, 0.2);
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
            border-color: rgba(47, 247, 252, 0.4);
        }
        
        h2 {
            font-size: 2rem;
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 3px solid #2ff7fc;
            color: #2ff7fc;
            display: inline-block;
        }
        
        /* About Me */
        .about-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .education, .research, .focus {
            background: rgba(11, 32, 53, 0.7);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(47, 247, 252, 0.2);
        }
        
        .focus-items {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
        }
        
        .focus-item {
            background: rgba(47, 247, 252, 0.1);
            padding: 8px 15px;
            border-radius: 30px;
            border: 1px solid rgba(47, 247, 252, 0.3);
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }
        
        .focus-item:hover {
            background: rgba(47, 247, 252, 0.2);
            transform: translateY(-3px);
        }
        
        /* Tech Stack */
        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .tech-category {
            background: rgba(11, 32, 53, 0.7);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(47, 247, 252, 0.2);
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .badge {
            background: rgba(47, 247, 252, 0.1);
            padding: 8px 15px;
            border-radius: 5px;
            border: 1px solid rgba(47, 247, 252, 0.3);
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
        }
        
        .badge:hover {
            background: rgba(47, 247, 252, 0.2);
            transform: translateY(-3px);
        }
        
        /* Stats */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 20px;
        }
        
        .stat-box {
            background: rgba(11, 32, 53, 0.7);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(47, 247, 252, 0.2);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .stat-box:hover {
            transform: scale(1.03);
        }
        
        .stat-title {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #2ff7fc;
        }
        
        .stat-content {
            font-size: 2.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, #2ff7fc, #6a11cb);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        /* Connect */
        .connect-container {
            text-align: center;
            padding: 40px;
        }
        
        .quote {
            font-size: 1.8rem;
            font-style: italic;
            margin: 30px 0;
            color: #b0e0e6;
            position: relative;
            max-width: 800px;
            margin: 40px auto;
            padding: 0 20px;
        }
        
        .quote::before, .quote::after {
            content: '"';
            font-size: 3rem;
            color: #2ff7fc;
            position: absolute;
            opacity: 0.5;
        }
        
        .quote::before {
            top: -20px;
            left: -10px;
        }
        
        .quote::after {
            bottom: -40px;
            right: -10px;
        }
        
        .author {
            font-size: 1.5rem;
            color: #2ff7fc;
            margin-top: 10px;
            font-weight: 600;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background: rgba(47, 247, 252, 0.1);
            border: 2px solid rgba(47, 247, 252, 0.3);
            font-size: 2rem;
            color: #2ff7fc;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background: rgba(47, 247, 252, 0.2);
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 0 25px rgba(47, 247, 252, 0.4);
        }
        
        .profile-views {
            background: rgba(16, 42, 67, 0.7);
            padding: 15px 30px;
            border-radius: 50px;
            display: inline-block;
            margin-top: 20px;
            font-size: 1.1rem;
            border: 1px solid rgba(47, 247, 252, 0.3);
            animation: pulse 2s infinite;
        }
        
        /* Animations */
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(47, 247, 252, 0.6); }
            70% { box-shadow: 0 0 0 15px rgba(47, 247, 252, 0); }
            100% { box-shadow: 0 0 0 0 rgba(47, 247, 252, 0); }
        }
        
        @keyframes titleGlow {
            0% { text-shadow: 0 0 5px rgba(47, 247, 252, 0.5); }
            100% { text-shadow: 0 0 20px rgba(47, 247, 252, 0.8), 0 0 30px rgba(47, 247, 252, 0.6); }
        }
        
        .fade-in {
            animation: fadeIn 1s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .profile-title {
                font-size: 2.5rem;
            }
            
            .profile-subtitle {
                font-size: 1.4rem;
            }
            
            .typing-text {
                font-size: 1.1rem;
            }
            
            .profile-container {
                width: 180px;
                height: 180px;
            }
            
            .profile-image {
                width: 160px;
                height: 160px;
            }
            
            .social-links {
                gap: 15px;
            }
            
            .social-link {
                width: 60px;
                height: 60px;
                font-size: 1.7rem;
            }
            
            .quote {
                font-size: 1.4rem;
            }
        }
        
        @media (max-width: 480px) {
            .profile-title {
                font-size: 2rem;
            }
            
            .typing-container {
                padding: 10px 20px;
            }
            
            .typing-text {
                font-size: 1rem;
            }
            
            section {
                padding: 20px;
            }
            
            .social-links {
                gap: 10px;
            }
            
            .social-link {
                width: 50px;
                height: 50px;
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="fade-in">
            <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="Header GIF" class="header-gif">
            <h1 class="profile-title">Hi 👋, I'm Muhammad Zaqeem</h1>
            <h2 class="profile-subtitle">AI Researcher | VLMs & LLMs | Deep Learning Enthusiast</h2>
            
            <div class="typing-container">
                <div class="typing-text">AI Researcher | LLMs & VLMs | Passionate about Multi-Modal AI</div>
            </div>
            
            <div class="profile-container">
                <img src="https://github.com/zaqeem.png" alt="Profile Image" class="profile-image">
            </div>
        </header>
        
        <section class="fade-in">
            <h2>🚀 About Me</h2>
            <div class="about-content">
                <div class="education">
                    <h3><i class="fas fa-graduation-cap"></i> Education</h3>
                    <p>🎓 <strong>BSCS</strong> (2022–2026) – Brains Institute, Peshawar</p>
                </div>
                
                <div class="research">
                    <h3><i class="fas fa-flask"></i> Research</h3>
                    <p>🔬 Research Assistant at <strong>DIP Lab</strong>, Islamia College University</p>
                </div>
                
                <div class="focus">
                    <h3><i class="fas fa-brain"></i> Research Focus</h3>
                    <div class="focus-items">
                        <div class="focus-item">🤖 LLMs: Transformers, fine-tuning</div>
                        <div class="focus-item">👁️ VLMs: CLIP, Flamingo</div>
                        <div class="focus-item">🧠 Deep Learning: CNNs, attention</div>
                        <div class="focus-item">🧬 Generative AI: GANs, Diffusion</div>
                        <div class="focus-item">📷 Computer Vision</div>
                        <div class="focus-item">💬 NLP</div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="fade-in">
            <h2>🛠️ Tech Stack & Tools</h2>
            <div class="tech-stack">
                <div class="tech-category">
                    <h3><i class="fas fa-code"></i> Languages & Frameworks</h3>
                    <div class="badges">
                        <div class="badge"><i class="fab fa-python"></i> Python</div>
                        <div class="badge"><i class="fas fa-copyright"></i> C++</div>
                        <div class="badge"><i class="fab fa-java"></i> Java</div>
                        <div class="badge"><i class="fab fa-js"></i> JavaScript</div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3><i class="fas fa-robot"></i> AI & Deep Learning</h3>
                    <div class="badges">
                        <div class="badge"><i class="fas fa-fire"></i> PyTorch</div>
                        <div class="badge"><i class="fas fa-project-diagram"></i> TensorFlow</div>
                        <div class="badge"><i class="fas fa-smile"></i> HuggingFace</div>
                        <div class="badge"><i class="fas fa-brain"></i> OpenAI</div>
                        <div class="badge"><i class="fas fa-exchange-alt"></i> Transformers</div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3><i class="fas fa-chart-bar"></i> Data Science</h3>
                    <div class="badges">
                        <div class="badge"><i class="fas fa-table"></i> Pandas</div>
                        <div class="badge"><i class="fas fa-calculator"></i> NumPy</div>
                        <div class="badge"><i class="fas fa-chart-line"></i> Matplotlib</div>
                        <div class="badge"><i class="fas fa-chart-pie"></i> Plotly</div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3><i class="fas fa-tools"></i> Development Tools</h3>
                    <div class="badges">
                        <div class="badge"><i class="fas fa-code"></i> VS Code</div>
                        <div class="badge"><i class="fab fa-git-alt"></i> Git</div>
                        <div class="badge"><i class="fab fa-docker"></i> Docker</div>
                        <div class="badge"><i class="fas fa-stream"></i> Streamlit</div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="fade-in">
            <h2>📈 GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-box">
                    <div class="stat-title">Repositories</div>
                    <div class="stat-content">42</div>
                </div>
                <div class="stat-box">
                    <div class="stat-title">Commits (2023)</div>
                    <div class="stat-content">1,247</div>
                </div>
                <div class="stat-box">
                    <div class="stat-title">Top Languages</div>
                    <div class="stat-content">Python</div>
                </div>
            </div>
        </section>
        
        <section class="connect-container fade-in">
            <h2>🔗 Let's Connect</h2>
            <div class="social-links">
                <a href="mailto:muhammadzaqeem@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="https://github.com/zaqeem" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
                <a href="#" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="#" class="social-link">
                    <i class="fab fa-twitter"></i>
                </a>
            </div>
            
            <div class="quote">
                "Building intelligent systems with code, research, and curiosity."
                <div class="author">— Muhammad Zaqeem</div>
            </div>
            
            <div class="profile-views">
                <i class="fas fa-eye"></i> Profile Views: 1,284
            </div>
        </section>
    </div>

    <script>
        // Simple typing effect for the tagline
        const taglines = [
            "AI Researcher | LLMs & VLMs",
            "Passionate about Multi-Modal AI",
            "Deep Learning | Vision Language Models"
        ];
        
        let currentTagline = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.querySelector('.typing-text');
        
        function type() {
            const fullTagline = taglines[currentTagline];
            
            if (isDeleting) {
                typingElement.textContent = fullTagline.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = fullTagline.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === fullTagline.length) {
                isDeleting = true;
                setTimeout(type, 1500);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                currentTagline = (currentTagline + 1) % taglines.length;
                setTimeout(type, 500);
            } else {
                setTimeout(type, isDeleting ? 50 : 100);
            }
        }
        
        // Start typing effect after page loads
        window.onload = function() {
            setTimeout(type, 1000);
        };
    </script>
</body>
</html>
