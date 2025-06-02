<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PackageAI - Reduziere deine Versandkosten um 40% durch KI</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
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
            font-size: 1.5rem;
            font-weight: 700;
            color: #ffffff;
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
            font-weight: 500;
        }

        .nav-links a:hover {
            color: #cccccc;
        }

        .cta-button {
            background: #ffffff;
            color: #000000;
            padding: 12px 24px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            font-weight: 600;
        }

        .cta-button:hover {
            background: #f0f0f0;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: #000000;
            color: white;
            padding: 120px 0 80px;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
            line-height: 1.2;
        }

        .hero .subtitle {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            font-weight: 400;
        }

        .hero .description {
            font-size: 1.1rem;
            margin-bottom: 3rem;
            opacity: 0.7;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-cta {
            display: inline-flex;
            align-items: center;
            gap: 1rem;
        }

        .roi-badge {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Problem Section */
        .problem {
            background: #ffffff;
            color: #000000;
            padding: 80px 0;
        }

        .problem-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .problem-item {
            text-align: center;
            padding: 2rem;
        }

        .problem-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #ff4444;
        }

        .problem-cost {
            font-size: 2rem;
            font-weight: 700;
            color: #ff4444;
            margin-bottom: 1rem;
        }

        /* Solution Section */
        .solution {
            background: #000000;
            color: #ffffff;
            padding: 80px 0;
        }

        .solution-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }

        .solution-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 2.5rem;
            border-radius: 8px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .solution-card:hover {
            transform: translateY(-5px);
            border-color: rgba(255, 255, 255, 0.3);
            background: rgba(255, 255, 255, 0.08);
        }

        .solution-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: #00ff88;
        }

        .solution-savings {
            font-size: 1.5rem;
            font-weight: 700;
            color: #00ff88;
            margin-bottom: 1rem;
        }

        /* Benefits Section */
        .benefits {
            background: #ffffff;
            color: #000000;
            padding: 80px 0;
        }

        .benefits-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .benefit-item {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            padding: 1.5rem;
            background: rgba(0, 0, 0, 0.02);
            border-radius: 8px;
        }

        .benefit-check {
            color: #00aa44;
            font-size: 1.5rem;
            font-weight: 700;
        }

        .benefit-content h4 {
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        /* Proof Section */
        .proof {
            background: #000000;
            color: #ffffff;
            padding: 80px 0;
        }

        .proof-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
            text-align: center;
        }

        .stat-item {
            padding: 2rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            color: #00ff88;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            opacity: 0.8;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.9rem;
        }

        /* Integration Section */
        .integration {
            background: #ffffff;
            color: #000000;
            padding: 80px 0;
        }

        .platform-logos {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 3rem;
            margin-top: 3rem;
            flex-wrap: wrap;
        }

        .platform-logo {
            font-size: 1.5rem;
            font-weight: 700;
            opacity: 0.6;
            transition: opacity 0.3s ease;
        }

        .platform-logo:hover {
            opacity: 1;
        }

        /* CTA Section */
        .final-cta {
            background: #000000;
            color: #ffffff;
            padding: 100px 0;
            text-align: center;
        }

        .cta-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .cta-form {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            max-width: 400px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-input {
            flex: 1;
            padding: 15px;
            border: 2px solid rgba(255, 255, 255, 0.2);
            background: transparent;
            color: white;
            border-radius: 6px;
        }

        .cta-input::placeholder {
            color: rgba(255, 255, 255, 0.5);
        }

        .cta-submit {
            background: #ffffff;
            color: #000000;
            padding: 15px 30px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .cta-submit:hover {
            background: #f0f0f0;
            transform: translateY(-2px);
        }

        .guarantee {
            margin-top: 2rem;
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* Section Titles */
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .section-subtitle {
            text-align: center;
            font-size: 1.2rem;
            opacity: 0.8;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-cta {
                flex-direction: column;
                align-items: center;
            }
            
            .cta-form {
                flex-direction: column;
            }
            
            .platform-logos {
                gap: 1.5rem;
            }
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .animate-on-scroll.animate {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">PackageAI</div>
            <ul class="nav-links">
                <li><a href="#problem">Problem</a></li>
                <li><a href="#solution">Lösung</a></li>
                <li><a href="#proof">Erfolge</a></li>
                <li><a href="#demo">Demo</a></li>
            </ul>
            <a href="#demo" class="cta-button">Kostenlose Demo</a>
        </nav>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Reduziere deine Versandkosten um 40%</h1>
            <div class="subtitle">durch KI-optimierte Verpackung</div>
            <div class="description">
                Für Shopify, WooCommerce & Magento Stores. Automatische Integration in 5 Minuten. 
                Sofortige Kosteneinsparung ab der ersten Bestellung.
            </div>
            <div class="hero-cta">
                <a href="#demo" class="cta-button" style="padding: 18px 36px; font-size: 1.1rem;">
                    Jetzt 30 Tage kostenlos testen
                </a>
                <div class="roi-badge">⚡ ROI in ersten 30 Tagen</div>
            </div>
        </div>
    </section>

    <section id="problem" class="problem">
        <div class="container">
            <h2 class="section-title">Diese Probleme kosten dich täglich Geld</h2>
            <div class="problem-grid">
                <div class="problem-item animate-on-scroll">
                    <div class="problem-icon">📦</div>
                    <div class="problem-cost">€2.50</div>
                    <h3>Überverpackung pro Bestellung</h3>
                    <p>Zu große Kartons, überflüssiges Füllmaterial und ineffiziente Verpackungsauswahl verschwenden täglich Geld</p>
                </div>
                <div class="problem-item animate-on-scroll">
                    <div class="problem-icon">⏱️</div>
                    <div class="problem-cost">15 Min</div>
                    <h3>Manuelle Verpackungszeit</h3>
                    <p>Mitarbeiter verbringen wertvolle Zeit mit der Auswahl der richtigen Verpackung statt mit produktiven Aufgaben</p>
                </div>
                <div class="problem-item animate-on-scroll">
                    <div class="problem-icon">📈</div>
                    <div class="problem-cost">25%</div>
                    <h3>Höhere Versandkosten</h3>
                    <p>Falsche Kartongrößen führen zu überhöhten DHL, UPS und DPD Versandkosten bei jeder Sendung</p>
                </div>
                <div class="problem-item animate-on-scroll">
                    <div class="problem-icon">😞</div>
                    <div class="problem-cost">12%</div>
                    <h3>Unzufriedene Kunden</h3>
                    <p>Beschädigte Ware durch schlechte Verpackung führt zu Retouren, Beschwerden und negativen Bewertungen</p>
                </div>
            </div>
        </div>
    </section>

    <section id="solution" class="solution">
        <div class="container">
            <h2 class="section-title">PackageAI löst das automatisch</h2>
            <div class="section-subtitle">Unsere KI analysiert jedes Produkt und wählt die perfekte Verpackung</div>
            <div class="solution-grid">
                <div class="solution-card animate-on-scroll">
                    <div class="solution-icon">🤖</div>
                    <div class="solution-savings">-40% Verpackungskosten</div>
                    <h3>Intelligente Größenoptimierung</h3>
                    <p>KI berechnet exakt die minimale Kartongröße für optimalen Schutz und niedrigste Versandkosten</p>
                </div>
                <div class="solution-card animate-on-scroll">
                    <div class="solution-icon">⚡</div>
                    <div class="solution-savings">-80% Packzeit</div>
                    <h3>Automatische Empfehlungen</h3>
                    <p>Sofortige Karton- und Materialempfehlung direkt in deinem Shop-Backend ohne manuelle Eingaben</p>
                </div>
                <div class="solution-card animate-on-scroll">
                    <div class="solution-icon">🌍</div>
                    <div class="solution-savings">-50% CO2 Ausstoß</div>
                    <h3>Nachhaltige Verpackung</h3>
                    <p>Reduziere Verpackungsmüll und verbessere deine Umweltbilanz durch präzise Materialauswahl</p>
                </div>
                <div class="solution-card animate-on-scroll">
                    <div class="solution-icon">📱</div>
                    <div class="solution-savings">5 Min Setup</div>
                    <h3>Plug & Play Integration</h3>
                    <p>Einfache Installation via API für Shopify, WooCommerce, Magento - ohne technische Kenntnisse</p>
                </div>
            </div>
        </div>
    </section>

    <section class="benefits">
        <div class="container">
            <h2 class="section-title">Was unsere E-Commerce Kunden sagen</h2>
            <div class="benefits-list">
                <div class="benefit-item animate-on-scroll">
                    <div class="benefit-check">✓</div>
                    <div class="benefit-content">
                        <h4>"€3.200 weniger Versandkosten pro Monat"</h4>
                        <p>Fashion Store mit 800 Bestellungen/Monat - Sarah M., Geschäftsführerin</p>
                    </div>
                </div>
                <div class="benefit-item animate-on-scroll">
                    <div class="benefit-check">✓</div>
                    <div class="benefit-content">
                        <h4>"Packzeit von 10 auf 2 Minuten reduziert"</h4>
                        <p>Electronics Store - Michael K., Logistics Manager</p>
                    </div>
                </div>
                <div class="benefit-item animate-on-scroll">
                    <div class="benefit-check">✓</div>
                    <div class="benefit-content">
                        <h4>"ROI von 450% im ersten Quartal"</h4>
                        <p>Home & Garden Shop - Lisa R., E-Commerce Managerin</p>
                    </div>
                </div>
                <div class="benefit-item animate-on-scroll">
                    <div class="benefit-check">✓</div>
                    <div class="benefit-content">
                        <h4>"Retouren um 60% gesunken"</h4>
                        <p>Beauty & Cosmetics - Thomas W., Operations Director</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="proof" class="proof">
        <div class="container">
            <h2 class="section-title">Bewiesene Resultate</h2>
            <div class="section-subtitle">Echte Zahlen von über 500+ E-Commerce Stores</div>
            <div class="proof-stats">
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">€2.8M</div>
                    <div class="stat-label">Eingesparte Kosten</div>
                </div>
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">45%</div>
                    <div class="stat-label">Ø Kosteneinsparung</div>
                </div>
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">2.1M</div>
                    <div class="stat-label">Optimierte Pakete</div>
                </div>
                <div class="stat-item animate-on-scroll">
                    <div class="stat-number">500+</div>
                    <div class="stat-label">Aktive Stores</div>
                </div>
            </div>
        </div>
    </section>

    <section class="integration">
        <div class="container">
            <h2 class="section-title">Nahtlose Integration</h2>
            <div class="section-subtitle">Funktioniert mit allen führenden E-Commerce Plattformen</div>
            <div class="platform-logos">
                <div class="platform-logo">SHOPIFY</div>
                <div class="platform-logo">WOOCOMMERCE</div>
                <div class="platform-logo">MAGENTO</div>
                <div class="platform-logo">PRESTASHOP</div>
                <div class="platform-logo">SHOPWARE</div>
                <div class="platform-logo">BIGCOMMERCE</div>
            </div>
        </div>
    </section>

    <section id="demo" class="final-cta">
        <div class="container">
            <div class="cta-content">
                <h2 class="section-title">Starte deine 30-Tage-Testphase</h2>
                <p style="font-size: 1.2rem; margin-bottom: 2rem;">
                    Keine Kreditkarte erforderlich. Setup in 5 Minuten. 
                    Sofortige Kosteneinsparung ab der ersten Bestellung.
                </p>
                <form class="cta-form">
                    <input type="email" class="cta-input" placeholder="Deine E-Mail-Adresse" required>
                    <button type="submit" class="cta-submit">Demo starten</button>
                </form>
                <div class="guarantee">
                    🔒 30 Tage Geld-zurück-Garantie • ⚡ Sofortiger Zugang • 📞 Persönlicher Support
                </div>
            </div>
        </div>
    </section>

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
        document.querySelector('.cta-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const email = this.querySelector('input[type="email"]').value;
            if (email) {
                alert(`Danke! Wir senden dir sofort den Demo-Zugang an ${email}`);
                this.reset();
            }
        });

        // Header background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.background = 'rgba(0, 0, 0, 0.98)';
            } else {
                header.style.background = 'rgba(0, 0, 0, 0.95)';
            }
        });

        // Add dynamic numbers animation when in view
        const animateNumbers = () => {
            const numbers = document.querySelectorAll('.stat-number');
            numbers.forEach(num => {
                const finalValue = num.textContent;
                const numValue = parseFloat(finalValue.replace(/[^0-9.]/g, ''));
                let currentValue = 0;
                const increment = numValue / 50;
                const timer = setInterval(() => {
                    currentValue += increment;
                    if (currentValue >= numValue) {
                        num.textContent = finalValue;
                        clearInterval(timer);
                    } else {
                        num.textContent = Math.floor(currentValue) + finalValue.replace(/[0-9]/g, '').replace('.', '');
                    }
                }, 30);
            });
        };

        // Trigger number animation when proof section is visible
        const proofSection = document.querySelector('.proof');
        const proofObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    setTimeout(animateNumbers, 500);
                    proofObserver.unobserve(entry.target);
                }
            });
        });

        if (proofSection) {
            proofObserver.observe(proofSection);
        }
    </script>
</body>
</html>
