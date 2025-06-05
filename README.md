<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Durgesh Singh - Data Scientist</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            overflow-x: hidden;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            overflow: hidden;
        }

        .header-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(120, 219, 255, 0.2) 0%, transparent 50%);
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-20px) rotate(1deg); }
            66% { transform: translateY(-10px) rotate(-1deg); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-title {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #fff, #f0f0f0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 50px rgba(255, 255, 255, 0.3);
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 4vw, 2rem);
            margin-bottom: 2rem;
            opacity: 0.9;
            font-weight: 300;
        }

        .wave-emoji {
            display: inline-block;
            animation: wave 2s infinite;
            transform-origin: 70% 70%;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(14deg); }
            20% { transform: rotate(-8deg); }
            40%, 60% { transform: rotate(14deg); }
            50% { transform: rotate(-8deg); }
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
        }

        nav.scrolled {
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: white;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            transform: translateY(-2px);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: white;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Sections */
        section {
            padding: 5rem 0;
            position: relative;
        }

        .section-title {
            font-size: 3rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(45deg, #fff, #f0f0f0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .skill-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 2rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }

        .skill-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .skill-card:hover::before {
            left: 100%;
        }

        .skill-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .skill-number {
            font-size: 2rem;
            font-weight: 700;
            color: #64ffda;
            margin-bottom: 1rem;
        }

        .skill-name {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .skill-description {
            opacity: 0.8;
            line-height: 1.6;
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
            cursor: pointer;
        }

        .tech-item:hover {
            transform: translateY(-5px) rotate(5deg);
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            display: block;
        }

        .tech-name {
            font-size: 0.9rem;
            font-weight: 500;
            opacity: 0.9;
        }

        /* Contact Section */
        .contact-content {
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-btn {
            display: inline-block;
            background: linear-gradient(45deg, #64ffda, #00bcd4);
            color: #1a1a1a;
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            margin: 1rem;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .contact-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .contact-btn:hover::before {
            left: 100%;
        }

        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(100, 255, 218, 0.3);
        }

        /* Floating Particles */
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: floatParticle 20s infinite linear;
        }

        .particle:nth-child(1) {
            width: 10px;
            height: 10px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .particle:nth-child(2) {
            width: 6px;
            height: 6px;
            top: 60%;
            left: 80%;
            animation-delay: 5s;
        }

        .particle:nth-child(3) {
            width: 8px;
            height: 8px;
            top: 80%;
            left: 20%;
            animation-delay: 10s;
        }

        @keyframes floatParticle {
            0% {
                transform: translateY(0px) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
                gap: 1rem;
            }
        }

        /* Scroll Indicator */
        .scroll-indicator {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: rgba(255, 255, 255, 0.1);
            z-index: 1001;
        }

        .scroll-progress {
            height: 100%;
            background: linear-gradient(90deg, #64ffda, #00bcd4);
            width: 0%;
            transition: width 0.1s ease;
        }
    </style>
</head>
<body>
    <div class="scroll-indicator">
        <div class="scroll-progress" id="scrollProgress"></div>
    </div>

    <nav id="navbar">
        <div class="container">
            <div class="nav-content">
                <div class="logo">DS</div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#tech">Tech Stack</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <header id="home">
        <div class="header-bg"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="container">
            <div class="hero-content">
                <h1 class="hero-title">Hi <span class="wave-emoji">👋</span>, I'm Durgesh Singh</h1>
                <p class="hero-subtitle">A passionate Data Scientist from India</p>
                <p style="font-size: 1.2rem; opacity: 0.8; max-width: 600px; margin: 0 auto;">
                    Transforming data into insights, building intelligent systems, and pushing the boundaries of AI
                </p>
            </div>
        </div>
    </header>

    <section id="skills">
        <div class="container">
            <h2 class="section-title">Technical Expertise</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-number">01</div>
                    <h3 class="skill-name">Python Mastery</h3>
                    <p class="skill-description">Advanced proficiency in Python programming with extensive experience in data manipulation, analysis, and automation.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-number">02</div>
                    <h3 class="skill-name">Machine Learning</h3>
                    <p class="skill-description">Deep expertise in ML algorithms, model development, and statistical analysis for predictive analytics.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-number">03</div>
                    <h3 class="skill-name">Deep Learning</h3>
                    <p class="skill-description">Neural network architectures, TensorFlow, PyTorch, and advanced deep learning techniques.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-number">04</div>
                    <h3 class="skill-name">Computer Vision</h3>
                    <p class="skill-description">Image processing, object detection, and visual recognition systems using OpenCV and modern frameworks.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-number">05</div>
                    <h3 class="skill-name">Natural Language Processing</h3>
                    <p class="skill-description">Text analysis, sentiment analysis, and language model development for intelligent text processing.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-number">06</div>
                    <h3 class="skill-name">MLOps</h3>
                    <p class="skill-description">Model deployment, monitoring, and production pipeline management for scalable ML systems.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-number">07</div>
                    <h3 class="skill-name">Generative AI</h3>
                    <p class="skill-description">Cutting-edge AI models, prompt engineering, and next-generation artificial intelligence applications.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="tech">
        <div class="container">
            <h2 class="section-title">Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <span class="tech-icon">🐍</span>
                    <div class="tech-name">Python</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🤖</span>
                    <div class="tech-name">TensorFlow</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🔥</span>
                    <div class="tech-name">PyTorch</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">📊</span>
                    <div class="tech-name">Pandas</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🧠</span>
                    <div class="tech-name">Scikit-learn</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">👁️</span>
                    <div class="tech-name">OpenCV</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">☁️</span>
                    <div class="tech-name">AWS</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🌐</span>
                    <div class="tech-name">Azure</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🏗️</span>
                    <div class="tech-name">GCP</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐳</span>
                    <div class="tech-name">Docker</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🗄️</span>
                    <div class="tech-name">MongoDB</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐬</span>
                    <div class="tech-name">MySQL</div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div class="contact-content">
                <h2 class="section-title">Let's Connect</h2>
                <p style="font-size: 1.2rem; margin-bottom: 2rem; opacity: 0.9;">
                    Ready to collaborate on exciting data science projects? Let's build something amazing together!
                </p>
                <a href="mailto:durgeshsingh12712@gmail.com" class="contact-btn">
                    📧 Get In Touch
                </a>
                <a href="https://github.com/Durgeshsingh12712?tab=repositories" target="_blank" class="contact-btn">
                    👨‍💻 View Projects
                </a>
            </div>
        </div>
    </section>

    <script>
        // Scroll Progress Indicator
        window.addEventListener('scroll', () => {
            const scrollProgress = document.getElementById('scrollProgress');
            const scrollHeight = document.documentElement.scrollHeight - window.innerHeight;
            const scrolled = (window.scrollY / scrollHeight) * 100;
            scrollProgress.style.width = scrolled + '%';
        });

        // Navbar Scroll Effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Smooth Scrolling for Navigation Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Intersection Observer for Animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe skill cards and tech items
        document.querySelectorAll('.skill-card, .tech-item').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'all 0.6s ease';
            observer.observe(el);
        });

        // Add random floating animations to particles
        document.querySelectorAll('.particle').forEach((particle, index) => {
            setInterval(() => {
                const randomX = Math.random() * 100;
                const randomY = Math.random() * 100;
                particle.style.left = randomX + '%';
                particle.style.top = randomY + '%';
            }, 10000 + index * 2000);
        });

        // Add mouse parallax effect to header
        document.addEventListener('mousemove', (e) => {
            const header = document.querySelector('.header-bg');
            const x = e.clientX / window.innerWidth;
            const y = e.clientY / window.innerHeight;
            
            header.style.transform = `translate(${x * 20}px, ${y * 20}px)`;
        });
    </script>
