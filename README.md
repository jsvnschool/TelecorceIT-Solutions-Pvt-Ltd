<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telecorcel IT Solutions Pvt Ltd | Enterprise Messaging, Cloud Communication & IT Engineering</title>
    
    <!-- Google Fonts & Font Awesome 6 Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #0284c7;
            --primary-dark: #0369a1;
            --primary-light: #e0f2fe;
            --secondary: #0f172a;
            --surface: #1e293b;
            --accent: #10b981;
            --accent-purple: #6366f1;
            --bg-light: #f8fafc;
            --border: #e2e8f0;
            --text-dark: #0f172a;
            --text-muted: #64748b;
            --white: #ffffff;
            --radius-md: 10px;
            --radius-lg: 16px;
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.08);
            --shadow-md: 0 8px 24px rgba(15,23,42,0.08);
            --shadow-lg: 0 14px 34px rgba(15,23,42,0.12);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--white);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Top Announcement Header */
        .top-banner {
            background: linear-gradient(90deg, #0f172a, #1e293b);
            color: #cbd5e1;
            padding: 9px 5%;
            font-size: 0.85rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255,255,255,0.08);
        }

        .top-banner .contact-links a {
            color: #f1f5f9;
            text-decoration: none;
            margin-left: 20px;
            font-weight: 500;
            transition: color 0.2s;
        }

        .top-banner .contact-links a:hover {
            color: var(--primary);
        }

        /* Navbar */
        header {
            position: sticky;
            top: 0;
            z-index: 1100;
            background: rgba(255,255,255,0.96);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 18px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .brand-logo {
            font-size: 1.45rem;
            font-weight: 800;
            color: var(--secondary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .brand-logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 26px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: #334155;
            font-weight: 600;
            font-size: 0.95rem;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .btn-cta {
            background: var(--primary);
            color: var(--white) !important;
            padding: 10px 22px;
            border-radius: 8px;
            font-weight: 700;
            box-shadow: 0 4px 14px rgba(2, 132, 199, 0.35);
            transition: all 0.25s ease;
        }

        .btn-cta:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
        }

        /* Ticker Bar */
        .marquee-bar {
            background: #f1f5f9;
            color: #475569;
            padding: 12px 0;
            overflow: hidden;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            white-space: nowrap;
            border-bottom: 1px solid var(--border);
        }

        .marquee-content {
            display: inline-block;
            animation: marquee 35s linear infinite;
        }

        @keyframes marquee {
            0% { transform: translateX(0%); }
            100% { transform: translateX(-50%); }
        }

        /* Hero Section */
        .hero {
            background: radial-gradient(circle at 80% 20%, rgba(2, 132, 199, 0.08) 0%, rgba(255, 255, 255, 0) 60%),
                        linear-gradient(180deg, #f8fafc 0%, #ffffff 100%);
            padding: 100px 5% 80px;
            text-align: center;
        }

        .hero-inner {
            max-width: 1050px;
            margin: 0 auto;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: var(--primary-light);
            color: var(--primary-dark);
            padding: 6px 16px;
            border-radius: 999px;
            font-size: 0.85rem;
            font-weight: 700;
            margin-bottom: 24px;
        }

        .hero h1 {
            font-size: 3.4rem;
            line-height: 1.15;
            font-weight: 800;
            color: var(--secondary);
            margin-bottom: 24px;
            letter-spacing: -0.02em;
        }

        .hero h1 span {
            background: linear-gradient(90deg, #0284c7, #6366f1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--text-muted);
            max-width: 820px;
            margin: 0 auto 36px;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 50px;
        }

        .btn-outline {
            border: 2px solid #cbd5e1;
            padding: 12px 26px;
            border-radius: 8px;
            color: var(--secondary);
            text-decoration: none;
            font-weight: 700;
            background: transparent;
            transition: all 0.25s;
        }

        .btn-outline:hover {
            border-color: var(--primary);
            color: var(--primary);
            background: #f0f9ff;
        }

        /* Stats strip */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            max-width: 960px;
            margin: 0 auto;
            padding: 30px;
            background: var(--white);
            border-radius: var(--radius-lg);
            box-shadow: var(--shadow-md);
            border: 1px solid var(--border);
        }

        .stat-item h3 {
            font-size: 2rem;
            font-weight: 800;
            color: var(--primary);
        }

        .stat-item p {
            font-size: 0.9rem;
            color: var(--text-muted);
            font-weight: 600;
        }

        /* Universal Section Structure */
        section {
            padding: 95px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            max-width: 750px;
            margin: 0 auto 60px;
        }

        .section-header h4 {
            color: var(--primary);
            text-transform: uppercase;
            font-size: 0.85rem;
            font-weight: 800;
            letter-spacing: 1.5px;
            margin-bottom: 10px;
        }

        .section-header h2 {
            font-size: 2.35rem;
            color: var(--secondary);
            font-weight: 800;
            letter-spacing: -0.02em;
        }

        .section-header p {
            color: var(--text-muted);
            margin-top: 12px;
            font-size: 1.05rem;
        }

        /* Core Services Grid */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .grid-4 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 24px;
        }

        .feature-card {
            background: var(--white);
            padding: 35px 30px;
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
            position: relative;
        }

        .feature-card:hover {
            transform: translateY(-8px);
            border-color: var(--primary);
            box-shadow: var(--shadow-lg);
        }

        .card-icon {
            width: 58px;
            height: 58px;
            background: #f0f9ff;
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 12px;
            font-size: 1.6rem;
            margin-bottom: 22px;
        }

        .feature-card h3 {
            font-size: 1.35rem;
            margin-bottom: 12px;
            color: var(--secondary);
            font-weight: 700;
        }

        .feature-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 16px;
        }

        .bullet-list {
            list-style: none;
            padding: 0;
            margin-top: 15px;
            border-top: 1px solid #f1f5f9;
            padding-top: 15px;
        }

        .bullet-list li {
            font-size: 0.9rem;
            color: #475569;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .bullet-list li i {
            color: var(--accent);
            font-size: 0.8rem;
        }

        /* Developer API Showcase Section */
        .api-section {
            background: var(--surface);
            color: var(--white);
            border-radius: var(--radius-lg);
            padding: 60px;
            margin: 40px auto;
            max-width: 1400px;
        }

        .api-container {
            display: grid;
            grid-template-columns: 1fr 1.1fr;
            gap: 40px;
            align-items: center;
        }

        .api-codebox {
            background: #090d16;
            border: 1px solid #334155;
            border-radius: 12px;
            padding: 24px;
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.85rem;
            color: #38bdf8;
            overflow-x: auto;
        }

        .api-codebox pre {
            font-family: inherit;
        }

        /* Industries Section */
        .industry-card {
            background: #ffffff;
            border: 1px solid var(--border);
            padding: 24px 18px;
            border-radius: var(--radius-md);
            text-align: center;
            font-weight: 700;
            color: var(--secondary);
            transition: all 0.2s;
        }

        .industry-card i {
            font-size: 2rem;
            color: var(--primary);
            display: block;
            margin-bottom: 12px;
        }

        .industry-card:hover {
            background: #f0f9ff;
            border-color: var(--primary);
            color: var(--primary-dark);
        }

        /* Pricing Matrix Section */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .pricing-card {
            background: var(--white);
            border: 1px solid var(--border);
            border-radius: var(--radius-lg);
            padding: 35px 25px;
            text-align: center;
            position: relative;
            transition: transform 0.3s;
        }

        .pricing-card:hover {
            transform: translateY(-6px);
            border-color: var(--primary);
            box-shadow: var(--shadow-md);
        }

        .pricing-card.featured {
            border: 2px solid var(--primary);
            background: #fcfdfe;
        }

        .badge-popular {
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary);
            color: var(--white);
            padding: 4px 14px;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 800;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }

        .pricing-card h3 {
            font-size: 1.25rem;
            color: var(--secondary);
            margin-bottom: 12px;
        }

        .pricing-card .price {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .pricing-card .price span {
            font-size: 0.85rem;
            color: var(--text-muted);
            font-weight: 500;
        }

        /* Leadership Block */
        .leadership-wrapper {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 30px;
            max-width: 850px;
            margin: 0 auto;
        }

        .leader-box {
            background: var(--white);
            border: 1px solid var(--border);
            border-radius: var(--radius-md);
            padding: 30px;
            display: flex;
            gap: 20px;
            align-items: center;
            box-shadow: var(--shadow-sm);
        }

        .leader-avatar {
            width: 75px;
            height: 75px;
            background: #e2e8f0;
            color: #64748b;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            flex-shrink: 0;
        }

        .leader-box h3 {
            font-size: 1.2rem;
            color: var(--secondary);
            margin-bottom: 4px;
        }

        .leader-box .tag {
            color: var(--primary);
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
        }

        /* Locations & Physical Presence */
        .locations-box {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
        }

        .loc-card {
            background: var(--bg-light);
            border: 1px solid var(--border);
            padding: 28px;
            border-radius: var(--radius-md);
            border-left: 5px solid var(--primary);
        }

        .loc-card h4 {
            color: var(--secondary);
            font-size: 1.15rem;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Contact Section */
        .contact-layout {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            background: #f8fafc;
            border-radius: var(--radius-lg);
            padding: 50px;
            border: 1px solid var(--border);
        }

        .form-row {
            margin-bottom: 18px;
        }

        .form-row label {
            display: block;
            margin-bottom: 7px;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--secondary);
        }

        .form-row input, .form-row select, .form-row textarea {
            width: 100%;
            padding: 12px 16px;
            border-radius: 8px;
            border: 1px solid #cbd5e1;
            font-size: 0.95rem;
            background: var(--white);
        }

        .form-row input:focus, .form-row select:focus, .form-row textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(2, 132, 199, 0.15);
        }

        /* Footer */
        footer {
            background: #090d16;
            color: #94a3b8;
            padding: 70px 5% 25px;
            border-top: 1px solid #1e293b;
        }

        .footer-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1.5fr;
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-grid h4 {
            color: var(--white);
            margin-bottom: 20px;
            font-size: 1rem;
        }

        .footer-grid ul {
            list-style: none;
        }

        .footer-grid ul li {
            margin-bottom: 10px;
            font-size: 0.9rem;
        }

        .footer-grid ul li a {
            color: #94a3b8;
            text-decoration: none;
            transition: color 0.2s;
        }

        .footer-grid ul li a:hover {
            color: var(--white);
        }

        .copyright {
            max-width: 1400px;
            margin: 0 auto;
            padding-top: 25px;
            border-top: 1px solid #1e293b;
            font-size: 0.85rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* Mobile responsiveness */
        @media (max-width: 900px) {
            .hero h1 { font-size: 2.3rem; }
            .stats-grid { grid-template-columns: repeat(2, 1fr); }
            .contact-layout { grid-template-columns: 1fr; padding: 25px; }
            .api-container { grid-template-columns: 1fr; }
            .nav-links { display: none; }
            .footer-grid { grid-template-columns: 1fr; }
            .top-banner { flex-direction: column; gap: 6px; text-align: center; }
            .top-banner .contact-links a { margin: 0 8px; }
        }
    </style>
</head>
<body>

    <!-- Top Info Bar -->
    <div class="top-banner">
        <div>
            <i class="fa-solid fa-building-shield"></i> Official TRAI DLT Compliant & Enterprise Telecom Partner
        </div>
        <div class="contact-links">
            <a href="tel:9012574505"><i class="fa-solid fa-phone"></i> +91 9012574505</a>
            <a href="tel:7678519164"><i class="fa-solid fa-phone"></i> +91 7678519164</a>
            <a href="#contact"><i class="fa-solid fa-envelope"></i> Sales Desk</a>
        </div>
    </div>

    <!-- Main Navigation Bar -->
    <header>
        <nav>
            <a href="#home" class="brand-logo">
                <i class="fa-solid fa-tower-broadcast" style="color: var(--primary);"></i>
                Telecorcel <span>IT Solutions</span>
            </a>
            <ul class="nav-links">
                <li><a href="#telecom">Bulk SMS & DLT</a></li>
                <li><a href="#omnichannel">WhatsApp & Email</a></li>
                <li><a href="#it-solutions">Software & Web</a></li>
                <li><a href="#digital-growth">Digital Ads & SEO</a></li>
                <li><a href="#apis">REST APIs</a></li>
                <li><a href="#pricing">Pricing</a></li>
                <li><a href="#leadership">Team</a></li>
                <li><a href="#contact" class="btn-cta">Enquire Now</a></li>
            </ul>
        </nav>
    </header>

    <!-- Services Announcement Ticker -->
    <div class="marquee-bar">
        <div class="marquee-content">
            &bull; Bulk SMS &bull; Email Marketing &bull; WhatsApp Business API &bull; Voice & IVR &bull; DLT Template Approval &bull; Website Development &bull; Android / iOS Apps &bull; ERP / CRM Development &bull; SEO &bull; Google Ads &bull; Social Media &bull; B2B Lead Generation &bull; Developer Messaging APIs &nbsp;&nbsp;&nbsp;&bull;&nbsp;&nbsp;&nbsp;
            &bull; Bulk SMS &bull; Email Marketing &bull; WhatsApp Business API &bull; Voice & IVR &bull; DLT Template Approval &bull; Website Development &bull; Android / iOS Apps &bull; ERP / CRM Development &bull; SEO &bull; Google Ads &bull; Social Media &bull; B2B Lead Generation &bull; Developer Messaging APIs
        </div>
    </div>

    <!-- Hero Section -->
    <div class="hero" id="home">
        <div class="hero-inner">
            <div class="badge"><i class="fa-solid fa-bolt"></i> High-Throughput Tier-1 SMS & Cloud Gateway</div>
            <h1>Scale Customer Outreach With <span>Unified Messaging & IT Engineering</span></h1>
            <p>From DLT-approved Transactional SMS, WhatsApp Business API, and automated Voice IVR to enterprise Web applications and high-impact digital marketing campaigns.</p>
            
            <div class="hero-buttons">
                <a href="#contact" class="btn-cta" style="padding: 14px 32px; font-size: 1.05rem;">Request a Consultation</a>
                <a href="#pricing" class="btn-outline">Explore Pricing Matrix</a>
            </div>

            <div class="stats-grid">
                <div class="stat-item">
                    <h3>99.98%</h3>
                    <p>API Uptime</p>
                </div>
                <div class="stat-item">
                    <h3>&lt; 5 Sec</h3>
                    <p>Fast OTP Delivery</p>
                </div>
                <div class="stat-item">
                    <h3>100%</h3>
                    <p>DLT Support</p>
                </div>
                <div class="stat-item">
                    <h3>500+</h3>
                    <p>Deployments</p>
                </div>
            </div>
        </div>
    </div>

    <!-- 1 & 2. Bulk SMS & DLT Architecture Section -->
    <section id="telecom">
        <div class="section-header">
            <h4>TRAI Compliant Telecom Gateway</h4>
            <h2>Enterprise Bulk SMS & DLT Services</h2>
            <p>Direct operator connectivity for lightning-fast OTPs, real-time alerts, and large-scale promotional broadcasts.</p>
        </div>

        <div class="grid-3">
            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-shield-halved"></i></div>
                <h3>Transactional & OTP SMS</h3>
                <p>Mission-critical delivery for 2FA, OTPs, booking confirmations, and bank alerts with prioritized carrier routing.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> High Priority Gateway</li>
                    <li><i class="fa-solid fa-check"></i> 24/7/365 Open Bandwidth</li>
                    <li><i class="fa-solid fa-check"></i> Failover Retries & Fallback</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-bullhorn"></i></div>
                <h3>Promotional & Flash SMS</h3>
                <p>Targeted discount broadcasts, customer outreach campaigns, product updates, and seasonal flash messages.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Unicode & Multi-lingual SMS</li>
                    <li><i class="fa-solid fa-check"></i> Non-DND 10 AM to 9 PM Window</li>
                    <li><i class="fa-solid fa-check"></i> Dynamic Sender Name Support</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-file-signature"></i></div>
                <h3>DLT Registration Assistance</h3>
                <p>Complete compliance guidance on Jio, Airtel, VI, and BSNL DLT portals to avoid template rejection and spam bans.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Entity & Telemarketer Registration</li>
                    <li><i class="fa-solid fa-check"></i> Sender ID (Header) Approval</li>
                    <li><i class="fa-solid fa-check"></i> Consent & Template Submissions</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- 4, 5 & 6. Omnichannel Marketing & Voice IVR -->
    <section id="omnichannel" style="background: var(--bg-light); border-radius: var(--radius-lg);">
        <div class="section-header">
            <h4>Omnichannel Engagement</h4>
            <h2>WhatsApp, Email Marketing & Voice IVR</h2>
            <p>Connect with your audience on channels they use every day with verifiable open rates and interactive responses.</p>
        </div>

        <div class="grid-3">
            <div class="feature-card">
                <div class="card-icon" style="color: #25d366; background: #e8fbee;"><i class="fa-brands fa-whatsapp"></i></div>
                <h3>WhatsApp Business API</h3>
                <p>Verified Green Tick guidance, automated chatbot flows, transactional updates, and approved marketing templates.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Order & Delivery Trackers</li>
                    <li><i class="fa-solid fa-check"></i> Automated Chatbot Journeys</li>
                    <li><i class="fa-solid fa-check"></i> Quick Reply Interactive Buttons</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon" style="color: #ea4335; background: #fdf2f2;"><i class="fa-solid fa-envelope-open-text"></i></div>
                <h3>Enterprise Email Marketing</h3>
                <p>High inbox delivery rates with clean IP pools, automated drip workflows, transactional notifications, and HTML newsletters.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Bulk Email Delivery at Scale</li>
                    <li><i class="fa-solid fa-check"></i> Real-Time Open/Click Analytics</li>
                    <li><i class="fa-solid fa-check"></i> SPF/DKIM/DMARC Security Setup</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon" style="color: #8b5cf6; background: #f3f0ff;"><i class="fa-solid fa-headset"></i></div>
                <h3>Voice Calls & Cloud IVR</h3>
                <p>Automate outbound customer calls, reminders, and interactive inbound menu trees with robust voice campaign logs.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Bulk Voice Broadcasts (OBD)</li>
                    <li><i class="fa-solid fa-check"></i> Multi-level IVR Systems</li>
                    <li><i class="fa-solid fa-check"></i> Real-Time Call Duration Logs</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- 7, 8, 9 & 10. IT Engineering, Web & Apps -->
    <section id="it-solutions">
        <div class="section-header">
            <h4>Full-Stack Engineering</h4>
            <h2>Web, Mobile App & SaaS Development</h2>
            <p>We engineer secure, scalable, and revenue-generating digital products built with modern cloud tech stacks.</p>
        </div>

        <div class="grid-3">
            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-code"></i></div>
                <h3>Website & Portal Development</h3>
                <p>Tailor-made web solutions designed for high conversion, robust SEO architectures, and responsive screen compatibility.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Corporate & Business Websites</li>
                    <li><i class="fa-solid fa-check"></i> E-commerce Portals & Gateways</li>
                    <li><i class="fa-solid fa-check"></i> Website Redesign & Maintenance</li>
                    <li><i class="fa-solid fa-check"></i> SSL, Domain & Cloud Hosting</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-mobile-screen-button"></i></div>
                <h3>Mobile Application Development</h3>
                <p>Native and hybrid smartphone apps optimized for high performance, smooth animations, and intuitive UI/UX design.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Android & iOS Native App Dev</li>
                    <li><i class="fa-solid fa-check"></i> Cross-Platform Apps (Flutter/React)</li>
                    <li><i class="fa-solid fa-check"></i> Service Booking & Delivery Apps</li>
                    <li><i class="fa-solid fa-check"></i> App Store & Play Store Submissions</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-cubes"></i></div>
                <h3>Software, ERP & SaaS Applications</h3>
                <p>Streamline internal business operations with modular back-office platforms, CRM setups, and custom web dashboards.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Custom CRM & Admin Panels</li>
                    <li><i class="fa-solid fa-check"></i> Inventory & Billing Softwares</li>
                    <li><i class="fa-solid fa-check"></i> Multi-tenant SaaS Product MVPs</li>
                    <li><i class="fa-solid fa-check"></i> Custom REST API Integrations</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Digital Advertising, SEO & Social Media -->
    <section id="digital-growth" style="background: var(--bg-light); border-radius: var(--radius-lg);">
        <div class="section-header">
            <h4>Performance Marketing & Branding</h4>
            <h2>Digital Advertising, Social Media & Lead Gen</h2>
            <p>Target bottom-of-the-funnel leads and maximize return on ad spend with end-to-end data-driven campaigns.</p>
        </div>

        <div class="grid-3">
            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-chart-line"></i></div>
                <h3>Google Ads & PPC Campaigns</h3>
                <p>High-intent Google Search ads, remarketing, and YouTube display advertisements designed to generate immediate inquiries.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Search Engine Marketing (SEM)</li>
                    <li><i class="fa-solid fa-check"></i> Conversion Rate Optimization (CRO)</li>
                    <li><i class="fa-solid fa-check"></i> High-Converting Landing Pages</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-share-nodes"></i></div>
                <h3>Social Media Marketing (SMM)</h3>
                <p>Comprehensive creative strategy, paid Facebook/Instagram ad funnels, audience targeting, and brand building.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Social Media Content Calendars</li>
                    <li><i class="fa-solid fa-check"></i> Paid Audience Retargeting</li>
                    <li><i class="fa-solid fa-check"></i> Brand Identity & Creative Design</li>
                </ul>
            </div>

            <div class="feature-card">
                <div class="card-icon"><i class="fa-solid fa-filter-circle-dollar"></i></div>
                <h3>B2B Lead Generation & SEO</h3>
                <p>Consistent organic traffic growth through search ranking, localized SEO citations, and qualified B2B lead pipelines.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Technical & On-Page SEO Audits</li>
                    <li><i class="fa-solid fa-check"></i> Qualified B2B Inquiry Funnels</li>
                    <li><i class="fa-solid fa-check"></i> Performance Tracking & Analytics</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Developer Messaging APIs Block -->
    <div class="api-section" id="apis">
        <div class="api-container">
            <div>
                <span class="badge" style="background: #38bdf8; color: #0f172a;">Developer First</span>
                <h2 style="font-size: 2.2rem; margin-bottom: 20px;">Robust, Low-Latency Messaging APIs</h2>
                <p style="color: #cbd5e1; margin-bottom: 25px;">Integrate SMS, OTP, WhatsApp, Email, and IVR services into your software stack with simple HTTP POST requests and real-time webhook status updates.</p>
                <ul class="bullet-list" style="border-top-color: #334155;">
                    <li style="color: #e2e8f0;"><i class="fa-solid fa-check" style="color: #38bdf8;"></i> Comprehensive REST API Documentation</li>
                    <li style="color: #e2e8f0;"><i class="fa-solid fa-check" style="color: #38bdf8;"></i> Instant Webhook & Delivery Status Callbacks</li>
                    <li style="color: #e2e8f0;"><i class="fa-solid fa-check" style="color: #38bdf8;"></i> Multi-language SDKs (PHP, Node.js, Python, Java)</li>
                </ul>
            </div>
            <div class="api-codebox">
<pre>
<span style="color: #64748b;">// Telecorcel SMS & OTP API Sample Call</span>
curl -X POST https://api.telecorcel.in/v1/sms/send \
  -H <span style="color: #facc15;">"Authorization: Bearer YOUR_API_TOKEN"</span> \
  -H <span style="color: #facc15;">"Content-Type: application/json"</span> \
  -d '{
    <span style="color: #f43f5e;">"sender_id"</span>: <span style="color: #facc15;">"TLCRCL"</span>,
    <span style="color: #f43f5e;">"dlt_template_id"</span>: <span style="color: #facc15;">"120116XXXXXXXX"</span>,
    <span style="color: #f43f5e;">"recipients"</span>: [<span style="color: #facc15;">"+919012574505"</span>],
    <span style="color: #f43f5e;">"message"</span>: <span style="color: #facc15;">"Your verification code is 849201. Telecorcel IT Solutions."</span>,
    <span style="color: #f43f5e;">"webhook_url"</span>: <span style="color: #facc15;">"https://yourdomain.com/callbacks"</span>
  }'
