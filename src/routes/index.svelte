<title>Fly View Visa | m.flyviewvisa.app</title>
    <!-- Font Awesome for Icons -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        /* --- 1. CORE STYLING & COLORS --- */
        :root {
            --bg-black: #000000;
            --card-black: #0f0f0f;
            --maroon-primary: #800000;
            --maroon-bright: #b30000;
            --whatsapp-green: #25D366;
            --wechat-green: #07C160;
            --instagram-pink: #E1306C;
            --text-white: #ffffff;
            --text-gray: #b0b0b0;
            --border-color: #222222;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            -webkit-tap-highlight-color: transparent;
        }

        html { scroll-behavior: smooth; }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--bg-black);
            color: var(--text-white);
            line-height: 1.5;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- 2. NAVIGATION & MENU --- */
        nav {
            background-color: rgba(0, 0, 0, 0.95);
            border-bottom: 1px solid var(--border-color);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* Minimal Logo Only Style */
        .logo-only {
            color: var(--maroon-primary);
            font-size: 1.8rem;
            text-decoration: none;
            display: flex;
            align-items: center;
        }

        .nav-right {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .lang-select-nav {
            background: #1a1a1a;
            color: white;
            border: 1px solid var(--border-color);
            padding: 5px 8px;
            border-radius: 4px;
            font-size: 0.75rem;
            outline: none;
            cursor: pointer;
            text-transform: uppercase;
        }

        .menu-btn {
            background: none;
            border: none;
            color: white;
            font-size: 1.6rem;
            cursor: pointer;
            padding: 4px;
            display: flex;
            align-items: center;
        }

        /* Mobile Slide-out Menu */
        .mobile-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.98);
            z-index: 2000;
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .mobile-overlay.active { display: flex; }

        .close-menu {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 2.5rem;
            color: white;
            cursor: pointer;
        }

        .overlay-links { display: flex; flex-direction: column; text-align: center; }

        .overlay-links a {
            color: white;
            text-decoration: none;
            font-size: 1.5rem;
            margin: 10px 0;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .overlay-links .lang-switcher-mobile {
            margin-top: 20px;
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
            padding: 0 20px;
        }

        .lang-btn {
            background: #1a1a1a;
            border: 1px solid var(--border-color);
            color: white;
            padding: 8px 12px;
            border-radius: 5px;
            font-size: 0.8rem;
            min-width: 60px;
        }

        .lang-btn.active {
            border-color: var(--maroon-primary);
            background: var(--maroon-primary);
        }

        /* --- 3. HERO SECTION --- */
        .hero {
            padding: 80px 0 50px;
            text-align: center;
            background: radial-gradient(circle at center, #3a0000 0%, #000000 85%);
        }

        .hero h1 {
            font-size: 2.5rem;
            line-height: 1.1;
            margin-bottom: 15px;
            font-weight: 900;
            text-transform: uppercase;
        }

        .hero h1 span { color: var(--maroon-primary); }

        .hero p {
            font-size: 1rem;
            color: var(--text-gray);
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* --- 4. BUTTONS & CTA --- */
        .cta-button {
            background-color: var(--maroon-primary);
            color: white;
            padding: 16px 32px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            display: inline-flex;
            align-items: center;
            font-size: 1rem;
            transition: 0.3s;
            border: none;
        }

        .cta-button:active { transform: scale(0.95); }
        .cta-button i { margin-right: 12px; font-size: 1.2rem; }

        .whatsapp-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background-color: var(--whatsapp-green);
            color: white;
            width: 50px; 
            height: 50px; 
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px; 
            box-shadow: 0 4px 15px rgba(0,0,0,0.6);
            z-index: 1001;
            text-decoration: none;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        /* --- 5. PROCESS SECTION --- */
        .section-header {
            text-align: center;
            margin-bottom: 40px;
            padding-top: 60px;
        }

        .section-header h2 {
            font-size: 1.6rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .section-header .line {
            width: 60px;
            height: 4px;
            background: var(--maroon-primary);
            margin: 15px auto;
        }

        .process-list {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .process-step {
            background-color: var(--card-black);
            padding: 25px;
            border-left: 5px solid var(--maroon-primary);
            border-radius: 4px;
        }

        .step-num { color: var(--maroon-primary); font-weight: bold; margin-bottom: 5px; display: block; }
        .process-step h3 { margin-bottom: 10px; font-size: 1.2rem; }
        .process-step p { color: var(--text-gray); font-size: 0.9rem; }

        /* --- 6. COUNTRIES GRID --- */
        .country-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin-bottom: 60px;
        }

        .country-card {
            background-color: var(--card-black);
            border: 1px solid var(--border-color);
            padding: 20px 10px;
            border-radius: 8px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            text-decoration: none;
            color: white;
            transition: 0.3s;
        }

        .country-card:active { background: var(--maroon-primary); }
        .country-card i { color: var(--maroon-primary); margin-bottom: 10px; font-size: 1.2rem; }
        .country-card span { font-size: 0.8rem; font-weight: 600; text-transform: uppercase; }

        /* --- 7. FOOTER --- */
        footer {
            background-color: #050505;
            padding: 60px 0 30px;
            border-top: 1px solid var(--border-color);
            text-align: center;
        }

        .footer-logo { font-size: 1.8rem; margin-bottom: 10px; display: flex; align-items: center; justify-content: center; font-weight: 900; text-transform: uppercase; }
        .footer-logo span { color: var(--maroon-primary); margin-left: 4px; }
        .footer-logo i { margin-right: 8px; color: var(--maroon-primary); }

        .social-row {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 30px 0;
        }

        .social-link {
            font-size: 2rem;
            color: white;
            text-decoration: none;
        }

        .social-link.insta { color: var(--instagram-pink); }
        .social-link.wa { color: var(--whatsapp-green); }
        .social-link.wc { color: var(--wechat-green); }

        .contact-info { color: var(--text-gray); font-size: 0.9rem; margin-bottom: 30px; }
        .contact-info p { margin: 10px 0; }

        .copyright {
            font-size: 0.8rem;
            color: #444;
            border-top: 1px solid var(--border-color);
            padding-top: 30px;
        }

        /* --- 8. DESKTOP OPTIMIZATION --- */
        @media (min-width: 768px) {
            .hero h1 { font-size: 3.5rem; }
            .process-list { flex-direction: row; flex-wrap: wrap; }
            .process-step { flex: 1 1 calc(50% - 20px); }
            .country-grid { grid-template-columns: repeat(5, 1fr); }
        }
    </style>
</head>
<body>

    <!-- Floating WhatsApp Action -->
    <a href="https://wa.me/60109654305?text=Hello%20Fly%20View%20Visa%21%20I%20want%20to%20apply%20for%20a%20visa." class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Navigation -->
    <nav>
        <div class="container nav-content">
            <!-- Logo Only (Minimalist) -->
            <a href="#" class="logo-only" aria-label="Fly View Visa Home">
                <i class="fas fa-paper-plane"></i>FVV
            </a>

            <!-- Right Controls -->
            <div class="nav-right">
                <select class="lang-select-nav" onchange="changeLanguage(this.value)" id="langSelectNav">
                    <option value="en">EN</option>
                    <option value="vi">VN</option>
                    <option value="zh">ZH</option>
                    <option value="bn">BN</option>
                </select>
                <button class="menu-btn" onclick="toggleMenu()" aria-label="Menu">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- Mobile Navigation Overlay -->
    <div id="mobileMenu" class="mobile-overlay">
        <div class="close-menu" onclick="toggleMenu()">&times;</div>
        <div class="overlay-links">
            <a href="#" onclick="toggleMenu()" id="m-home">Home</a>
            <a href="#destinations" onclick="toggleMenu()" id="m-dest">Destinations</a>
            <a href="#process" onclick="toggleMenu()" id="m-process">How to Apply</a>
            <a href="https://wa.me/60109654305" target="_blank" id="m-chat">WhatsApp Chat</a>
            
            <div class="lang-switcher-mobile">
                <button class="lang-btn" id="btn-en" onclick="changeLanguage('en')">EN</button>
                <button class="lang-btn" id="btn-vi" onclick="changeLanguage('vi')">VN</button>
                <button class="lang-btn" id="btn-zh" onclick="changeLanguage('zh')">ZH</button>
                <button class="lang-btn" id="btn-bn" onclick="changeLanguage('bn')">BN</button>
            </div>
        </div>
    </div>

    <!-- Hero -->
    <header class="hero">
        <div class="container">
            <h1 id="hero-title">Fly View <span>Visa</span></h1>
            <p id="hero-desc">Premium Visa Consultation for 40+ countries. Fast, reliable, and directly accessible via WhatsApp or WeChat.</p>
            <a href="https://wa.me/60109654305?text=I%20want%20to%20book%20a%20visa%20consultation." class="cta-button" id="hero-cta">
                <i class="fab fa-whatsapp"></i> Book Appointment
            </a>
            <div style="margin-top: 15px; font-size: 0.8rem; color: var(--maroon-primary); font-weight: bold;">
                m.flyviewvisa.app
            </div>
        </div>
    </header>

    <!-- Process Section -->
    <section id="process" class="container">
        <div class="section-header">
            <h2 id="process-header">Application Process</h2>
            <div class="line"></div>
        </div>

        <div class="process-list">
            <div class="process-step">
                <span class="step-num">01</span>
                <h3 id="step1-title">Direct Chat</h3>
                <p id="step1-desc">Connect with our experts instantly via WhatsApp or WeChat (ID: Turjo1992) to start your journey.</p>
            </div>
            <div class="process-step">
                <span class="step-num">02</span>
                <h3 id="step2-title">Profile Assessment</h3>
                <p id="step2-desc">Share your travel history and destination. We provide a tailored document checklist.</p>
            </div>
            <div class="process-step">
                <span class="step-num">03</span>
                <h3 id="step3-title">Submission</h3>
                <p id="step3-desc">Once documents are ready, we handle the formal submission to the respective embassy.</p>
            </div>
            <div class="process-step">
                <span class="step-num">04</span>
                <h3 id="step4-title">Approval</h3>
                <p id="step4-desc">We monitor your application daily and deliver the visa approval directly to you.</p>
            </div>
        </div>
    </section>

    <!-- Destination Grid -->
    <section id="destinations" class="container" style="padding: 60px 0;">
        <div class="section-header">
            <h2 id="dest-header">Select Destination</h2>
            <p style="color: var(--text-gray); margin-top: -10px;" id="dest-sub">Tap a country to apply via WhatsApp</p>
            <div class="line"></div>
        </div>

        <div class="country-grid">
            <script>
                const countries = [
                    "USA", "Canada", "UK", "Germany", "France", 
                    "Italy", "Spain", "Netherlands", "Switzerland", "Sweden",
                    "UAE", "Saudi Arabia", "Qatar", "Turkey", "Japan",
                    "South Korea", "China", "Singapore", "Thailand", "Malaysia",
                    "Australia", "New Zealand", "South Africa", "Egypt", "Russia",
                    "Brazil", "Argentina", "Mexico", "Portugal", "Greece",
                    "Poland", "Finland", "Belgium", "Norway", "Ireland",
                    "Indonesia", "Vietnam", "Philippines", "India", "Maldives"
                ];
                
                countries.forEach(name => {
                    document.write(`
                        <a href="https://wa.me/60109654305?text=I%20am%20interested%20in%20applying%20for%20a%20${name}%20visa." class="country-card">
                            <i class="fas fa-passport"></i>
                            <span>${name}</span>
                        </a>
                    `);
                });
            </script>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-logo">
                <i class="fas fa-paper-plane"></i> Fly View<span>Visa</span>
            </div>
            <div style="color: var(--maroon-primary); font-weight: bold; margin-bottom: 20px;">m.flyviewvisa.app</div>
            
            <div class="contact-info">
                <p><i class="fas fa-phone-alt" style="color: var(--maroon-primary);"></i> +60 10-965 4305</p>
                <p><i class="fab fa-weixin" style="color: var(--wechat-green);"></i> ID: Turjo1992</p>
                <p><i class="fas fa-envelope" style="color: var(--maroon-primary);"></i> info@flyviewvisa.app</p>
            </div>

            <div class="social-row">
                <a href="https://wa.me/60109654305" class="social-link wa" target="_blank" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                <a href="https://instagram.com/flyviewvisa" class="social-link insta" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-link wc" aria-label="WeChat"><i class="fab fa-weixin"></i></a>
            </div>

            <div class="copyright" id="copyright-text">
                &copy; 2025 Fly View Visa Services. All Rights Reserved.<br>
                Professional Visa Consultation & Processing.
            </div>
        </div>
    </footer>

    <script>
        const translations = {
            en: {
                home: "Home",
                destinations: "Destinations",
                apply: "How to Apply",
                chat: "WhatsApp Chat",
                heroTitle: "Fly View <span>Visa</span>",
                heroDesc: "Premium Visa Consultation for 40+ countries. Fast, reliable, and directly accessible via WhatsApp or WeChat.",
                heroCta: "Book Appointment",
                procHeader: "Application Process",
                step1T: "Direct Chat",
                step1D: "Connect with our experts instantly via WhatsApp or WeChat (ID: Turjo1992) to start your journey.",
                step2T: "Profile Assessment",
                step2D: "Share your travel history and destination. We provide a tailored document checklist.",
                step3T: "Submission",
                step3D: "Once documents are ready, we handle the formal submission to the respective embassy.",
                step4T: "Approval",
                step4D: "We monitor your application daily and deliver the visa approval directly to you.",
                destH: "Select Destination",
                destS: "Tap a country to apply via WhatsApp",
                copy: "&copy; 2025 Fly View Visa Services. All Rights Reserved.<br>Professional Visa Consultation & Processing."
            },
            vi: {
                home: "Trang chÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ§",
                destinations: "ÃÂÃÂÃÂÃÂiÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂm ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿n",
                apply: "CÃÂÃÂÃÂÃÂ¡ch ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂng kÃÂÃÂÃÂÃÂ½",
                chat: "Chat WhatsApp",
                heroTitle: "Fly View <span>Visa</span>",
                heroDesc: "TÃÂÃÂÃÂÃÂ° vÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¥n Visa cao cÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¥p cho hÃÂÃÂÃÂÃÂ¡n 40 quÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂc gia. Nhanh chÃÂÃÂÃÂÃÂ³ng, tin cÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ­y vÃÂÃÂÃÂÃÂ  liÃÂÃÂÃÂÃÂªn hÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ trÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ±c tiÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿p qua WhatsApp hoÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ·c WeChat.",
                heroCta: "ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ·t lÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂch hÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¹n",
                procHeader: "Quy trÃÂÃÂÃÂÃÂ¬nh ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂng kÃÂÃÂÃÂÃÂ½",
                step1T: "Chat trÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ±c tiÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿p",
                step1D: "KÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿t nÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂi vÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂi chuyÃÂÃÂÃÂÃÂªn gia cÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ§a chÃÂÃÂÃÂÃÂºng tÃÂÃÂÃÂÃÂ´i ngay lÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ­p tÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ©c qua WhatsApp hoÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ·c WeChat (ID: Turjo1992) ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ bÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¯t ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ§u hÃÂÃÂÃÂÃÂ nh trÃÂÃÂÃÂÃÂ¬nh cÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ§a bÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¡n.",
                step2T: "ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂ¡nh giÃÂÃÂÃÂÃÂ¡ hÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ sÃÂÃÂÃÂÃÂ¡",
                step2D: "Chia sÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ» lÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂch sÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ­ du lÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂch vÃÂÃÂÃÂÃÂ  ÃÂÃÂÃÂÃÂiÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂm ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿n cÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ§a bÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¡n. ChÃÂÃÂÃÂÃÂºng tÃÂÃÂÃÂÃÂ´i cung cÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¥p danh sÃÂÃÂÃÂÃÂ¡ch kiÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂm tra hÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ sÃÂÃÂÃÂÃÂ¡ phÃÂÃÂÃÂÃÂ¹ hÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ£p.",
                step3T: "NÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂp hÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ sÃÂÃÂÃÂÃÂ¡",
                step3D: "Khi tÃÂÃÂÃÂÃÂ i liÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂu ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂ£ sÃÂÃÂ¡ÃÂÃÂºÃÂÃÂµn sÃÂÃÂÃÂÃÂ ng, chÃÂÃÂÃÂÃÂºng tÃÂÃÂÃÂÃÂ´i sÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ½ nÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂp ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂ¡n chÃÂÃÂÃÂÃÂ­nh thÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ©c cho ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¡i sÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ© quÃÂÃÂÃÂÃÂ¡n tÃÂÃÂÃÂÃÂ°ÃÂÃÂÃÂÃÂ¡ng ÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ©ng.",
                step4T: "PhÃÂÃÂÃÂÃÂª duyÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂt",
                step4D: "ChÃÂÃÂÃÂÃÂºng tÃÂÃÂÃÂÃÂ´i theo dÃÂÃÂÃÂÃÂµi ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂ¡n ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂng kÃÂÃÂÃÂÃÂ½ cÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ§a bÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¡n hÃÂÃÂÃÂÃÂ ng ngÃÂÃÂÃÂÃÂ y vÃÂÃÂÃÂÃÂ  gÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ­i trÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ±c tiÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿p kÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿t quÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ£ phÃÂÃÂÃÂÃÂª duyÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂt thÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ thÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ±c cho bÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¡n.",
                destH: "ChÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂn ÃÂÃÂÃÂÃÂiÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂm ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¿n",
                destS: "NhÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¥n vÃÂÃÂÃÂÃÂ o mÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂt quÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂc gia ÃÂÃÂÃÂÃÂÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ ÃÂÃÂÃÂÃÂÃÂÃÂÃÂÃÂng kÃÂÃÂÃÂÃÂ½ qua WhatsApp",
                copy: "&copy; 2025 DÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂch vÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ¥ Fly View Visa. BÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ£o lÃÂÃÂÃÂÃÂ°u mÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂi quyÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂn.<br>TÃÂÃÂÃÂÃÂ° vÃÂÃÂ¡ÃÂÃÂºÃÂÃÂ¥n & XÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂ­ lÃÂÃÂÃÂÃÂ½ Visa chuyÃÂÃÂÃÂÃÂªn nghiÃÂÃÂ¡ÃÂÃÂ»ÃÂÃÂp."
            },
            zh: {
                home: "ÃÂÃÂ©ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ©ÃÂÃÂ¡ÃÂÃÂµ",
                destinations: "ÃÂÃÂ§ÃÂÃÂÃÂÃÂ®ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ°",
                apply: "ÃÂÃÂ¥ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¤ÃÂÃÂ½ÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ·",
                chat: "WhatsApp ÃÂÃÂ¨ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¤ÃÂÃÂ©",
                heroTitle: "Fly View <span>ÃÂÃÂ§ÃÂÃÂ­ÃÂÃÂ¾ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ</span>",
                heroDesc: "ÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂº 40 ÃÂÃÂ¥ÃÂÃÂ¤ÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂªÃÂÃÂ¥ÃÂÃÂÃÂÃÂ½ÃÂÃÂ¥ÃÂÃÂ®ÃÂÃÂ¶ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¾ÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¼ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ´ÃÂÃÂ¨ÃÂÃÂ§ÃÂÃÂ­ÃÂÃÂ¾ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ¢ÃÂÃÂ£ÃÂÃÂÃÂÃÂÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¿ÃÂÃÂ WhatsApp ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¾ÃÂÃÂ®ÃÂÃÂ¤ÃÂÃÂ¿ÃÂÃÂ¡ÃÂÃÂ¥ÃÂÃÂ¿ÃÂÃÂ«ÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ£ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¯ÃÂÃÂ©ÃÂÃÂÃÂÃÂ ÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂ´ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¨ÃÂÃÂ®ÃÂÃÂ¿ÃÂÃÂ©ÃÂÃÂÃÂÃÂ®ÃÂÃÂ£ÃÂÃÂÃÂÃÂ",
                heroCta: "ÃÂÃÂ©ÃÂÃÂ¢ÃÂÃÂÃÂÃÂ§ÃÂÃÂºÃÂÃÂ¦ÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ¢",
                procHeader: "ÃÂÃÂ§ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ·ÃÂÃÂ¦ÃÂÃÂµÃÂÃÂÃÂÃÂ§ÃÂÃÂ¨ÃÂÃÂ",
                step1T: "ÃÂÃÂ§ÃÂÃÂÃÂÃÂ´ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¨ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¤ÃÂÃÂ©",
                step1D: "ÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¿ÃÂÃÂ WhatsApp ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¾ÃÂÃÂ®ÃÂÃÂ¤ÃÂÃÂ¿ÃÂÃÂ¡ (ID: Turjo1992) ÃÂÃÂ§ÃÂÃÂ«ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂ³ÃÂÃÂ»ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ»ÃÂÃÂ¬ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ®ÃÂÃÂ¶ÃÂÃÂ¯ÃÂÃÂ¼ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¼ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¯ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂ¨ÃÂÃÂÃÂÃÂ£ÃÂÃÂÃÂÃÂ",
                step2T: "ÃÂÃÂ¨ÃÂÃÂµÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¼ÃÂÃÂ°",
                step2D: "ÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂºÃÂÃÂ«ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¡ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ²ÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂ®ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ°ÃÂÃÂ£ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ»ÃÂÃÂ¬ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¾ÃÂÃÂÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ¨ÃÂÃÂºÃÂÃÂ«ÃÂÃÂ¥ÃÂÃÂ®ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¶ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ£ÃÂÃÂÃÂÃÂ",
                step3T: "ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂºÃÂÃÂ¤ÃÂÃÂ§ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ·",
                step3D: "ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¤ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ°ÃÂÃÂ±ÃÂÃÂ§ÃÂÃÂ»ÃÂÃÂªÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ¯ÃÂÃÂ¼ÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ»ÃÂÃÂ¬ÃÂÃÂ¨ÃÂÃÂ´ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ´ÃÂÃÂ£ÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂ¸ÃÂÃÂ¥ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¤ÃÂÃÂ½ÃÂÃÂ¿ÃÂÃÂ©ÃÂÃÂ¢ÃÂÃÂÃÂÃÂ©ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ£ÃÂÃÂ¥ÃÂÃÂ¼ÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂºÃÂÃÂ¤ÃÂÃÂ§ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ·ÃÂÃÂ£ÃÂÃÂÃÂÃÂ",
                step4T: "ÃÂÃÂ§ÃÂÃÂ­ÃÂÃÂ¾ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¨ÃÂÃÂÃÂÃÂ·ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¹",
                step4D: "ÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¤ÃÂÃÂ»ÃÂÃÂ¬ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¤ÃÂÃÂ©ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂ§ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ·ÃÂÃÂ¯ÃÂÃÂ¼ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¹ÃÂÃÂ¶ÃÂÃÂ¥ÃÂÃÂ°ÃÂÃÂÃÂÃÂ§ÃÂÃÂ­ÃÂÃÂ¾ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¹ÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂ»ÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂ´ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¥ÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂ»ÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ£ÃÂÃÂÃÂÃÂ",
                destH: "ÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂ©ÃÂÃÂ§ÃÂÃÂÃÂÃÂ®ÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ°",
                destS: "ÃÂÃÂ§ÃÂÃÂÃÂÃÂ¹ÃÂÃÂ¥ÃÂÃÂÃÂÃÂ»ÃÂÃÂ¥ÃÂÃÂÃÂÃÂ½ÃÂÃÂ¥ÃÂÃÂ®ÃÂÃÂ¶ÃÂÃÂ©ÃÂÃÂÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¿ÃÂÃÂ WhatsApp ÃÂÃÂ§ÃÂÃÂÃÂÃÂ³ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ·",
                copy: "&copy; 2025 Fly View ÃÂÃÂ§ÃÂÃÂ­ÃÂÃÂ¾ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¡ÃÂÃÂ£ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ¦ÃÂÃÂÃÂÃÂÃÂÃÂ£ÃÂÃÂÃÂÃÂ<br>ÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂÃÂÃÂ§ÃÂÃÂ­ÃÂÃÂ¾ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂ¨ÃÂÃÂ¨ÃÂÃÂ¯ÃÂÃÂ¢ÃÂÃÂ¤ÃÂÃÂ¸ÃÂÃÂÃÂÃÂ¥ÃÂÃÂÃÂÃÂÃÂÃÂ§ÃÂÃÂÃÂÃÂÃÂÃÂ£ÃÂÃÂÃÂÃÂ"
            },
            bn: {
                home: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®",
                destinations: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯",
                apply: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿",
                chat: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂª ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ",
                heroTitle: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ«ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ <span>ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾</span>",
                heroDesc: "ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ® ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂª ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤",
                heroCta: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨",
                procHeader: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾",
                step1T: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ",
                step1D: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂª ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° (ID: Turjo1992) ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ·ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¥ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤",
                step2T: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ«ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ² ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨",
                step2D: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ£ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ·ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¥ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤",
                step3T: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨",
                step3D: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¥ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ, ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ·ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ·ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤",
                step4T: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨",
                step4D: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ·ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ£ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤",
                destH: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨",
                destS: "ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¹ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¼ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ®ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¯ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂª ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨",
                copy: "&copy; ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂ« ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ«ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¬ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ·ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¤ÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤<br>ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ° ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ­ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¾ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ²ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¶ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¨ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂªÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ°ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ§ÃÂÃÂÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¸ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂ¿ÃÂÃÂ ÃÂÃÂ¦ÃÂÃÂÃÂÃÂ ÃÂÃÂ¥ÃÂÃÂ¤"
            }
        };

        function changeLanguage(lang) {
            const t = translations[lang];
            
            // Hero
            document.getElementById('hero-title').innerHTML = t.heroTitle;
            document.getElementById('hero-desc').innerText = t.heroDesc;
            document.getElementById('hero-cta').innerHTML = `<i class="fab fa-whatsapp"></i> ${t.heroCta}`;
            
            // Process
            document.getElementById('process-header').innerText = t.procHeader;
            document.getElementById('step1-title').innerText = t.step1T;
            document.getElementById('step1-desc').innerText = t.step1D;
            document.getElementById('step2-title').innerText = t.step2T;
            document.getElementById('step2-desc').innerText = t.step2D;
            document.getElementById('step3-title').innerText = t.step3T;
            document.getElementById('step3-desc').innerText = t.step3D;
            document.getElementById('step4-title').innerText = t.step4T;
            document.getElementById('step4-desc').innerText = t.step4D;
            
            // Destinations
            document.getElementById('dest-header').innerText = t.destH;
            document.getElementById('dest-sub').innerText = t.destS;
            
            // Mobile Menu
            document.getElementById('m-home').innerText = t.home;
            document.getElementById('m-dest').innerText = t.destinations;
            document.getElementById('m-process').innerText = t.apply;
            document.getElementById('m-chat').innerText = t.chat;
            
            // Footer
            document.getElementById('copyright-text').innerHTML = t.copy;

            // Update UI elements
            document.getElementById('langSelectNav').value = lang;
            
            // Toggle active buttons in mobile menu
            document.querySelectorAll('.lang-btn').forEach(btn => btn.classList.remove('active'));
            const mobileBtn = document.getElementById('btn-' + lang);
            if(mobileBtn) mobileBtn.classList.add('active');

            // Save preference
            localStorage.setItem('flyview_lang', lang);
        }

        function toggleMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('active');
            document.body.style.overflow = menu.classList.contains('active') ? 'hidden' : 'auto';
        }

        // Initialize with English or saved language
        window.onload = () => {
            const savedLang = localStorage.getItem('flyview_lang') || 'en';
            changeLanguage(savedLang);
        };
    </script>
</body>