# ai-solutions
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PackageAI - Intelligente Verpackungslösungen für E-Commerce</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #ffffff;
            background: #000000;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: rgba(0, 0, 0, 0.95);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: #cccccc;
            transform: translateY(-2px);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: white;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .cta-button {
            background: #ffffff;
            color: #000000;
            padding: 12px 24px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cta-button:hover {
            background: #cccccc;
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(255, 255, 255, 0.2);
        }

        /* Hero Section */
        .hero {
            background: #000000;
            color: white;
            padding: 150px 0 100px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 30% 40%, rgba(255, 255, 255, 0.05) 0%, transparent 50%),
                        radial-gradient(circle at 80% 10%, rgba(255, 255, 255, 0.03) 0%, transparent 50%),
                        radial-gradient(circle at 40% 80%, rgba(255, 255, 255, 0.04) 0%, transparent 50%);
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1.5rem;
            font-weight: 100;
            letter-spacing: 3px;
            text-transform: uppercase;
            animation: slideInUp 1s ease;
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 3rem;
            opacity: 0.8;
            font-weight: 300;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            animation: slideInUp 1s ease 0.2s both;
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Features Section */
        .features {
            padding: 100px 0;
            background: #ffffff;
            color: #000000;
        }

        .section-title {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 4rem;
            font-weight: 100;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 2px;
            background: #000000;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            margin-top: 5rem;
        }

        .feature-card {
            background: #000000;
            color: #ffffff;
            padding: 3rem;
            border-radius: 0;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: #ffffff;
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .feature-card:hover::before {
            transform: scaleX(1);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 255, 255, 0.3);
        }

        .feature-icon {
            width: 80px;
            height: 80px;
            border: 2px solid #ffffff;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 2rem;
            font-size: 2rem;
            color: white;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 300;
        }

        .feature-card p {
            opacity: 0.8;
            line-height: 1.8;
            font-weight: 300;
        }

        /* Stats Section */
        .stats {
            background: #000000;
            color: white;
            padding: 80px 0;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
            text-align: center;
        }

        .stat-item h3 {
            font-size: 4rem;
            margin-bottom: 1rem;
            font-weight: 100;
            color: #ffffff;
        }

        .stat-item p {
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 300;
            opacity: 0.8;
        }

        /* How it Works */
        .how-it-works {
            padding: 100px 0;
            background: #ffffff;
            color: #000000;
        }

        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 4rem;
            margin-top: 5rem;
        }

        .step {
            text-align: center;
            position: relative;
        }

        .step-number {
            width: 100px;
            height: 100px;
            border: 3px solid #000000;
            color: #000000;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            font-weight: 100;
            margin: 0 auto 2rem;
            transition: all 0.3s ease;
        }

        .step:hover .step-number {
            background: #000000;
            color: #ffffff;
        }

        .step h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 300;
        }

        .step p {
            opacity: 0.7;
            line-height: 1.8;
            font-weight: 300;
        }

        /* About Section */
        .about {
            padding: 100px 0;
            background: #000000;
            color: #ffffff;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .about h2 {
            font-size: 3rem;
            margin-bottom: 3rem;
            font-weight: 100;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .about p {
            font-size: 1.2rem;
            line-height: 2;
            opacity: 0.8;
            font-weight: 300;
            margin-bottom: 2rem;
        }

        /* Contact */
        .contact {
            background: #ffffff;
            color: #000000;
            padding: 100px 0;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 20px;
            border: 2px solid #000000;
            border-radius: 0;
            background: transparent;
            color: #000000;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #666666;
            background: rgba(0, 0, 0, 0.05);
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(0, 0, 0, 0.5);
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 300;
        }

        /* Footer */
        footer {
            background: #000000;
            color: white;
            padding: 60px 0 30px;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        footer p {
            opacity: 0.7;
            font-weight: 300;
            letter-spacing: 1px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .features-grid,
            .steps {
                grid-template-columns: 1fr;
            }
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(50px);
            transition: all 1s ease;
        }

        .animate-on-scroll.animate {
            opacity: 1;
            transform: translateY(0);
        }

        /* Mobile Menu */
        .mobile-menu {
            display: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        @media (max-width: 768px) {
            .mobile-menu {
                display: block;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">PackageAI</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#about">Über uns</a></li>
                <li><a href="#contact">Kontakt</a></li>
            </ul>
            <div class="mobile-menu">☰</div>
            <a href="#contact" class="cta-button">Demo anfordern</a>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Intelligente Verpackung</h1>
                <p>Revolutionieren Sie Ihre Verpackungsprozesse mit KI-gestützter Optimierung. Reduzieren Sie Kosten, verbessern Sie die Nachhaltigkeit und steigern Sie die Kundenzufriedenheit durch präzise Algorithmen.</p>
                <a href="#contact" class="cta-button">Jetzt starten</a>
            </div>
        </div>
    </section>

    <section id="features" class="features">
        <div class="container">
            <h2 class="section-title animate-on-scroll">Warum PackageAI?</h2>
            <div class="features-grid">
                <div class="feature-card animate-on-scroll">
                    <div class="feature-icon">AI</div>
                    <h3>KI-Optimierung</h3>
                    <p>Unsere fortschrittliche künstliche Intelligenz analysiert Ihre Produkte in Echtzeit und bestimmt die optimale Verpackungsgröße und -art für jede einzelne Bestellung.</p>
                </div>
                <div class="feature-card animate-on-scroll">
                    <div class="feature-icon">€</div>
                    <h3>Kosteneinsparung</h3>
                    <p>Reduzieren Sie Verpackungskosten signifikant durch intelligente Materialauswahl, optimierte Größenbestimmung und Minimierung von Verschwendung.</p>
                </div>
                <div class="feature-card animate-on-scroll">
                    <div class="feature-icon">♻</div>
                    <h3>Nachhaltigkeit</h3>
                    <p>Minimieren Sie Ihren ökologischen Fußabdruck durch optimierte Verpackungsgrößen, umweltfreundliche Materialauswahl und Reduktion von Überverpackung.</p>
                </div>
                <div class="feature-card animate-on-scroll">
                    <div class="feature-icon">⚡</div>
                    <h3>Automatisierung</h3>
                    <p>Vollautomatische Integration in Ihre bestehenden E-Commerce-Systeme und Fulfillment-Prozesse ohne manuelle Eingriffe oder Unterbrechungen.</p>
                </div>
                <div class="feature-card animate-on-scroll">
                    <div class="feature-icon">📊</div>
                    <h3>Analytics</h3>
                    <p>Detaillierte Berichte und tiefgreifende Einblicke in Ihre Verpackungseffizienz, Kostenstrukturen und kontinuierliche Optimierungspotentiale.</p>
                </div>
                <div class="feature-card animate-on-scroll">
                    <div class="feature-icon">🔗</div>
                    <h3>Integration</h3>
                    <p>Nahtlose Anbindung über REST-API an Shopify, WooCommerce, Magento und andere führende E-Commerce-Plattformen innerhalb weniger Minuten.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item animate-on-scroll">
                    <h3>35%</h3>
                    <p>Kosteneinsparung</p>
                </div>
                <div class="stat-item animate-on-scroll">
                    <h3>50%</h3>
                    <p>Weniger Material</p>
                </div>
                <div class="stat-item animate-on-scroll">
                    <h3>99.9%</h3>
                    <p>Verfügbarkeit</p>
                </div>
                <div class="stat-item animate-on-scroll">
                    <h3>24/7</h3>
                    <p>Support</p>
                </div>
            </div>
        </div>
    </section>

    <section id="how-it-works" class="how-it-works">
        <div class="container">
            <h2 class="section-title animate-on-scroll">So funktioniert's</h2>
            <div class="steps">
                <div class="step animate-on-scroll">
                    <div class="step-number">1</div>
                    <h3>Produktanalyse</h3>
                    <p>Unsere KI analysiert präzise Größe, Gewicht, Zerbrechlichkeit und weitere relevante Eigenschaften Ihrer Produkte für optimale Verpackungsempfehlungen.</p>
                </div>
                <div class="step animate-on-scroll">
                    <div class="step-number">2</div>
                    <h3>Intelligente Optimierung</h3>
                    <p>Fortschrittliche Algorithmen bestimmen die ideale Verpackungsgröße, das beste Material und die kosteneffizienteste Lösung für jeden Auftrag.</p>
                </div>
                <div class="step animate-on-scroll">
                    <div class="step-number">3</div>
                    <h3>Automatische Umsetzung</h3>
                    <p>Nahtlose Integration in Ihr Fulfillment-System ermöglicht automatische Verpackungsauswahl und -prozesse ohne manuelle Intervention.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <div class="about-content animate-on-scroll">
                <h2>Über PackageAI</h2>
                <p>Wir sind ein innovatives Technologieunternehmen, das sich auf die Entwicklung intelligenter Verpackungslösungen für den E-Commerce spezialisiert hat.</p>
                <p>Unsere Mission ist es, durch den Einsatz modernster KI-Technologien die Effizienz, Nachhaltigkeit und Kostenwirksamkeit von Verpackungsprozessen zu revolutionieren.</p>
                <p>Mit jahrelanger Erfahrung in der Entwicklung von Machine Learning-Algorithmen und Deep Learning-Modellen schaffen wir maßgeschneiderte Lösungen für Unternehmen jeder Größe.</p>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title animate-on-scroll">Kontakt</h2>
            <form class="contact-form">
                <div class="form-group">
                    <input type="text" placeholder="Ihr Name" required>
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Ihre E-Mail-Adresse" required>
                </div>
                <div class="form-group">
                    <input type="text" placeholder="Unternehmen">
                </div>
                <div class="form-group">
                    <input type="tel" placeholder="Telefonnummer">
                </div>
                <div class="form-group">
                    <textarea rows="6" placeholder="Ihre Nachricht oder Anfrage"></textarea>
                </div>
                <button type="submit" class="cta-button" style="width: 100%; padding: 20px;">Nachricht senden</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 PackageAI. Alle Rechte vorbehalten.</p>
            <p style="margin-top: 1rem;">Revolutionieren Sie Ihre Verpackungsprozesse mit künstlicher Intelligenz.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
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

        // Animate elements on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.animate-on-scroll').forEach(el => {
            observer.observe(el);
        });

        // Form submission
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Vielen Dank für Ihre Nachricht! Wir melden uns bald bei Ihnen.');
            this.reset();
        });

        // Header background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(0, 0, 0, 0.98)';
                header.style.borderBottom = '1px solid rgba(255, 255, 255, 0.2)';
            } else {
                header.style.background = 'rgba(0, 0, 0, 0.95)';
                header.style.borderBottom = '1px solid rgba(255, 255, 255, 0.1)';
            }
        });

        // Mobile menu toggle (basic implementation)
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const navLinks = document.querySelector('.nav-links');
            if (navLinks.style.display === 'flex') {
                navLinks.style.display = 'none';
            } else {
                navLinks.style.display = 'flex';
                navLinks.style.flexDirection = 'column';
                navLinks.style.position = 'absolute';
                navLinks.style.top = '100%';
                navLinks.style.left = '0';
                navLinks.style.right = '0';
                navLinks.style.background = 'rgba(0, 0, 0, 0.98)';
                navLinks.style.padding = '2rem';
            }
        });
    </script>
</body>
</html>