</pre>
            </div>
        </div>
    </div>

    <!-- Industries Served -->
    <section>
        <div class="section-header">
            <h4>Versatile Implementations</h4>
            <h2>Industries Empowered By Telecorcel</h2>
            <p>Proven reliability across consumer-facing and corporate verticals.</p>
        </div>
        <div class="grid-4">
            <div class="industry-card"><i class="fa-solid fa-cart-shopping"></i> E-commerce & Retail</div>
            <div class="industry-card"><i class="fa-solid fa-graduation-cap"></i> Education & EdTech</div>
            <div class="industry-card"><i class="fa-solid fa-stethoscope"></i> Healthcare & Hospitals</div>
            <div class="industry-card"><i class="fa-solid fa-building-wheat"></i> Real Estate & Infra</div>
            <div class="industry-card"><i class="fa-solid fa-landmark"></i> Banking & Finance (BFSI)</div>
            <div class="industry-card"><i class="fa-solid fa-plane-departure"></i> Tours, Travel & Hospitality</div>
            <div class="industry-card"><i class="fa-solid fa-truck-fast"></i> Logistics & Supply Chain</div>
            <div class="industry-card"><i class="fa-solid fa-utensils"></i> Restaurants & FoodTech</div>
        </div>
    </section>

    <!-- Pricing Matrix Cards -->
    <section id="pricing" style="background: var(--bg-light); border-radius: var(--radius-lg);">
        <div class="section-header">
            <h4>Transparent Subscriptions</h4>
            <h2>Pricing Cards & Packages</h2>
            <p>Competitive wholesale pricing with zero hidden charges. Contact us for custom volume slab discounts.</p>
        </div>

        <div class="pricing-grid">
            <!-- Promotional SMS -->
            <div class="pricing-card">
                <h3>Promotional SMS</h3>
                <div class="price">₹0.15<span> / SMS</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Volume: Minimum 50k credits</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Open Timing (10 AM - 9 PM)</li>
                    <li><i class="fa-solid fa-check"></i> 100% Delivery Reports</li>
                    <li><i class="fa-solid fa-check"></i> Free DLT Template Setup</li>
                </ul>
                <a href="#contact" class="btn-outline" style="display:block; margin-top:20px;">Book Plan</a>
            </div>

            <!-- Transactional / OTP SMS -->
            <div class="pricing-card featured">
                <span class="badge-popular">Highest Demand</span>
                <h3>Transactional / OTP</h3>
                <div class="price">₹0.18<span> / SMS</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Volume: Minimum 25k credits</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> High Priority Carrier Routes</li>
                    <li><i class="fa-solid fa-check"></i> Round-the-clock 24/7 Delivery</li>
                    <li><i class="fa-solid fa-check"></i> Ultra-Fast Delivery (&lt; 5s)</li>
                </ul>
                <a href="#contact" class="btn-cta" style="display:block; margin-top:20px;">Get Started</a>
            </div>

            <!-- WhatsApp Business -->
            <div class="pricing-card">
                <h3>WhatsApp Marketing</h3>
                <div class="price">₹0.65<span> / Msg</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Cloud API & Portal Access</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Official Meta Cloud API</li>
                    <li><i class="fa-solid fa-check"></i> Verified Blue/Green Tick Help</li>
                    <li><i class="fa-solid fa-check"></i> Multimedia & Quick Reply Buttons</li>
                </ul>
                <a href="#contact" class="btn-outline" style="display:block; margin-top:20px;">Book Plan</a>
            </div>

            <!-- Bulk Email -->
            <div class="pricing-card">
                <h3>Email Campaigns</h3>
                <div class="price">₹0.04<span> / Email</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Minimum 1 Lakh emails</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> High Inbox Placement</li>
                    <li><i class="fa-solid fa-check"></i> Detailed Click & Open Analytics</li>
                    <li><i class="fa-solid fa-check"></i> Automation & Drip Scheduling</li>
                </ul>
                <a href="#contact" class="btn-outline" style="display:block; margin-top:20px;">Book Plan</a>
            </div>

            <!-- Voice / OBD -->
            <div class="pricing-card">
                <h3>Voice Calls / IVR</h3>
                <div class="price">₹0.28<span> / 30 Sec</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Customized Sound Files</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Automatic Pulse Dialing</li>
                    <li><i class="fa-solid fa-check"></i> User Keypad (DTMF) Capture</li>
                    <li><i class="fa-solid fa-check"></i> Detailed Call Duration Stats</li>
                </ul>
                <a href="#contact" class="btn-outline" style="display:block; margin-top:20px;">Book Plan</a>
            </div>

            <!-- API Suite -->
            <div class="pricing-card">
                <h3>Developer APIs</h3>
                <div class="price">FREE<span> Setup</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;">Pay-as-you-use balance</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> SMS, WhatsApp & Email REST APIs</li>
                    <li><i class="fa-solid fa-check"></i> Webhook Event Listeners</li>
                    <li><i class="fa-solid fa-check"></i> Dedicated Developer Support</li>
                </ul>
                <a href="#contact" class="btn-outline" style="display:block; margin-top:20px;">Get API Key</a>
            </div>
        </div>
    </section>

    <!-- Leadership Section -->
    <section id="leadership">
        <div class="section-header">
            <h4>Corporate Leadership</h4>
            <h2>Meet The Executive Officers</h2>
            <p>Our experienced team ensures seamless operations and transparent client partnerships.</p>
        </div>

        <div class="leadership-wrapper">
            <!-- CEO -->
            <div class="leader-box">
                <div class="leader-avatar"><i class="fa-solid fa-user-tie"></i></div>
                <div>
                    <div class="tag">Chief Executive Officer</div>
                    <h3>Satyam Sharma</h3>
                    <p style="font-size: 0.85rem; color: var(--text-muted);">Leading strategic growth, tech development, and long-term vision at Telecorcel IT Solutions.</p>
                </div>
            </div>

            <!-- Sales Manager -->
            <div class="leader-box">
                <div class="leader-avatar"><i class="fa-solid fa-user-gear"></i></div>
                <div>
                    <div class="tag">Sales Manager</div>
                    <h3>Shivam Sharma</h3>
                    <p style="font-size: 0.85rem; color: var(--text-muted);">Overseeing bulk wholesale campaigns, enterprise accounts, and IT software consultations.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Presence & Regional Locations -->
    <section style="padding-top: 0;">
        <div class="section-header">
            <h4>Physical Locations & Coverage</h4>
            <h2>Registered Office & Regional Support</h2>
            <p>Strategically positioned in Noida's industrial corridors to serve business hubs across NCR.</p>
        </div>

        <div class="locations-box">
            <div class="loc-card">
                <h4><i class="fa-solid fa-building"></i> Registered Head Office</h4>
                <p><strong>Telecorcel IT Solutions Pvt Ltd</strong></p>
                <p>Block A, Industrial Area, Sector 62</p>
                <p>Noida, Uttar Pradesh - 201309, India</p>
            </div>

            <div class="loc-card">
                <h4><i class="fa-solid fa-map-location-dot"></i> Regional Desk: Sector 44</h4>
                <p><strong>Local Enterprise Support Hub</strong></p>
                <p>Dedicated customer service & technical consultation presence serving clients in and around <strong>Sector 44, Noida</strong>.</p>
            </div>

            <div class="loc-card">
                <h4><i class="fa-solid fa-network-wired"></i> Local Operations: Wazidpur</h4>
                <p><strong>Service & Network Coordination</strong></p>
                <p>Operations and rapid on-ground client onboarding unit positioned near <strong>Wazidpur, Noida</strong>.</p>
            </div>
        </div>
    </section>

    <!-- Contact & Consultation Form -->
    <section id="contact" style="padding-top: 0;">
        <div class="contact-layout">
            <div>
                <h4 style="color: var(--primary); text-transform: uppercase; font-size: 0.85rem; letter-spacing: 1px;">Direct Access</h4>
                <h2 style="font-size: 2rem; color: var(--secondary); margin-bottom: 20px;">Ready to Scale Your Communications?</h2>
                <p style="color: var(--text-muted); margin-bottom: 30px;">Reach out to our sales and technical managers for volume rate cards, custom software proposals, or free DLT template support.</p>

                <div style="margin-bottom: 25px;">
                    <strong style="color: var(--secondary);"><i class="fa-solid fa-phone" style="color: var(--primary); margin-right: 8px;"></i> Direct Phone Numbers:</strong>
                    <div style="margin-top: 6px;">
                        <a href="tel:9012574505" style="color: var(--primary); text-decoration: none; font-size: 1.1rem; font-weight: 700; margin-right: 15px;">+91 9012574505</a>
                        <a href="tel:7678519164" style="color: var(--primary); text-decoration: none; font-size: 1.1rem; font-weight: 700;">+91 7678519164</a>
                    </div>
                </div>

                <div style="margin-bottom: 25px;">
                    <strong style="color: var(--secondary);"><i class="fa-solid fa-location-dot" style="color: var(--primary); margin-right: 8px;"></i> Corporate Address:</strong>
                    <p style="color: var(--text-muted); margin-top: 5px;">Block A, Industrial Area, Sector 62, Noida, Uttar Pradesh 201309</p>
                </div>

                <div>
                    <strong style="color: var(--secondary);"><i class="fa-solid fa-clock" style="color: var(--primary); margin-right: 8px;"></i> Operational Timings:</strong>
                    <p style="color: var(--text-muted); margin-top: 5px;">Monday - Saturday: 9:30 AM to 6:30 PM (API & Server Gateway: 24/7)</p>
                </div>
            </div>

            <!-- Interactive Form -->
            <div>
                <form action="#" method="POST" onsubmit="event.preventDefault(); alert('Dhanyawad! Telecorcel Sales Team will call you back within 30 minutes.');">
                    <div class="form-row">
                        <label>Your Full Name / Company Name *</label>
                        <input type="text" required placeholder="e.g. Rahul Sharma / ABC Logistics">
                    </div>

                    <div class="form-row">
                        <label>Phone Number (with WhatsApp) *</label>
                        <input type="tel" required placeholder="+91 XXXXXXXXXX">
                    </div>

                    <div class="form-row">
                        <label>Primary Service Needed *</label>
                        <select required>
                            <option value="">-- Choose Solution --</option>
                            <option value="bulk-sms">Bulk SMS (Transactional / Promotional / OTP)</option>
                            <option value="dlt">DLT Registration & Template Support</option>
                            <option value="whatsapp">WhatsApp Business API</option>
                            <option value="voice">Voice Calls / IVR Solutions</option>
                            <option value="email">Bulk Email Marketing</option>
                            <option value="website">Website / Web App Development</option>
                            <option value="app">Mobile App (Android & iOS)</option>
                            <option value="software">Custom ERP / CRM Software</option>
                            <option value="digital-ads">Google Ads & Performance Lead Gen</option>
                            <option value="apis">Messaging REST APIs</option>
                        </select>
                    </div>

                    <div class="form-row">
                        <label>Requirements or Estimated Volume</label>
                        <textarea rows="3" placeholder="Tell us your requirements, estimated monthly SMS/call volume, or website ideas..."></textarea>
                    </div>

                    <button type="submit" class="btn-cta" style="width: 100%; border: none; cursor: pointer; padding: 14px; font-size: 1rem;">Submit Request to Sales Desk</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div>
                <h3 style="color: var(--white); margin-bottom: 12px; font-size: 1.3rem;">Telecorcel IT Solutions Pvt Ltd</h3>
                <p style="font-size: 0.9rem; line-height: 1.6; margin-bottom: 15px;">Enterprise-grade telecom connectivity and bespoke software architecture tailored for scaling modern Indian businesses.</p>
                <p style="font-size: 0.85rem;"><i class="fa-solid fa-envelope"></i> contact@telecorcel.in</p>
            </div>

            <div>
                <h4>Telecom & Messaging</h4>
                <ul>
                    <li><a href="#telecom">Transactional SMS</a></li>
                    <li><a href="#telecom">Promotional SMS</a></li>
                    <li><a href="#telecom">DLT Support</a></li>
                    <li><a href="#omnichannel">WhatsApp API</a></li>
                    <li><a href="#omnichannel">Bulk Email</a></li>
                    <li><a href="#omnichannel">Voice IVR</a></li>
                </ul>
            </div>

            <div>
                <h4>IT & Digital Growth</h4>
                <ul>
                    <li><a href="#it-solutions">Website Development</a></li>
                    <li><a href="#it-solutions">Android & iOS Apps</a></li>
                    <li><a href="#it-solutions">CRM & ERP Systems</a></li>
                    <li><a href="#digital-growth">Google Ads (PPC)</a></li>
                    <li><a href="#digital-growth">Social Media Marketing</a></li>
                    <li><a href="#digital-growth">Search Engine Optimization</a></li>
                </ul>
            </div>

            <div>
                <h4>Presence & Offices</h4>
                <p style="font-size: 0.85rem; margin-bottom: 10px;"><strong>Corporate Head Office:</strong><br>Block A, Industrial Area, Sector 62, Noida, UP 201309</p>
                <p style="font-size: 0.85rem;"><strong>Regional Presence:</strong><br>Active field service units around Sector 44 and Wazidpur, Noida.</p>
            </div>
        </div>

        <div class="copyright">
            <div>&copy; 2026 Telecorcel IT Solutions Pvt Ltd. All rights reserved.</div>
            <div>Designed for Enterprise Scale & 100% Telecom Compliance</div>
        </div>
    </footer>

</body>
</html>
