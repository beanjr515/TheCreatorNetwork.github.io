
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Creator Network - Master Your Content Empire</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-red: #DC143C;
            --dark-red: #B71C1C;
            --black: #0D0D0D;
            --white: #FFFFFF;
            --gray: #333333;
            --light-gray: #F5F5F5;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, var(--black) 0%, var(--gray) 50%, var(--black) 100%);
            color: var(--white);
            overflow-x: hidden;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Animated Background Elements */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            overflow: hidden;
        }

        .floating-icon {
            position: absolute;
            font-size: 24px;
            color: var(--primary-red);
            opacity: 0.1;
            animation: floatAround 15s infinite linear;
        }

        @keyframes floatAround {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 0.1; }
            90% { opacity: 0.1; }
            100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(13, 13, 13, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 2px solid var(--primary-red);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo {
            font-size: 28px;
            font-weight: 900;
            color: var(--primary-red);
            text-shadow: 0 0 20px rgba(220, 20, 60, 0.5);
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 20px rgba(220, 20, 60, 0.5); }
            to { text-shadow: 0 0 30px rgba(220, 20, 60, 0.8), 0 0 40px rgba(220, 20, 60, 0.6); }
        }

        .discord-header-btn {
            background: linear-gradient(45deg, var(--primary-red), var(--dark-red));
            color: var(--white);
            padding: 12px 30px;
            border: none;
            border-radius: 25px;
            font-weight: 700;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(220, 20, 60, 0.4);
            animation: pulse 2s infinite;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .discord-header-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(220, 20, 60, 0.6);
            background: linear-gradient(45deg, var(--dark-red), var(--primary-red));
        }

        /* Hero Section */
        .hero {
            padding: 120px 0 60px;
            text-align: center;
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }

        .hero-content {
            width: 100%;
        }

        .hero h1 {
            font-size: 4.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--white), var(--primary-red), var(--white));
            background-size: 200% 200%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientText 3s ease-in-out infinite;
        }

        @keyframes gradientText {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 40px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.9;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .animated-text {
            display: inline-block;
            animation: bounce 2s infinite;
        }

        .animated-text:nth-child(1) { animation-delay: 0s; }
        .animated-text:nth-child(2) { animation-delay: 0.1s; }
        .animated-text:nth-child(3) { animation-delay: 0.2s; }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Content Creator Icons */
        .creator-icons {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 60px 0;
            flex-wrap: wrap;
        }

        .creator-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(45deg, var(--primary-red), var(--dark-red));
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 32px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(220, 20, 60, 0.3);
            animation: float 3s ease-in-out infinite;
        }

        .creator-icon:nth-child(even) {
            animation-delay: 1.5s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
        }

        .creator-icon:hover {
            transform: scale(1.2) rotate(10deg);
            box-shadow: 0 10px 30px rgba(220, 20, 60, 0.6);
        }

        /* Main CTA Button */
        .main-cta {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary-red), var(--dark-red));
            color: var(--white);
            padding: 20px 50px;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.3rem;
            font-weight: 700;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(220, 20, 60, 0.4);
            position: relative;
            overflow: hidden;
            animation: fadeInUp 1s ease-out 1s both;
        }

        .main-cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .main-cta:hover::before {
            left: 100%;
        }

        .main-cta:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(220, 20, 60, 0.6);
        }

        /* Features Section */
        .features {
            padding: 100px 0;
            background: rgba(255, 255, 255, 0.05);
        }

        .features h2 {
            text-align: center;
            font-size: 3.5rem;
            margin-bottom: 60px;
            font-weight: 800;
            color: var(--primary-red);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }

        .feature-card {
            background: linear-gradient(145deg, rgba(220, 20, 60, 0.1), rgba(13, 13, 13, 0.8));
            border: 2px solid var(--primary-red);
            border-radius: 20px;
            padding: 40px;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(220, 20, 60, 0.1), transparent);
            transform: rotate(45deg);
            transition: all 0.5s ease;
            opacity: 0;
        }

        .feature-card:hover::before {
            animation: shimmer 1s ease-in-out;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); opacity: 0; }
        }

        .feature-card:hover {
            transform: translateY(-10px);
            border-color: var(--white);
            box-shadow: 0 20px 40px rgba(220, 20, 60, 0.3);
        }

        .feature-card h3 {
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: var(--primary-red);
            font-weight: 700;
        }

        /* Stats Section */
        .stats {
            padding: 80px 0;
            text-align: center;
            background: var(--black);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
        }

        .stat-item {
            padding: 30px;
            border: 2px solid var(--primary-red);
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .stat-item:hover {
            background: rgba(220, 20, 60, 0.1);
            transform: scale(1.05);
        }

        .stat-number {
            font-size: 3.5rem;
            font-weight: 900;
            color: var(--primary-red);
            display: block;
            text-shadow: 0 0 10px rgba(220, 20, 60, 0.5);
        }

        .stat-label {
            font-size: 1.2rem;
            margin-top: 10px;
            color: var(--white);
        }

        /* Special styling for Cost to Join */
        .cost-stat {
            border-color: var(--primary-red) !important;
            background: rgba(220, 20, 60, 0.08) !important;
        }

        .cost-stat .stat-number {
            color: #E8E8E8 !important;
            text-shadow: 0 0 5px rgba(220, 20, 60, 0.3);
        }

        .cost-stat .stat-label {
            color: var(--white) !important;
            font-weight: 500 !important;
        }

        /* Discord Section */
        .discord-section {
            padding: 100px 0;
            text-align: center;
            background: linear-gradient(135deg, rgba(220, 20, 60, 0.2), rgba(13, 13, 13, 0.9));
        }

        .discord-card {
            background: rgba(13, 13, 13, 0.9);
            border: 3px solid var(--primary-red);
            border-radius: 25px;
            padding: 60px;
            max-width: 700px;
            margin: 0 auto;
            box-shadow: 0 20px 50px rgba(220, 20, 60, 0.3);
        }

        .discord-card h2 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            color: var(--primary-red);
        }

        .word-animation {
            display: inline-block;
            animation: wordSlide 0.8s ease-out;
        }

        @keyframes wordSlide {
            from { transform: translateX(-20px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

        /* Footer */
        footer {
            padding: 40px 0;
            text-align: center;
            background: var(--black);
            border-top: 2px solid var(--primary-red);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.8rem; }
            .creator-icons { gap: 20px; }
            .creator-icon { width: 60px; height: 60px; font-size: 24px; }
            .features-grid { grid-template-columns: 1fr; }
            .stats-grid { grid-template-columns: repeat(2, 1fr); }
            .discord-card { padding: 40px 20px; }
        }
    </style>
</head>
<body>
    <div class="bg-animation" id="bgAnimation"></div>

    <header>
        <nav class="container">
            <div class="logo">The Creator Network</div>
            <a href="https://discord.gg/CsuBZryn" target="_blank" rel="noopener noreferrer" class="discord-header-btn">
                💬 Join Discord
            </a>
        </nav>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h1>
                        <span class="animated-text">Build</span>
                        <span class="animated-text">Your</span>
                        <span class="animated-text">Empire</span>
                    </h1>
                    <p class="word-animation">Transform your passion into profit. Join thousands of creators mastering the art of viral content, massive audiences, and unstoppable growth.</p>
                    
                    <div class="creator-icons">
                        <div class="creator-icon" title="YouTube">📹</div>
                        <div class="creator-icon" title="TikTok">🎵</div>
                        <div class="creator-icon" title="Instagram">📸</div>
                        <div class="creator-icon" title="Twitch">🎮</div>
                        <div class="creator-icon" title="Twitter">🐦</div>
                        <div class="creator-icon" title="Podcast">🎙️</div>
                    </div>

                    <a href="https://discord.gg/CsuBZryn" target="_blank" rel="noopener noreferrer" class="main-cta">
                        🚀 Join The Network
                    </a>
                </div>
            </div>
        </section>

        <section class="stats">
            <div class="container">
                <div class="stats-grid">
                    <div class="stat-item">
                        <span class="stat-number" data-target="24">0</span>
                        <div class="stat-label">Hours Daily Support</div>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number" data-target="7">0</span>
                        <div class="stat-label">Days a Week Active</div>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number" data-target="100">0</span>
                        <div class="stat-label">% Fresh Content</div>
                    </div>
                    <div class="stat-item cost-stat">
                        <span class="stat-number" data-target="0">FREE</span>
                        <div class="stat-label">💰 Cost to Join 💰</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="features">
            <div class="container">
                <h2>Master Every Platform</h2>
                <div class="features-grid">
                    <div class="feature-card">
                        <h3>🔥 Viral Content Secrets</h3>
                        <p>Learn the psychology behind viral content. Get proven templates, hooks, and strategies that guarantee engagement across all platforms.</p>
                    </div>
                    <div class="feature-card">
                        <h3>📊 Algorithm Mastery</h3>
                        <p>Crack the code of YouTube, TikTok, and Instagram algorithms. Get your content seen by millions with insider optimization techniques.</p>
                    </div>
                    <div class="feature-card">
                        <h3>💰 Monetization Blueprint</h3>
                        <p>Turn followers into dollars. Master sponsorships, affiliate marketing, product launches, and building multiple revenue streams.</p>
                    </div>
                    <div class="feature-card">
                        <h3>🎯 Personal Branding</h3>
                        <p>Build an unshakeable personal brand that attracts opportunities, collaborations, and devoted fans who buy everything you create.</p>
                    </div>
                    <div class="feature-card">
                        <h3>🤝 Elite Networking</h3>
                        <p>Connect with top creators, industry insiders, and potential collaborators. Access exclusive partnerships and growth opportunities.</p>
                    </div>
                    <div class="feature-card">
                        <h3>⚡ Live Mentorship</h3>
                        <p>Get real-time feedback from creators who've built million-follower audiences and generated six-figure incomes from content.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="discord-section">
            <div class="container">
                <div class="discord-card">
                    <h2>
                        <span class="word-animation" style="animation-delay: 0s;">Ready</span>
                        <span class="word-animation" style="animation-delay: 0.2s;">To</span>
                        <span class="word-animation" style="animation-delay: 0.4s;">Dominate?</span>
                    </h2>
                    <p>Stop dreaming. Start building. Join the most ambitious creator community where viral content, massive growth, and life-changing income become your reality.</p>
                    <br><br>
                    <a href="https://discord.gg/CsuBZryn" target="_blank" rel="noopener noreferrer" class="main-cta">
                        💬 Join The Discord Community Now
                    </a>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 The Creator Network. Where legends are made.</p>
        </div>
    </footer>

    <script>
        // Create floating content creator icons
        function createFloatingIcons() {
            const container = document.getElementById('bgAnimation');
            const icons = ['📹', '📸', '🎵', '🎮', '🎙️', '💡', '🚀', '⚡', '🔥', '💎'];
            
            for (let i = 0; i < 15; i++) {
                const icon = document.createElement('div');
                icon.className = 'floating-icon';
                icon.textContent = icons[Math.floor(Math.random() * icons.length)];
                icon.style.left = Math.random() * 100 + '%';
                icon.style.animationDelay = Math.random() * 15 + 's';
                icon.style.animationDuration = (10 + Math.random() * 10) + 's';
                container.appendChild(icon);
            }
        }

        // Animate counters - ONE TIME ONLY
        function animateCounters() {
            const counters = document.querySelectorAll('.stat-number');
            const observerOptions = { threshold: 0.7 };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting && !entry.target.hasAttribute('data-animated')) {
                        const counter = entry.target;
                        const target = parseInt(counter.getAttribute('data-target'));
                        
                        // Mark as animated to prevent re-animation
                        counter.setAttribute('data-animated', 'true');
                        
                        if (target === 0) {
                            // Special handling for FREE - just show FREE with special styling
                            counter.textContent = 'FREE';
                        } else {
                            const increment = target / 40;
                            let current = 0;

                            const updateCounter = () => {
                                if (current < target) {
                                    current += increment;
                                    counter.textContent = Math.ceil(current);
                                    setTimeout(updateCounter, 50);
                                } else {
                                    counter.textContent = target;
                                }
                            };

                            updateCounter();
                        }
                        observer.unobserve(counter);
                    }
                });
            }, observerOptions);

            counters.forEach(counter => observer.observe(counter));
        }

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(13, 13, 13, 0.98)';
                header.style.borderBottom = '3px solid var(--primary-red)';
            } else {
                header.style.background = 'rgba(13, 13, 13, 0.95)';
                header.style.borderBottom = '2px solid var(--primary-red)';
            }
        });

        // Add word animation on scroll
        function animateWordsOnScroll() {
            const wordElements = document.querySelectorAll('.word-animation');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'wordSlide 0.8s ease-out';
                    }
                });
            });

            wordElements.forEach(el => observer.observe(el));
        }

        // Initialize everything
        document.addEventListener('DOMContentLoaded', () => {
            createFloatingIcons();
            animateCounters();
            animateWordsOnScroll();
        });

        // Enhanced click tracking for Discord links
        document.querySelectorAll('a[href*="discord.gg"]').forEach(link => {
            link.addEventListener('click', function(e) {
                console.log('Discord link clicked:', this.href);
                // Optional: Add analytics tracking here
            });
        });
    </script>
</body>
</html>
