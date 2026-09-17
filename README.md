<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telecorcel IT Solutions Pvt Ltd | Enterprise Messaging & Digital Engineering</title>
    
    <!-- Google Fonts & Font Awesome 6 Pro Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --brand-green: #56ba2a;
            --brand-green-dark: #378018;
            --brand-green-light: #edf8e7;
            --brand-glow: rgba(86, 186, 42, 0.35);
            --secondary: #0f172a;
            --dark-surface: #09130d;
            --bg-light: #f8fafc;
            --border: #e2e8f0;
            --text-dark: #0f172a;
            --text-muted: #64748b;
            --white: #ffffff;
            --radius-md: 12px;
            --radius-lg: 20px;
        }

        /* Anti-flicker hardware acceleration */
        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', sans-serif;
            -webkit-font-smoothing: antialiased;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--white);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
            width: 100%;
        }

        /* Top Announcement Header */
        .top-banner {
            background: #060e09;
            color: #d1e7dd;
            padding: 9px 5%;
            font-size: 0.82rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid var(--brand-green);
            position: relative;
            z-index: 20;
        }

        .top-banner .contact-links a {
            color: #ffffff;
            text-decoration: none;
            margin-left: 18px;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: color 0.2s;
        }

        .top-banner .contact-links a:hover {
            color: var(--brand-green);
        }

        /* Header Navbar */
        header {
            position: sticky;
            top: 0;
            z-index: 1100;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border);
            box-shadow: 0 4px 25px rgba(0,0,0,0.03);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .brand-container {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
        }

        .logo-img-wrapper {
            background: #ffffff;
            border-radius: 10px;
            padding: 4px 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid #edf2f7;
            height: 52px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
        }

        .brand-logo-img {
            height: 44px;
            width: auto;
            display: block;
            object-fit: contain;
        }

        .brand-text-block {
            display: flex;
            flex-direction: column;
        }

        .company-name-bold {
            font-size: 1.32rem;
            font-weight: 900;
            color: #0f172a;
            text-transform: uppercase;
            line-height: 1.15;
            letter-spacing: -0.02em;
        }

        .company-name-bold span {
            color: var(--brand-green-dark);
            background: linear-gradient(120deg, #56ba2a, #2f7a14);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .brand-subtitle {
            font-size: 0.72rem;
            font-weight: 700;
            letter-spacing: 2px;
            color: #475569;
            text-transform: uppercase;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 22px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: #334155;
            font-weight: 600;
            font-size: 0.9rem;
            position: relative;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: color 0.25s;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--brand-green);
            transition: width 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .nav-links a:hover {
            color: var(--brand-green-dark);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .btn-cta {
            background: var(--brand-green);
            color: var(--white) !important;
            padding: 10px 22px;
            border-radius: 8px;
            font-weight: 700;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 14px var(--brand-glow);
            transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .btn-cta:hover {
            background: var(--brand-green-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(86, 186, 42, 0.4);
        }

        /* Marquee Ticker */
        .marquee-bar {
            background: #08120b;
            color: #a7f3d0;
            padding: 10px 0;
            overflow: hidden;
            font-size: 0.82rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            white-space: nowrap;
        }

        .marquee-content {
            display: inline-block;
            white-space: nowrap;
            animation: smoothScroll 35s linear infinite;
        }

        @keyframes smoothScroll {
            from { transform: translate3d(0, 0, 0); }
            to { transform: translate3d(-50%, 0, 0); }
        }

        /* ============================================================
           iEnergizer 4D Interactive Canvas & Hero Section
           ============================================================ */
        .hero-4d-container {
            position: relative;
            background: radial-gradient(circle at 50% 30%, #0d2215 0%, #050e08 100%);
            color: var(--white);
            padding: 110px 5% 95px;
            text-align: center;
            overflow: hidden;
            min-height: 680px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Interactive 4D HTML5 Canvas Layer */
        #interactive-4d-canvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            pointer-events: auto;
        }

        /* Ambient 4D Geometric Glow Spheres */
        .ambient-sphere {
            position: absolute;
            border-radius: 50%;
            filter: blur(90px);
            z-index: 2;
            pointer-events: none;
            opacity: 0.45;
            animation: float4D 12s ease-in-out infinite alternate;
        }

        .ambient-sphere.one {
            width: 450px;
            height: 450px;
            background: rgba(86, 186, 42, 0.28);
            top: -100px;
            right: 5%;
        }

        .ambient-sphere.two {
            width: 380px;
            height: 380px;
            background: rgba(16, 185, 129, 0.22);
            bottom: -50px;
            left: 5%;
            animation-delay: -6s;
        }

        @keyframes float4D {
            0% { transform: translate3d(0, 0, 0) scale(1) rotate(0deg); }
            50% { transform: translate3d(30px, -40px, 50px) scale(1.15) rotate(180deg); }
            100% { transform: translate3d(-30px, 30px, -50px) scale(0.9) rotate(360deg); }
        }

        .hero-content {
            position: relative;
            z-index: 5;
            max-width: 1080px;
            margin: 0 auto;
            pointer-events: none;
        }

        .hero-content a, .hero-content button {
            pointer-events: auto;
        }

        .name-banner-dark {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(86, 186, 42, 0.15);
            border: 1px solid rgba(86, 186, 42, 0.4);
            color: #86efac;
            padding: 7px 22px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 800;
            letter-spacing: 1.2px;
            text-transform: uppercase;
            margin-bottom: 24px;
            backdrop-filter: blur(8px);
        }

        .hero-4d-container h1 {
            font-size: 3.5rem;
            line-height: 1.15;
            font-weight: 900;
            color: #ffffff;
            margin-bottom: 24px;
            letter-spacing: -0.03em;
        }

        .hero-4d-container h1 span {
            background: linear-gradient(120deg, #56ba2a, #a3e635);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-4d-container p {
            font-size: 1.2rem;
            color: #cbd5e1;
            max-width: 840px;
            margin: 0 auto 38px;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 50px;
        }

        .btn-outline-glow {
            border: 2px solid rgba(255, 255, 255, 0.25);
            padding: 11px 26px;
            border-radius: 8px;
            color: #ffffff;
            text-decoration: none;
            font-weight: 700;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(8px);
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.25s;
        }

        .btn-outline-glow:hover {
            border-color: var(--brand-green);
            color: #86efac;
            background: rgba(86, 186, 42, 0.15);
        }

        /* Elevation Stats Matrix */
        .stats-grid-4d {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            max-width: 1000px;
            margin: 0 auto;
            padding: 26px;
            background: rgba(13, 27, 18, 0.75);
            backdrop-filter: blur(14px);
            border-radius: var(--radius-lg);
            border: 1px solid rgba(86, 186, 42, 0.25);
            box-shadow: 0 16px 40px rgba(0,0,0,0.3);
        }

        .stat-item-4d i {
            color: var(--brand-green);
            font-size: 1.4rem;
            margin-bottom: 8px;
            display: block;
        }

        .stat-item-4d h3 {
            font-size: 2.1rem;
            font-weight: 900;
            color: #ffffff;
        }

        .stat-item-4d p {
            font-size: 0.85rem;
            color: #94a3b8;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Section Layouts */
        section {
            padding: 85px 5%;
            max-width: 1400px;
            margin: 0 auto;
            position: relative;
        }

        .section-header {
            text-align: center;
            max-width: 820px;
            margin: 0 auto 55px;
        }

        .section-header h4 {
            color: var(--brand-green-dark);
            text-transform: uppercase;
            font-size: 0.85rem;
            font-weight: 800;
            letter-spacing: 1.5px;
            margin-bottom: 8px;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .section-header h2 {
            font-size: 2.3rem;
            color: var(--secondary);
            font-weight: 800;
            letter-spacing: -0.02em;
        }

        .section-header p {
            color: var(--text-muted);
            margin-top: 10px;
            font-size: 1.05rem;
        }

        /* Grid Frameworks & 4D Interactive Tilt Cards */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 28px;
        }

        .card-4d {
            background: var(--white);
            padding: 34px 28px;
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            transition: all 0.35s cubic-bezier(0.2, 0.8, 0.2, 1);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        .card-4d::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, var(--brand-green), #60cf31);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .card-4d:hover {
            transform: translateY(-8px);
            border-color: rgba(86, 186, 42, 0.4);
            box-shadow: 0 16px 36px rgba(15, 23, 42, 0.08);
        }

        .card-4d:hover::before {
            opacity: 1;
        }

        .card-icon {
            width: 58px;
            height: 58px;
            background: var(--brand-green-light);
            color: var(--brand-green-dark);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 14px;
            font-size: 1.6rem;
            margin-bottom: 20px;
            transition: all 0.3s ease;
        }

        .card-4d:hover .card-icon {
            transform: scale(1.08) rotate(3deg);
            background: var(--brand-green);
            color: var(--white);
        }

        .card-4d h3 {
            font-size: 1.3rem;
            margin-bottom: 12px;
            color: var(--secondary);
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .card-4d p {
            color: var(--text-muted);
            font-size: 0.94rem;
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
            font-size: 0.88rem;
            color: #475569;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .bullet-list li i {
            color: var(--brand-green);
            font-size: 0.82rem;
        }

        /* 11 Photos Grid Showcase Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 24px;
        }

        .gallery-card {
            background: var(--white);
            border-radius: var(--radius-md);
            overflow: hidden;
            border: 1px solid var(--border);
            box-shadow: var(--shadow-sm);
            transition: all 0.35s cubic-bezier(0.2, 0.8, 0.2, 1);
            display: flex;
            flex-direction: column;
        }

        .gallery-card:hover {
            transform: translateY(-8px);
            border-color: var(--brand-green);
            box-shadow: 0 18px 36px rgba(15, 23, 42, 0.09);
        }

        .gallery-img-box {
            width: 100%;
            height: 240px;
            background: #f1f5f9;
            position: relative;
            overflow: hidden;
        }

        .gallery-img-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.6s cubic-bezier(0.2, 0.8, 0.2, 1);
        }

        .gallery-card:hover .gallery-img-box img {
            transform: scale(1.08);
        }

        .gallery-caption {
            padding: 18px;
            background: var(--white);
            flex-grow: 1;
        }

        .gallery-caption h4 {
            font-size: 1.05rem;
            color: var(--secondary);
            font-weight: 700;
            margin-bottom: 4px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .gallery-caption p {
            font-size: 0.85rem;
            color: var(--text-muted);
            margin: 0;
        }

        /* Live Workspace Section */
        .workspace-section {
            background: #ffffff;
            border: 1px solid var(--border);
            border-radius: var(--radius-lg);
            overflow: hidden;
            display: grid;
            grid-template-columns: 1.15fr 1fr;
            margin: 40px auto 60px;
            max-width: 1400px;
            box-shadow: 0 10px 30px rgba(15, 23, 42, 0.05);
        }

        .workspace-img-box {
            height: 400px;
            background: #e2e8f0;
            overflow: hidden;
        }

        .workspace-img-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.6s ease;
        }

        .workspace-section:hover .workspace-img-box img {
            transform: scale(1.04);
        }

        .workspace-content {
            padding: 50px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        /* Pricing Section */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 22px;
        }

        .pricing-card {
            background: var(--white);
            border: 1px solid var(--border);
            border-radius: var(--radius-lg);
            padding: 34px 22px;
            text-align: center;
            position: relative;
            transition: all 0.3s ease;
        }

        .pricing-card:hover {
            transform: translateY(-6px);
            border-color: var(--brand-green);
            box-shadow: 0 12px 28px rgba(86, 186, 42, 0.12);
        }

        .pricing-card.featured {
            border: 2px solid var(--brand-green);
            background: #fafdf8;
        }

        .badge-popular {
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--brand-green-dark);
            color: var(--white);
            padding: 4px 14px;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 800;
            text-transform: uppercase;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .pricing-card h3 {
            font-size: 1.25rem;
            color: var(--secondary);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .pricing-card .price {
            font-size: 1.8rem;
            font-weight: 900;
            color: var(--secondary);
            margin-bottom: 12px;
        }

        .pricing-card .price span {
            font-size: 0.85rem;
            color: var(--text-muted);
            font-weight: 500;
        }

        /* Leadership Cards */
        .leadership-wrapper {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
            max-width: 860px;
            margin: 0 auto;
        }

        .leader-box {
            background: var(--white);
            border: 1px solid var(--border);
            border-radius: var(--radius-md);
            padding: 28px;
            display: flex;
            gap: 20px;
            align-items: center;
            transition: all 0.3s ease;
        }

        .leader-box:hover {
            transform: translateY(-5px);
            border-color: var(--brand-green);
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
        }

        .leader-avatar {
            width: 72px;
            height: 72px;
            background: var(--brand-green-light);
            color: var(--brand-green-dark);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.9rem;
            flex-shrink: 0;
            transition: transform 0.3s ease;
        }

        .leader-box:hover .leader-avatar {
            transform: scale(1.06);
        }

        .leader-box h3 {
            font-size: 1.22rem;
            color: var(--secondary);
            margin-bottom: 3px;
        }

        .leader-box .tag {
            color: var(--brand-green-dark);
            font-size: 0.82rem;
            font-weight: 800;
            text-transform: uppercase;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        /* Locations Block */
        .locations-box {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 22px;
        }

        .loc-card {
            background: var(--bg-light);
            border: 1px solid var(--border);
            padding: 26px;
            border-radius: var(--radius-md);
            border-left: 5px solid var(--brand-green);
            transition: all 0.25s ease;
        }

        .loc-card:hover {
            background: #ffffff;
            box-shadow: 0 8px 20px rgba(0,0,0,0.04);
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
            grid-template-columns: 1fr 1.1fr;
            gap: 50px;
            background: #f8fafc;
            border-radius: var(--radius-lg);
            padding: 50px;
            border: 1px solid var(--border);
        }

        .contact-item {
            margin-bottom: 22px;
        }

        .contact-item strong {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.84rem;
            text-transform: uppercase;
            color: var(--brand-green-dark);
            margin-bottom: 6px;
        }

        .contact-item a {
            color: var(--secondary);
            text-decoration: none;
            font-size: 1.15rem;
            font-weight: 800;
        }

        .form-row {
            margin-bottom: 16px;
        }

        .form-row label {
            display: flex;
            align-items: center;
            gap: 6px;
            margin-bottom: 6px;
            font-size: 0.88rem;
            font-weight: 600;
            color: var(--secondary);
        }

        .form-row input, .form-row select, .form-row textarea {
            width: 100%;
            padding: 12px 16px;
            border-radius: 8px;
            border: 1px solid #cbd5e1;
            font-size: 0.94rem;
            background: var(--white);
            transition: all 0.2s ease;
        }

        .form-row input:focus, .form-row select:focus, .form-row textarea:focus {
            outline: none;
            border-color: var(--brand-green);
            box-shadow: 0 0 0 4px var(--brand-glow);
        }

        /* Scroll-Trigger Reveal Animation Classes */
        .reveal-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.7s cubic-bezier(0.16, 1, 0.3, 1), transform 0.7s cubic-bezier(0.16, 1, 0.3, 1);
            will-change: opacity, transform;
        }

        .reveal-on-scroll.is-revealed {
            opacity: 1;
            transform: translateY(0);
        }

        /* Footer */
        footer {
            background: #08110a;
            color: #94a3b8;
            padding: 70px 5% 25px;
            border-top: 2px solid var(--brand-green);
        }

        .footer-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.8fr 1.1fr 1.1fr 1.4fr;
            gap: 40px;
            margin-bottom: 45px;
        }

        .footer-grid h4 {
            color: var(--white);
            margin-bottom: 18px;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-grid ul {
            list-style: none;
        }

        .footer-grid ul li {
            margin-bottom: 9px;
            font-size: 0.88rem;
        }

        .footer-grid ul li a {
            color: #94a3b8;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: color 0.2s;
        }

        .footer-grid ul li a:hover {
            color: var(--brand-green);
        }

        .copyright {
            max-width: 1400px;
            margin: 0 auto;
            padding-top: 25px;
            border-top: 1px solid #1a2a1e;
            font-size: 0.85rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        @media (max-width: 900px) {
            .hero-4d-container h1 { font-size: 2.3rem; }
            .stats-grid-4d { grid-template-columns: repeat(2, 1fr); }
            .workspace-section { grid-template-columns: 1fr; }
            .workspace-img-box { height: 260px; }
            .contact-layout { grid-template-columns: 1fr; padding: 25px; }
            .nav-links { display: none; }
            .footer-grid { grid-template-columns: 1fr; }
            .top-banner { flex-direction: column; gap: 6px; text-align: center; }
            .top-banner .contact-links a { margin: 0 6px; }
        }
    </style>
</head>
<body>

    <!-- Top Announcement Bar -->
    <div class="top-banner">
        <div>
            <i class="fa-solid fa-shield-halved" style="color:var(--brand-green);"></i> Enterprise Telecom & Full-Stack IT Solutions Provider
        </div>
        <div class="contact-links">
            <a href="tel:9012574505"><i class="fa-solid fa-phone"></i> +91 9012574505</a>
            <a href="tel:7678519164"><i class="fa-solid fa-phone-volume"></i> +91 7678519164</a>
            <a href="#contact"><i class="fa-solid fa-headset"></i> Sales Desk</a>
        </div>
    </div>

    <!-- Sticky Header with Logo -->
    <header>
        <nav>
            <a href="#home" class="brand-container">
                <!-- LOGO IMAGE (With Inline Vector Fallback) -->
                <div class="logo-img-wrapper">
                    <img src="logo.png" alt="Telecorcel Logo" class="brand-logo-img" onerror="this.style.display='none'; document.getElementById('svg-fallback').style.display='block';">
                    
                    <svg id="svg-fallback" style="display:none; height:42px; width:56px;" viewBox="0 0 100 80">
                        <path d="M 40,12 C 75,12 90,26 80,48" stroke="#56ba2a" stroke-width="8" stroke-linecap="round" fill="none" />
                        <path d="M 78,48 C 65,72 10,72 10,48 C 10,30 25,18 40,14" stroke="#378018" stroke-width="8" stroke-linecap="round" fill="none" />
                    </svg>
                </div>

                <div class="brand-text-block">
                    <span class="company-name-bold">TELECORCEL <span>IT SOLUTIONS</span></span>
                    <span class="brand-subtitle"><i class="fa-solid fa-circle-check" style="color:var(--brand-green);"></i> PVT LTD &bull; NOIDA</span>
                </div>
            </a>

            <ul class="nav-links">
                <li><a href="#sms-services"><i class="fa-solid fa-comment-sms"></i> Bulk SMS</a></li>
                <li><a href="#omnichannel"><i class="fa-brands fa-whatsapp"></i> WhatsApp & Voice</a></li>
                <li><a href="#gallery"><i class="fa-solid fa-images"></i> Media Showcase</a></li>
                <li><a href="#it-solutions"><i class="fa-solid fa-laptop-code"></i> Software & Web</a></li>
                <li><a href="#pricing"><i class="fa-solid fa-tags"></i> Pricing</a></li>
                <li><a href="#leadership"><i class="fa-solid fa-users"></i> Leadership</a></li>
                <li><a href="#contact" class="btn-cta"><i class="fa-solid fa-paper-plane"></i> Enquire Now</a></li>
            </ul>
        </nav>
    </header>

    <!-- Marquee Ticker -->
    <div class="marquee-bar">
        <div class="marquee-content">
            &bull; TELECORCEL IT SOLUTIONS PVT LTD &bull; Bulk SMS &bull; OTP SMS &bull; Transactional SMS &bull; Promotional SMS &bull; WhatsApp API &bull; Voice SMS &bull; IVR Solutions &bull; Website Development &bull; Mobile Apps &bull; Sector 62 Noida &nbsp;&nbsp;&nbsp;&bull;&nbsp;&nbsp;&nbsp;
            &bull; TELECORCEL IT SOLUTIONS PVT LTD &bull; Bulk SMS &bull; OTP SMS &bull; Transactional SMS &bull; Promotional SMS &bull; WhatsApp API &bull; Voice SMS &bull; IVR Solutions &bull; Website Development &bull; Mobile Apps &bull; Sector 62 Noida &nbsp;&nbsp;&nbsp;&bull;&nbsp;&nbsp;&nbsp;
        </div>
    </div>

    <!-- ============================================================
         iEnergizer-Style 4D Interactive Kinetic Mesh Hero Canvas
         ============================================================ -->
    <div class="hero-4d-container" id="home">
        <!-- Interactive 4D WebGL/Canvas Layer -->
        <canvas id="interactive-4d-canvas"></canvas>
        
        <!-- Ambient Depth Spheres -->
        <div class="ambient-sphere one"></div>
        <div class="ambient-sphere two"></div>

        <div class="hero-content reveal-on-scroll">
            <div class="name-banner-dark">
                <i class="fa-solid fa-atom"></i> Officially Registered: Telecorcel IT Solutions Pvt Ltd
            </div>
            <h1>Empowering Brands with <span>Bulk SMS, Cloud Telephony</span> & Enterprise IT</h1>
            <p>Direct operator connectivity for Transactional SMS, Promotional broadcasts, official WhatsApp API, Cloud IVR, and bespoke mobile application & web engineering.</p>
            
            <div class="hero-buttons">
                <a href="#contact" class="btn-cta" style="padding: 13px 34px; font-size: 1.05rem;"><i class="fa-solid fa-bolt"></i> Connect With Sales</a>
                <a href="#pricing" class="btn-outline-glow"><i class="fa-solid fa-table-list"></i> Explore Wholesale Plans</a>
            </div>

            <div class="stats-grid-4d">
                <div class="stat-item-4d">
                    <i class="fa-solid fa-server"></i>
                    <h3>99.98%</h3>
                    <p>Gateway Uptime</p>
                </div>
                <div class="stat-item-4d">
                    <i class="fa-solid fa-stopwatch-20"></i>
                    <h3>&lt; 5 Sec</h3>
                    <p>Priority OTP Latency</p>
                </div>
                <div class="stat-item-4d">
                    <i class="fa-solid fa-certificate"></i>
                    <h3>100%</h3>
                    <p>TRAI DLT Verified</p>
                </div>
                <div class="stat-item-4d">
                    <i class="fa-solid fa-network-wired"></i>
                    <h3>24/7</h3>
                    <p>Live Monitoring</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Live Workspace Section (telecorcel9.jpeg) -->
    <div class="workspace-section reveal-on-scroll" id="workspace">
        <div class="workspace-img-box">
            <img src="telecorcel9.jpeg" alt="Telecorcel Operations Floor">
        </div>
        <div class="workspace-content">
            <span class="name-banner-dark" style="background: var(--brand-green-light); color: var(--brand-green-dark); border-color: rgba(86,186,42,0.3); max-width: fit-content;">
                <i class="fa-solid fa-building-circle-check"></i> Live Operations Hub
            </span>
            <h2 style="font-size: 2.1rem; color: var(--secondary); margin-bottom: 16px;">Dedicated Floor Support & Technical Desk</h2>
            <p style="color: var(--text-muted); margin-bottom: 22px;">Hamara technical operations floor 24/7 high-volume routes, delivery reports, aur customer technical support ko actively manage karta hai.</p>
            <ul class="bullet-list" style="border:none; padding:0; margin-bottom:24px;">
                <li><i class="fa-solid fa-check-double"></i> Real-time carrier route balancing and failover</li>
                <li><i class="fa-solid fa-check-double"></i> Dedicated client onboarding support</li>
                <li><i class="fa-solid fa-check-double"></i> Corporate Office: Block A, Industrial Area, Sector 62, Noida</li>
            </ul>
            <div>
                <a href="#contact" class="btn-cta"><i class="fa-solid fa-calendar-check"></i> Schedule Consultation</a>
            </div>
        </div>
    </div>

    <!-- All Remaining 9 Campaign Images (Photos 3 to 11) in Gallery -->
    <section id="gallery" style="background: var(--bg-light); border-radius: var(--radius-lg);">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-photo-film"></i> Campaign Media & Operations</h4>
            <h2>Our Verified Campaign Portals & Formats</h2>
            <p>Explore our active campaign creatives, operator routing artworks, and promotional graphics.</p>
        </div>

        <div class="gallery-grid">
            <!-- PHOTO 3: telecorcel11.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel11.jpeg" alt="Campaign Graphic 11">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-layer-group" style="color:var(--brand-green);"></i> Multi-Traffic Campaign Portal</h4>
                    <p>High delivery rates supporting Gaming, Casino, Spa, and Clinic messaging.</p>
                </div>
            </div>

            <!-- PHOTO 4: telecorcel0.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel0.jpeg" alt="Campaign Graphic 0">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-sliders" style="color:var(--brand-green);"></i> Versatile Traffic Solutions</h4>
                    <p>Clean OTP, gaming, and local business promotional broadcasts.</p>
                </div>
            </div>

            <!-- PHOTO 5: telecorcel8.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel8.jpeg" alt="Campaign Graphic 8">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-route" style="color:var(--brand-green);"></i> India Stable SMS Route</h4>
                    <p>MKT/OTP routes with high delivery rates and click analytics.</p>
                </div>
            </div>

            <!-- PHOTO 6: telecorcel7.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel7.jpeg" alt="Campaign Graphic 7">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-mobile-screen-button" style="color:var(--brand-green);"></i> Instant Smartphone Reach</h4>
                    <p>Direct inbox message delivery with zero screen distortion.</p>
                </div>
            </div>

            <!-- PHOTO 7: telecorcel6.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel6.jpeg" alt="Campaign Graphic 6">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-network-wired" style="color:var(--brand-green);"></i> Operator-Grade Gateway</h4>
                    <p>High-concurrency carrier connectivity for fast delivery.</p>
                </div>
            </div>

            <!-- PHOTO 8: telecorcel5.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel5.jpeg" alt="Campaign Graphic 5">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-chart-line" style="color:var(--brand-green);"></i> SMS Marketing Made Easy</h4>
                    <p>Instant delivery with DND and Non-DND sender ID support.</p>
                </div>
            </div>

            <!-- PHOTO 9: telecorcel4.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel4.jpeg" alt="Campaign Graphic 4">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-key" style="color:var(--brand-green);"></i> India OTP Clean Route</h4>
                    <p>Stable dynamic 2FA authentication for apps and banking portals.</p>
                </div>
            </div>

            <!-- PHOTO 10: telecorcel3.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel3.jpeg" alt="Campaign Graphic 3">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-arrow-trend-up" style="color:var(--brand-green);"></i> Sales Conversion Engine</h4>
                    <p>Direct SMS routes designed to accelerate customer response rates.</p>
                </div>
            </div>

            <!-- PHOTO 11: telecorcel2.jpeg -->
            <div class="gallery-card reveal-on-scroll">
                <div class="gallery-img-box">
                    <img src="telecorcel2.jpeg" alt="Campaign Graphic 2">
                </div>
                <div class="gallery-caption">
                    <h4><i class="fa-solid fa-cloud" style="color:var(--brand-green);"></i> Enterprise Gateway Network</h4>
                    <p>High-throughput architecture for scalable enterprise communications.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Bulk SMS & Communication Routing -->
    <section id="sms-services">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-tower-broadcast"></i> Direct Telecom Gateway</h4>
            <h2>Enterprise Bulk SMS & DLT Solutions</h2>
            <p>Engineered for high-volume deliverability across transactional, promotional, and automated notifications.</p>
        </div>

        <div class="grid-3">
            <div class="card-4d reveal-on-scroll">
                <div class="card-icon"><i class="fa-solid fa-shield-halved"></i></div>
                <h3><i class="fa-solid fa-lock" style="font-size:1rem; color:var(--brand-green);"></i> Transactional & OTP SMS</h3>
                <p>Prioritized carrier band for critical OTPs, two-factor authentication, security alerts, and order updates.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Round-the-clock 24/7 Open Bandwidth</li>
                    <li><i class="fa-solid fa-check"></i> Automated Carrier Failover & Retries</li>
                    <li><i class="fa-solid fa-check"></i> Sub-5 Second Delivery Latency</li>
                </ul>
            </div>

            <div class="card-4d reveal-on-scroll">
                <div class="card-icon"><i class="fa-solid fa-bullhorn"></i></div>
                <h3><i class="fa-solid fa-bullseye" style="font-size:1rem; color:var(--brand-green);"></i> Promotional & Flash SMS</h3>
                <p>Scalable customer outreach for sales offers, announcements, and immediate pop-up Flash SMS alerts on phone screens.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Standard Delivery Window (10 AM - 9 PM)</li>
                    <li><i class="fa-solid fa-check"></i> Direct Screen Popup Flash SMS</li>
                    <li><i class="fa-solid fa-check"></i> Smart DND Scrubbing & Reporting</li>
                </ul>
            </div>

            <div class="card-4d reveal-on-scroll">
                <div class="card-icon"><i class="fa-solid fa-file-signature"></i></div>
                <h3><i class="fa-solid fa-stamp" style="font-size:1rem; color:var(--brand-green);"></i> DLT Registration Support</h3>
                <p>Complete entity registration, header whitelisting, and content template approvals across Jio, Airtel, VI, and BSNL.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Entity & Sender ID (Header) Approval</li>
                    <li><i class="fa-solid fa-check"></i> Content Template Submissions</li>
                    <li><i class="fa-solid fa-check"></i> TRAI Regulatory Compliance</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Omnichannel: WhatsApp, Voice IVR & Email -->
    <section id="omnichannel" style="background: var(--bg-light); border-radius: var(--radius-lg);">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-arrows-split-up-and-left"></i> Omnichannel Communication</h4>
            <h2>WhatsApp Business, Cloud Voice IVR & Email</h2>
            <p>Reach your customers on high-engagement touchpoints with automated workflows.</p>
        </div>

        <div class="grid-3">
            <div class="card-4d reveal-on-scroll">
                <div class="card-icon" style="color: #25d366; background: #e8fbee;"><i class="fa-brands fa-whatsapp"></i></div>
                <h3><i class="fa-solid fa-message" style="font-size:1rem; color:#25d366;"></i> WhatsApp Business API</h3>
                <p>Official Meta Cloud API integration, verified badge assistance, chatbot flows, and broadcast marketing.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Automated Chatbot Workflows</li>
                    <li><i class="fa-solid fa-check"></i> Interactive Quick Reply Buttons</li>
                    <li><i class="fa-solid fa-check"></i> Dynamic PDF Invoice Alerts</li>
                </ul>
            </div>

            <div class="card-4d reveal-on-scroll">
                <div class="card-icon" style="color: #8b5cf6; background: #f3f0ff;"><i class="fa-solid fa-headset"></i></div>
                <h3><i class="fa-solid fa-phone-volume" style="font-size:1rem; color:#8b5cf6;"></i> Voice Calls & IVR</h3>
                <p>Automate outbound voice broadcasts (OBD), customer reminders, and intelligent multi-level IVR inbound calling trees.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> High Concurrency Voice Channels</li>
                    <li><i class="fa-solid fa-check"></i> User Keypad (DTMF) Capture</li>
                    <li><i class="fa-solid fa-check"></i> Exact Duration Analytics</li>
                </ul>
            </div>

            <div class="card-4d reveal-on-scroll">
                <div class="card-icon" style="color: #ea4335; background: #fdf2f2;"><i class="fa-solid fa-envelope-open-text"></i></div>
                <h3><i class="fa-solid fa-envelope" style="font-size:1rem; color:#ea4335;"></i> Bulk Email Marketing</h3>
                <p>High inbox placement rates through dedicated IP pools, drip automations, and transactional email gateways.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Real-time Open & Click Tracking</li>
                    <li><i class="fa-solid fa-check"></i> Automated Drip Schedules</li>
                    <li><i class="fa-solid fa-check"></i> SPF, DKIM & DMARC Setup</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- IT Engineering, Web & Mobile App Development -->
    <section id="it-solutions">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-microchip"></i> Full-Stack Software Architecture</h4>
            <h2>Custom Web, Mobile App & SaaS Engineering</h2>
            <p>Engineered with modern cloud frameworks to deliver fast, secure, and conversion-optimized digital platforms.</p>
        </div>

        <div class="grid-3">
            <div class="card-4d reveal-on-scroll">
                <div class="card-icon"><i class="fa-solid fa-laptop-code"></i></div>
                <h3><i class="fa-solid fa-globe" style="font-size:1rem; color:var(--brand-green);"></i> Corporate Web & Portals</h3>
                <p>Performance-driven, responsive, and SEO-optimized business websites, landing pages, and e-commerce web applications.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Corporate Websites & Landing Pages</li>
                    <li><i class="fa-solid fa-check"></i> E-commerce Gateways & Shopping Carts</li>
                    <li><i class="fa-solid fa-check"></i> SSL Security & Cloud Hosting</li>
                </ul>
            </div>

            <div class="card-4d reveal-on-scroll">
                <div class="card-icon"><i class="fa-solid fa-mobile-screen"></i></div>
                <h3><i class="fa-brands fa-android" style="font-size:1rem; color:var(--brand-green);"></i> Mobile App Development</h3>
                <p>High-speed, feature-packed mobile applications developed for Android and iOS devices using native and cross-platform frameworks.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Android & iOS Mobile Applications</li>
                    <li><i class="fa-solid fa-check"></i> Service Booking & Delivery Apps</li>
                    <li><i class="fa-solid fa-check"></i> Play Store & App Store Deployment</li>
                </ul>
            </div>

            <div class="card-4d reveal-on-scroll">
                <div class="card-icon"><i class="fa-solid fa-cubes"></i></div>
                <h3><i class="fa-solid fa-gears" style="font-size:1rem; color:var(--brand-green);"></i> Custom CRM, ERP & SaaS</h3>
                <p>Automate internal administration with custom dashboards, CRM pipelines, inventory managers, and billing systems.</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Custom Admin Panels & CRM Suites</li>
                    <li><i class="fa-solid fa-check"></i> Automated Billing & Invoicing Systems</li>
                    <li><i class="fa-solid fa-check"></i> REST API Engineering & Integrations</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" style="background: var(--bg-light); border-radius: var(--radius-lg);">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-circle-dollar-to-slot"></i> Transparent Wholesale Rates</h4>
            <h2>Competitive Pricing Cards</h2>
            <p>Wholesale volume pricing with zero hidden maintenance charges. Contact sales for custom slab discounts.</p>
        </div>

        <div class="pricing-grid">
            <div class="pricing-card reveal-on-scroll">
                <h3><i class="fa-solid fa-paper-plane" style="color:var(--brand-green);"></i> Promotional SMS</h3>
                <div class="price">₹0.15<span> / SMS</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;"><i class="fa-solid fa-cubes-stacked"></i> Volume: Min 50k Credits</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Standard Hours (10 AM - 9 PM)</li>
                    <li><i class="fa-solid fa-check"></i> 100% Delivery Reports</li>
                    <li><i class="fa-solid fa-check"></i> Free DLT Template Setup</li>
                </ul>
                <a href="#contact" class="btn-outline-glow" style="display:inline-flex; justify-content:center; width:100%; color:var(--secondary); border-color:#cbd5e1; margin-top:20px;"><i class="fa-solid fa-cart-plus"></i> Book Plan</a>
            </div>

            <div class="pricing-card featured reveal-on-scroll">
                <span class="badge-popular"><i class="fa-solid fa-fire"></i> Highest Demand</span>
                <h3><i class="fa-solid fa-key" style="color:var(--brand-green);"></i> Transactional / OTP</h3>
                <div class="price">₹0.18<span> / SMS</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;"><i class="fa-solid fa-cubes-stacked"></i> Volume: Min 25k Credits</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Direct Carrier Priority Band</li>
                    <li><i class="fa-solid fa-check"></i> 24/7 Delivery Under 5 Sec</li>
                    <li><i class="fa-solid fa-check"></i> 99.9% Delivery Guarantee</li>
                </ul>
                <a href="#contact" class="btn-cta" style="display:inline-flex; justify-content:center; width:100%; margin-top:20px;"><i class="fa-solid fa-bolt"></i> Get Started</a>
            </div>

            <div class="pricing-card reveal-on-scroll">
                <h3><i class="fa-brands fa-whatsapp" style="color:#25d366;"></i> WhatsApp Marketing</h3>
                <div class="price">₹0.65<span> / Msg</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;"><i class="fa-solid fa-cloud"></i> Meta Cloud API Access</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Official Meta Cloud API</li>
                    <li><i class="fa-solid fa-check"></i> Verified Blue/Green Tick Help</li>
                    <li><i class="fa-solid fa-check"></i> Multimedia & Buttons</li>
                </ul>
                <a href="#contact" class="btn-outline-glow" style="display:inline-flex; justify-content:center; width:100%; color:var(--secondary); border-color:#cbd5e1; margin-top:20px;"><i class="fa-solid fa-cart-plus"></i> Book Plan</a>
            </div>

            <div class="pricing-card reveal-on-scroll">
                <h3><i class="fa-solid fa-phone-volume" style="color:#8b5cf6;"></i> Voice Calls & IVR</h3>
                <div class="price">₹0.28<span> / 30 Sec</span></div>
                <p style="color: var(--text-muted); font-size: 0.85rem;"><i class="fa-solid fa-tower-cell"></i> High Concurrency Channels</p>
                <ul class="bullet-list">
                    <li><i class="fa-solid fa-check"></i> Automatic Dialing Engine</li>
                    <li><i class="fa-solid fa-check"></i> Keypad (DTMF) Response</li>
                    <li><i class="fa-solid fa-check"></i> Exact Duration Stats</li>
                </ul>
                <a href="#contact" class="btn-outline-glow" style="display:inline-flex; justify-content:center; width:100%; color:var(--secondary); border-color:#cbd5e1; margin-top:20px;"><i class="fa-solid fa-cart-plus"></i> Book Plan</a>
            </div>
        </div>
    </section>

    <!-- Leadership Section -->
    <section id="leadership">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-user-shield"></i> Corporate Leadership</h4>
            <h2>Meet The Executive Management</h2>
            <p>Guiding operations, enterprise sales, and technical excellence at Telecorcel IT Solutions Pvt Ltd.</p>
        </div>

        <div class="leadership-wrapper">
            <div class="leader-box reveal-on-scroll">
                <div class="leader-avatar"><i class="fa-solid fa-user-tie"></i></div>
                <div>
                    <div class="tag"><i class="fa-solid fa-award"></i> Chief Executive Officer</div>
                    <h3>Satyam Sharma</h3>
                    <p style="font-size: 0.88rem; color: var(--text-muted);">Spearheading company strategy, carrier partnerships, and technical innovation at Telecorcel IT Solutions Pvt Ltd.</p>
                </div>
            </div>

            <div class="leader-box reveal-on-scroll">
                <div class="leader-avatar"><i class="fa-solid fa-user-gear"></i></div>
                <div>
                    <div class="tag"><i class="fa-solid fa-briefcase"></i> Sales Manager</div>
                    <h3>Shivam Sharma</h3>
                    <p style="font-size: 0.88rem; color: var(--text-muted);">Overseeing bulk messaging volume contracts, enterprise client onboarding, and software proposals.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Physical Presence & Local Listings -->
    <section style="padding-top: 0;">
        <div class="section-header reveal-on-scroll">
            <h4><i class="fa-solid fa-location-dot"></i> Infrastructure & Locations</h4>
            <h2>Registered Office & Regional Support</h2>
            <p>Headquartered in Noida's central IT corridor with localized support coverage.</p>
        </div>

        <div class="locations-box">
            <div class="loc-card reveal-on-scroll">
                <h4><i class="fa-solid fa-building" style="color: var(--brand-green-dark);"></i> Registered Corporate Office</h4>
                <p><strong>Telecorcel IT Solutions Pvt Ltd</strong></p>
                <p><i class="fa-solid fa-map-pin" style="color:var(--brand-green);"></i> Block A, Industrial Area, Sector 62</p>
                <p>Noida, Uttar Pradesh – 201309, India</p>
            </div>

            <div class="loc-card reveal-on-scroll">
                <h4><i class="fa-solid fa-map-location-dot" style="color: var(--brand-green-dark);"></i> Regional Hub: Sector 44</h4>
                <p><strong>Dedicated Enterprise Support</strong></p>
                <p><i class="fa-solid fa-city" style="color:var(--brand-green);"></i> Client onboarding, quick issue resolution, and consultation unit catering to corporate clusters around <strong>Sector 44, Noida</strong>.</p>
            </div>

            <div class="loc-card reveal-on-scroll">
                <h4><i class="fa-solid fa-network-wired" style="color: var(--brand-green-dark);"></i> Local Field Unit: Wazidpur</h4>
                <p><strong>Service & Network Operations</strong></p>
                <p><i class="fa-solid fa-tower-cell" style="color:var(--brand-green);"></i> Regional team stationed to coordinate direct accounts and merchant activations near <strong>Wazidpur, Noida</strong>.</p>
            </div>
        </div>
    </section>

    <!-- Contact & Consultation Form -->
    <section id="contact" style="padding-top: 0;">
        <div class="contact-layout reveal-on-scroll">
            <div>
                <h4 style="color: var(--brand-green-dark); text-transform: uppercase; font-size: 0.85rem; letter-spacing: 1px;"><i class="fa-solid fa-address-book"></i> Direct Access</h4>
                <h2 style="font-size: 2.1rem; color: var(--secondary); margin-bottom: 20px;">Get in Touch With Telecorcel Sales</h2>
                <p style="color: var(--text-muted); margin-bottom: 30px;">Reach out directly to our sales leadership to discuss volume rate cards, custom software proposals, or DLT template compliance.</p>

                <div class="contact-item">
                    <strong><i class="fa-solid fa-phone" style="color:var(--brand-green);"></i> Direct Helplines:</strong>
                    <a href="tel:9012574505">+91 9012574505</a> &nbsp;|&nbsp; 
                    <a href="tel:7678519164">+91 7678519164</a>
                </div>

                <div class="contact-item">
                    <strong><i class="fa-solid fa-map-location" style="color:var(--brand-green);"></i> Corporate Registered Address:</strong>
                    <p style="color: var(--text-dark); font-weight: 600;">Block A, Industrial Area, Sector 62, Noida, Uttar Pradesh 201309</p>
                </div>

                <div class="contact-item">
                    <strong><i class="fa-solid fa-compass" style="color:var(--brand-green);"></i> Local Presence & Regional Coverage:</strong>
                    <p style="color: var(--text-muted);">Serving businesses across Sector 44, Wazidpur, Noida and NCR Region.</p>
                </div>

                <div class="contact-item">
                    <strong><i class="fa-solid fa-clock" style="color:var(--brand-green);"></i> Operating Hours:</strong>
                    <p style="color: var(--text-muted);">Monday – Saturday: 9:30 AM to 6:30 PM (Telecom Gateway: 24/7)</p>
                </div>
            </div>

            <!-- Form -->
            <div>
                <form action="#" method="POST" onsubmit="event.preventDefault(); alert('Dhanyawad! Telecorcel team will connect with you shortly.');">
                    <div class="form-row">
                        <label><i class="fa-solid fa-user"></i> Your Name / Company Name *</label>
                        <input type="text" required placeholder="Enter full name or firm name">
                    </div>

                    <div class="form-row">
                        <label><i class="fa-solid fa-phone"></i> Phone Number *</label>
                        <input type="tel" required placeholder="+91 XXXXXXXXXX">
                    </div>

                    <div class="form-row">
                        <label><i class="fa-solid fa-list-check"></i> Service Needed *</label>
                        <select required>
                            <option value="">-- Choose Solution --</option>
                            <option value="bulk-sms">Bulk SMS (Transactional / Promotional / OTP)</option>
                            <option value="dlt">DLT Registration & Templates</option>
                            <option value="whatsapp">WhatsApp Business API</option>
                            <option value="voice">Voice Calls & Cloud IVR</option>
                            <option value="website">Website / Web App Development</option>
                            <option value="app">Mobile App (Android & iOS)</option>
                            <option value="software">Custom ERP / CRM Software</option>
                        </select>
                    </div>

                    <div class="form-row">
                        <label><i class="fa-solid fa-message"></i> Requirements or Estimated Volume</label>
                        <textarea rows="3" placeholder="Tell us your monthly message volume or project details..."></textarea>
                    </div>

                    <button type="submit" class="btn-cta" style="width: 100%; border: none; cursor: pointer; padding: 14px; font-size: 1rem; justify-content:center;"><i class="fa-solid fa-paper-plane"></i> Submit Request to Sales Desk</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div>
                <div style="display:flex; align-items:center; gap:10px; margin-bottom:15px;">
                    <div style="background:#fff; padding:4px 8px; border-radius:6px; display:flex; align-items:center;">
                        <img src="logo.png" alt="Telecorcel Logo" style="height:32px;">
                    </div>
                    <h3 style="color: var(--white); font-size: 1.15rem; font-weight:800;">TELECORCEL IT SOLUTIONS</h3>
                </div>
                <p style="font-size: 0.88rem; line-height: 1.6; margin-bottom: 15px;">Official enterprise provider of Bulk SMS, WhatsApp Business API, Cloud IVR, and custom full-stack software development.</p>
                <p style="font-size: 0.85rem;"><i class="fa-solid fa-phone" style="color:var(--brand-green);"></i> +91 9012574505 / +91 7678519164</p>
            </div>

            <div>
                <h4><i class="fa-solid fa-comments"></i> Telecom Solutions</h4>
                <ul>
                    <li><a href="#sms-services"><i class="fa-solid fa-angle-right"></i> Transactional SMS</a></li>
                    <li><a href="#sms-services"><i class="fa-solid fa-angle-right"></i> Promotional SMS</a></li>
                    <li><a href="#sms-services"><i class="fa-solid fa-angle-right"></i> OTP & Flash SMS</a></li>
                    <li><a href="#sms-services"><i class="fa-solid fa-angle-right"></i> DLT Registration</a></li>
                    <li><a href="#omnichannel"><i class="fa-solid fa-angle-right"></i> WhatsApp API</a></li>
                    <li><a href="#omnichannel"><i class="fa-solid fa-angle-right"></i> Voice & IVR</a></li>
                </ul>
            </div>

            <div>
                <h4><i class="fa-solid fa-code"></i> IT Engineering</h4>
                <ul>
                    <li><a href="#it-solutions"><i class="fa-solid fa-angle-right"></i> Corporate Websites</a></li>
                    <li><a href="#it-solutions"><i class="fa-solid fa-angle-right"></i> Android & iOS Apps</a></li>
                    <li><a href="#it-solutions"><i class="fa-solid fa-angle-right"></i> Custom CRM & ERP</a></li>
                    <li><a href="#it-solutions"><i class="fa-solid fa-angle-right"></i> Landing Pages</a></li>
                    <li><a href="#it-solutions"><i class="fa-solid fa-angle-right"></i> Billing Software</a></li>
                </ul>
            </div>

            <div>
                <h4><i class="fa-solid fa-building-flag"></i> Corporate Presence</h4>
                <p style="font-size: 0.85rem; margin-bottom: 8px;"><strong>Head Office:</strong><br><i class="fa-solid fa-location-dot" style="color:var(--brand-green);"></i> Block A, Industrial Area, Sector 62, Noida, UP 201309</p>
                <p style="font-size: 0.85rem;"><strong>Regional Presence:</strong><br><i class="fa-solid fa-map-pin" style="color:var(--brand-green);"></i> Sector 44 & Wazidpur, Noida</p>
            </div>
        </div>

        <div class="copyright">
            <div>&copy; 2026 <strong>Telecorcel IT Solutions Pvt Ltd</strong>. All rights reserved.</div>
            <div style="color: var(--brand-green); font-weight: 600;"><i class="fa-solid fa-circle-check"></i> Sector 62, Noida, Uttar Pradesh 201309</div>
        </div>
    </footer>

    <!-- ============================================================
         iEnergizer-Style 4D Interactive Particle Engine (Zero Lag)
         ============================================================ -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const canvas = document.getElementById('interactive-4d-canvas');
            const ctx = canvas.getContext('2d');
            let width, height;
            let particles = [];

            // Mouse tracking coordinates for 4D dynamic depth interaction
            const mouse = {
                x: null,
                y: null,
                radius: 160
            };

            window.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                mouse.x = e.clientX - rect.left;
                mouse.y = e.clientY - rect.top;
            });

            window.addEventListener('mouseleave', () => {
                mouse.x = null;
                mouse.y = null;
            });

            function resize() {
                width = canvas.width = canvas.parentElement.offsetWidth;
                height = canvas.height = canvas.parentElement.offsetHeight;
                initParticles();
            }

            class Particle4D {
                constructor() {
                    this.x = Math.random() * width;
                    this.y = Math.random() * height;
                    this.z = Math.random() * 2 + 0.5; // 3D/4D depth layer
                    this.vx = (Math.random() - 0.5) * 0.9 * this.z;
                    this.vy = (Math.random() - 0.5) * 0.9 * this.z;
                    this.baseRadius = (Math.random() * 2 + 1) * this.z;
                    this.radius = this.baseRadius;
                    this.color = this.z > 1.5 ? 'rgba(134, 239, 172, ' : 'rgba(86, 186, 42, ';
                }

                update() {
                    this.x += this.vx;
                    this.y += this.vy;

                    // Screen boundary reflection
                    if (this.x < 0 || this.x > width) this.vx *= -1;
                    if (this.y < 0 || this.y > height) this.vy *= -1;

                    // Dynamic 4D Mouse Gravitational Wave
                    if (mouse.x !== null && mouse.y !== null) {
                        const dx = mouse.x - this.x;
                        const dy = mouse.y - this.y;
                        const dist = Math.sqrt(dx * dx + dy * dy);

                        if (dist < mouse.radius) {
                            const force = (mouse.radius - dist) / mouse.radius;
                            const angle = Math.atan2(dy, dx);
                            this.x -= Math.cos(angle) * force * 4.5 * this.z;
                            this.y -= Math.sin(angle) * force * 4.5 * this.z;
                            this.radius = this.baseRadius * (1 + force * 1.2);
                        } else {
                            this.radius = this.baseRadius;
                        }
                    }
                }

                draw() {
                    ctx.beginPath();
                    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                    ctx.fillStyle = this.color + (0.35 * this.z) + ')';
                    ctx.shadowBlur = 10;
                    ctx.shadowColor = '#56ba2a';
                    ctx.fill();
                    ctx.shadowBlur = 0;
                }
            }

            function initParticles() {
                particles = [];
                // Density calculation based on screen width
                const count = Math.floor((width * height) / 10000);
                for (let i = 0; i < count; i++) {
                    particles.push(new Particle4D());
                }
            }

            function renderLines() {
                for (let i = 0; i < particles.length; i++) {
                    for (let j = i + 1; j < particles.length; j++) {
                        const dx = particles[i].x - particles[j].x;
                        const dy = particles[i].y - particles[j].y;
                        const dist = Math.sqrt(dx * dx + dy * dy);

                        if (dist < 115) {
                            const alpha = (1 - dist / 115) * 0.22;
                            ctx.beginPath();
                            ctx.moveTo(particles[i].x, particles[i].y);
                            ctx.lineTo(particles[j].x, particles[j].y);
                            ctx.strokeStyle = `rgba(86, 186, 42, ${alpha})`;
                            ctx.lineWidth = 0.8;
                            ctx.stroke();
                        }
                    }
                }
            }

            function animate() {
                ctx.clearRect(0, 0, width, height);
                for (let i = 0; i < particles.length; i++) {
                    particles[i].update();
                    particles[i].draw();
                }
                renderLines();
                requestAnimationFrame(animate);
            }

            window.addEventListener('resize', resize);
            resize();
            animate();

            // Scroll Reveal Activation
            const revealElements = document.querySelectorAll('.reveal-on-scroll');
            const revealObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('is-revealed');
                        observer.unobserve(entry.target);
                    }
                });
            }, {
                threshold: 0.12,
                rootMargin: "0px 0px -40px 0px"
            });
            revealElements.forEach(el => revealObserver.observe(el));
        });
    </script>
</body>
</html>
