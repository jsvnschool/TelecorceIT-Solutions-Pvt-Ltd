<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>J.S. Vidya Niketan - Residential School, Aliganj</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&family=Orbitron:wght@600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #8b0000;
            --secondary: #d4a373;
            --accent: #e65100;
            --dark: #1f2421;
            --light: #f8f9fa;
            --white: #ffffff;
            --boss-gold: #ffd700;
            --neon-blue: #00f2fe;
            --neon-glow: rgba(0, 242, 254, 0.45);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: #f4f6f9;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Top Bar */
        .top-bar {
            background-color: var(--primary);
            color: var(--white);
            padding: 8px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.88rem;
            flex-wrap: wrap;
        }
        .top-bar a {
            color: #ffeb3b;
            text-decoration: none;
            margin-left: 15px;
            font-weight: 600;
        }

        /* Navbar */
        header {
            background: var(--white);
            box-shadow: 0 4px 10px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 5%;
        }
        .logo-box {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .school-crest {
            background: var(--primary);
            color: #ffeb3b;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-size: 1.6rem;
            border: 2px solid var(--secondary);
        }
        .logo-box h1 {
            font-size: 1.35rem;
            color: var(--primary);
            font-weight: 700;
            text-transform: uppercase;
        }
        .logo-box p {
            font-size: 0.78rem;
            color: #666;
            font-weight: 600;
        }
        nav ul {
            display: flex;
            list-style: none;
            gap: 18px;
            align-items: center;
        }
        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-size: 0.92rem;
            transition: color 0.3s;
        }
        nav a:hover {
            color: var(--primary);
        }
        .btn-apply-nav {
            background: #2e7d32;
            color: white !important;
            padding: 8px 16px;
            border-radius: 20px;
            font-weight: bold;
        }
        .btn-admin-nav {
            background: linear-gradient(135deg, #111, #8b0000);
            color: #ffd700 !important;
            border: 1px solid #ffd700;
            padding: 8px 16px;
            border-radius: 20px;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
        }

        /* Hero */
        .hero {
            background: linear-gradient(rgba(139, 0, 0, 0.75), rgba(31, 36, 33, 0.88)), url('https://images.unsplash.com/photo-1580582932707-520aed937b7b?auto=format&fit=crop&w=1200&q=80') center/cover no-repeat;
            color: white;
            text-align: center;
            padding: 85px 20px;
        }
        .hero h2 {
            font-size: 2.6rem;
            font-weight: 700;
            margin-bottom: 12px;
            color: #ffe082;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 25px;
        }
        .badge-tag {
            background: var(--accent);
            color: white;
            padding: 6px 18px;
            border-radius: 30px;
            display: inline-block;
            font-weight: bold;
            text-transform: uppercase;
            margin-bottom: 15px;
        }

        /* Marquee Alert */
        .alert-ticker {
            background: #ffecb3;
            color: #b71c1c;
            padding: 10px 5%;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 15px;
            border-bottom: 2px solid #ffe082;
        }
        .alert-ticker span {
            background: var(--primary);
            color: white;
            padding: 2px 10px;
            border-radius: 4px;
            font-size: 0.8rem;
            white-space: nowrap;
        }

        /* Section Layouts */
        .section {
            padding: 55px 5%;
        }
        .section-title {
            text-align: center;
            margin-bottom: 40px;
        }
        .section-title h3 {
            font-size: 2rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        .section-title h3::after {
            content: '';
            width: 50%;
            height: 3px;
            background: var(--accent);
            position: absolute;
            bottom: 0;
            left: 25%;
        }

        /* Features */
        .grid-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
        }
        .card {
            background: white;
            border-radius: 10px;
            padding: 28px 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.06);
            border-top: 4px solid var(--primary);
            text-align: center;
            transition: transform 0.3s;
        }
        .card:hover {
            transform: translateY(-6px);
        }
        .card i {
            font-size: 2.3rem;
            color: var(--accent);
            margin-bottom: 12px;
        }
        .card h4 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--dark);
        }

        /* Admission Form Box */
        .admission-container {
            background: white;
            max-width: 850px;
            margin: 0 auto;
            border-radius: 12px;
            padding: 35px;
            box-shadow: 0 5px 25px rgba(0,0,0,0.08);
            border: 2px solid #eee;
        }
        .form-row {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            margin-bottom: 15px;
        }
        .form-group {
            flex: 1;
            min-width: 240px;
        }
        .form-group label {
            display: block;
            font-size: 0.88rem;
            font-weight: 600;
            margin-bottom: 6px;
        }
        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 0.95rem;
        }
        .btn-submit {
            background: var(--primary);
            color: white;
            padding: 12px 28px;
            border: none;
            border-radius: 6px;
            font-size: 1rem;
            cursor: pointer;
            font-weight: 600;
            transition: 0.3s;
        }
        .btn-submit:hover {
            background: #6d0000;
        }

        /* Admin Modal Base */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.85);
            backdrop-filter: blur(10px);
            z-index: 2000;
            overflow-y: auto;
            justify-content: center;
            align-items: center;
            padding: 20px;
            perspective: 1200px;
        }
        .modal-content {
            background: #ffffff;
            border-radius: 16px;
            max-width: 950px;
            width: 100%;
            padding: 30px;
            position: relative;
            box-shadow: 0 20px 60px rgba(0,0,0,0.5);
            transition: all 0.4s ease;
        }
        .close-btn {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 2rem;
            cursor: pointer;
            color: #666;
            z-index: 10;
        }

        /* 4D HOLOGRAM LOGIN STYLING */
        .boss-login-card {
            text-align: center;
            padding: 30px 15px;
            position: relative;
        }
        .hologram-stage-4d {
            width: 180px;
            height: 180px;
            margin: 0 auto 20px;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            transform-style: preserve-3d;
            perspective: 800px;
        }
        .hologram-ring {
            position: absolute;
            width: 170px;
            height: 170px;
            border-radius: 50%;
            border: 2px dashed #00f2fe;
            box-shadow: 0 0 25px #00f2fe, inset 0 0 25px #00f2fe;
            animation: rotateHolo 8s linear infinite;
        }
        .hologram-avatar {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            background: linear-gradient(135deg, #111, #4a0000);
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 30px rgba(0, 242, 254, 0.4);
            border: 3px solid #ffd700;
            z-index: 2;
            animation: float4D 3.5s ease-in-out infinite;
        }
        .hologram-avatar img {
            width: 105px;
            height: 105px;
            border-radius: 50%;
            object-fit: cover;
        }
        @keyframes rotateHolo {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        @keyframes float4D {
            0%, 100% { transform: translateY(0px) rotateY(0deg); }
            50% { transform: translateY(-10px) rotateY(12deg); }
        }

        /* 4D WELCOME POPUP MODAL (LADKI AA KE BOLEGI) */
        #boss4DGreetingOverlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(5, 8, 15, 0.94);
            backdrop-filter: blur(15px);
            z-index: 3000;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        .box-4d-character {
            position: relative;
            background: radial-gradient(circle, rgba(139, 0, 0, 0.45) 0%, rgba(0, 0, 0, 0.9) 80%);
            border: 2px solid #00f2fe;
            box-shadow: 0 0 50px rgba(0, 242, 254, 0.6), inset 0 0 35px rgba(255, 215, 0, 0.2);
            border-radius: 25px;
            padding: 40px 30px;
            max-width: 550px;
            width: 90%;
            animation: zoom4D 0.7s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        @keyframes zoom4D {
            0% { transform: scale(0.3) rotateX(45deg); opacity: 0; }
            100% { transform: scale(1) rotateX(0deg); opacity: 1; }
        }
        .hostess-figure {
            width: 150px;
            height: 150px;
            margin: 0 auto 15px;
            border-radius: 50%;
            padding: 5px;
            background: linear-gradient(45deg, #00f2fe, #ffd700);
            box-shadow: 0 0 35px #00f2fe;
            animation: pulseWave 2s infinite;
        }
        .hostess-figure img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
        }
        @keyframes pulseWave {
            0% { box-shadow: 0 0 15px #00f2fe; }
            50% { box-shadow: 0 0 40px #ffd700, 0 0 20px #00f2fe; }
            100% { box-shadow: 0 0 15px #00f2fe; }
        }
        .speech-bubble-4d {
            background: #ffffff;
            color: #111;
            padding: 12px 24px;
            border-radius: 30px;
            font-weight: 800;
            font-size: 1.2rem;
            display: inline-block;
            margin: 15px 0;
            box-shadow: 0 5px 20px rgba(0,0,0,0.5);
            border: 2px solid #ffd700;
        }

        /* Admin Tabs & UI */
        .boss-banner-dashboard {
            background: linear-gradient(135deg, #0b0c10, #8b0000);
            border: 2px solid #ffd700;
            color: var(--boss-gold);
            padding: 20px;
            border-radius: 12px;
            text-align: center;
            margin-bottom: 25px;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.25);
        }
        .admin-nav-tabs {
            display: flex;
            gap: 12px;
            border-bottom: 2px solid #ddd;
            margin-bottom: 20px;
            padding-bottom: 10px;
        }
        .tab-btn {
            background: #eee;
            border: none;
            padding: 10px 20px;
            font-weight: 600;
            border-radius: 6px;
            cursor: pointer;
        }
        .tab-btn.active {
            background: var(--primary);
            color: white;
        }

        /* Custom Table */
        .custom-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            font-size: 0.9rem;
        }
        .custom-table th, .custom-table td {
            border: 1px solid #ddd;
            padding: 10px 12px;
            text-align: center;
        }
        .custom-table th {
            background: #8b0000;
            color: white;
        }
        .custom-table tr:nth-child(even) {
            background-color: #f9f9f9;
        }

        /* Marksheet Styling */
        #marksheet-preview {
            display: none;
            background: #ffffff;
            padding: 25px;
            border: 4px double #8b0000;
            border-radius: 8px;
            margin-top: 25px;
        }

        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 25px;
            margin-top: 50px;
            font-size: 0.9rem;
        }

        @media print {
            body * { visibility: hidden; }
            #marksheet-preview, #marksheet-preview * { visibility: visible; }
            #marksheet-preview { position: absolute; left: 0; top: 0; width: 100%; display: block !important; border: 2px solid #000; }
            .no-print { display: none !important; }
        }
    </style>
</head>
<body>

    <!-- 4D AUDIO GREETING OVERLAY (Voice Hostess) -->
    <div id="boss4DGreetingOverlay">
        <div class="box-4d-character">
            <div class="hostess-figure">
                <!-- AI Animated Hostess Assistant -->
                <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&w=300&q=80" alt="Virtual AI Hostess">
            </div>
            <div style="color: #00f2fe; font-size: 0.9rem; letter-spacing: 2px; text-transform: uppercase;">
                <i class="fa fa-wave-square"></i> 4D Virtual Assistant Activated
            </div>
            <div class="speech-bubble-4d">
                <i class="fa fa-volume-high" style="color: #e65100;"></i> "Welcome Mr. Boss!"
            </div>
            <p style="color: #eee; font-size: 0.95rem; margin-bottom: 20px;">
                प्रबंधक श्री <strong>Ajeet Yadav</strong> जी, सिस्टम आपके स्वागत के लिए तैयार है।
            </p>
            <button onclick="enterDashboard()" class="btn-submit" style="background: linear-gradient(45deg, #ffd700, #ff8c00); color: #000; font-weight: 800; border-radius: 30px; padding: 12px 35px; box-shadow: 0 0 20px #ffd700;">
                <i class="fa fa-door-open"></i> Proceed to Terminal
            </button>
        </div>
    </div>

    <!-- Top Contact Bar -->
    <div class="top-bar">
        <div>
            <i class="fa fa-map-marker-alt"></i> Radha Krishna Mohalla, Aliganj (Etah)
            <span style="margin-left: 15px;"><i class="fa fa-phone"></i> 9412874591, 9761805343</span>
        </div>
        <div>
            <span>School Manager: <strong>Ajeet Yadav</strong></span>
            <a href="#admission">Online Admission Form</a>
        </div>
    </div>

    <!-- Navigation Header -->
    <header>
        <div class="nav-container">
            <div class="logo-box">
                <div class="school-crest"><i class="fa-solid fa-graduation-cap"></i></div>
                <div>
                    <h1>J.S. Vidya Niketan</h1>
                    <p>Residential School | Classes Nursery to 8th | Aliganj (Etah)</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#facilities">Facilities</a></li>
                    <li><a href="#admission" class="btn-apply-nav"><i class="fa fa-pencil-alt"></i> Online Admission</a></li>
                    <li><a href="javascript:void(0)" onclick="openAdmin()" class="btn-admin-nav"><i class="fa fa-fingerprint"></i> jsterminal admine.in</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Notice Ticker -->
    <div class="alert-ticker">
        <span>सूचना / Notice:</span>
        <marquee id="live-marquee" behavior="scroll" direction="left">
            नए सत्र के लिए ऑनलाइन प्रवेश प्रारंभ (Admission Open) | Nursery से 8th क्लास | हॉस्टल व बस सुविधा उपलब्ध | 3 बच्चों से अधिक पर विशेष छूट!
        </marquee>
    </div>

    <!-- Hero Banner -->
    <section class="hero" id="home">
        <div class="badge-tag">Residential School - Aliganj (Etah)</div>
        <h2>J.S. VIDYA NIKETAN</h2>
        <p>A Premier Educational & Residential Institution dedicated to shaping bright futures through values, discipline, and academic excellence.</p>
        <div>
            <a href="#admission" style="background: #ffeb3b; color: #333; padding: 12px 28px; text-decoration: none; border-radius: 30px; font-weight: bold; margin-right: 10px;"><i class="fa fa-file-signature"></i> Online Admission लें</a>
            <a href="tel:9761805343" style="background: transparent; color: white; border: 2px solid white; padding: 10px 25px; text-decoration: none; border-radius: 30px; font-weight: bold;"><i class="fa fa-phone"></i> 9761805343</a>
        </div>
    </section>

    <!-- Facilities -->
    <section class="section" id="facilities">
        <div class="section-title">
            <h3>Facilities & Salient Features</h3>
            <p>विद्यार्थियों के सर्वांगीण विकास के लिए सर्वश्रेष्ठ सुविधाएं</p>
        </div>
        <div class="grid-features">
            <div class="card">
                <i class="fa fa-bed"></i>
                <h4>Hostel Facility</h4>
                <p>सुरक्षित, अनुशासित और घरेलू वातावरण वाला आधुनिक हॉस्टल (Residential Campus)।</p>
            </div>
            <div class="card">
                <i class="fa fa-chalkboard-teacher"></i>
                <h4>Classes: Nursery to 8th</h4>
                <p>अनुभवी और योग्य शिक्षकों द्वारा बच्चों की मजबूत बुनियादी शिक्षा पर विशेष ध्यान।</p>
            </div>
            <div class="card">
                <i class="fa fa-bus"></i>
                <h4>Van & Bus Service</h4>
                <p>छात्रों के सुरक्षित आवागमन के लिए विस्तृत क्षेत्रों में वाहन सुविधा उपलब्ध।</p>
            </div>
            <div class="card">
                <i class="fa fa-futbol"></i>
                <h4>Spacious Play Field</h4>
                <p>शारीरिक विकास व खेलकूद के लिए विशाल और सुरक्षित खेल का मैदान।</p>
            </div>
            <div class="card">
                <i class="fa fa-user-graduate"></i>
                <h4>Skill & Career Guidance</h4>
                <p>प्रारंभिक स्तर से ही बच्चों के कौशल विकास और करियर काउंसलिंग पर विशेष ध्यान।</p>
            </div>
            <div class="card">
                <i class="fa fa-percent"></i>
                <h4>Special Benefits</h4>
                <p>3 या अधिक बच्चों के दाखिले पर अभिभावकों के लिए विशेष फीस डिस्काउंट।</p>
            </div>
        </div>
    </section>

    <!-- ONLINE ADMISSION FORM SECTION -->
    <section class="section" style="background: #eef2f5;" id="admission">
        <div class="section-title">
            <h3>Online Admission Form (सत्र 2026-27)</h3>
            <p>घर बैठे अपने बच्चे का एडमिशन फॉर्म भरें, विद्यालय द्वारा आपसे तुरंत संपर्क किया जाएगा।</p>
        </div>
        
        <div class="admission-container">
            <form id="studentAdmissionForm" onsubmit="handleAdmissionSubmit(event)">
                <div class="form-row">
                    <div class="form-group">
                        <label>Student Full Name (छात्र/छात्रा का पूरा नाम) *</label>
                        <input type="text" id="adm_name" placeholder="उदा. रोहन यादव" required>
                    </div>
                    <div class="form-group">
                        <label>Father's Name (पिता का नाम) *</label>
                        <input type="text" id="adm_father" placeholder="उदा. श्री अमरपाल यादव" required>
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label>Mobile Number (मोबाइल नंबर) *</label>
                        <input type="tel" id="adm_mobile" pattern="[0-9]{10}" placeholder="उदा. 9876543210" required>
                    </div>
                    <div class="form-group">
                        <label>Class for Admission (किस कक्षा में प्रवेश चाहिए) *</label>
                        <select id="adm_class" required>
                            <option value="">-- कक्षा चुनें --</option>
                            <option value="Nursery">Nursery</option>
                            <option value="LKG">LKG</option>
                            <option value="UKG">UKG</option>
                            <option value="Class 1">Class 1</option>
                            <option value="Class 2">Class 2</option>
                            <option value="Class 3">Class 3</option>
                            <option value="Class 4">Class 4</option>
                            <option value="Class 5">Class 5</option>
                            <option value="Class 6">Class 6</option>
                            <option value="Class 7">Class 7</option>
                            <option value="Class 8">Class 8</option>
                        </select>
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label>Hostel Facility Required? (क्या हॉस्टल चाहिए?) *</label>
                        <select id="adm_hostel" required>
                            <option value="No">No (डे-स्कॉलर / Day Scholar)</option>
                            <option value="Yes">Yes (हॉस्टल में रहना है / Residential)</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Address / Village (गाँव / मोहल्ला / शहर) *</label>
                        <input type="text" id="adm_address" placeholder="उदा. राधा कृष्ण मोहल्ला, अलीगंज" required>
                    </div>
                </div>

                <div style="text-align: center; margin-top: 20px;">
                    <button type="submit" class="btn-submit" style="background: #2e7d32; font-size: 1.1rem; padding: 12px 35px;">
                        <i class="fa fa-paper-plane"></i> Submit Admission Form
                    </button>
                </div>
            </form>
        </div>
    </section>

    <!-- About & Management -->
    <section class="section" id="about">
        <div style="background: white; padding: 40px; border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.06); display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px;">
            <div>
                <h3 style="color: var(--primary); margin-bottom: 15px;"><i class="fa fa-bullseye"></i> Our Vision & Mission</h3>
                <p style="margin-bottom: 15px;">
                    "To be a world-class institution that will provide quantitative and qualitative education to give students a future hope and experience."
                </p>
                <p>
                    J.S. Vidya Niketan Aliganj (Etah) का उद्देश्य हर बच्चे को अनुशासन, संस्कार और आधुनिक शिक्षा के साथ आत्मनिर्भर बनाना है।
                </p>
            </div>
            <div>
                <h3 style="color: var(--primary); margin-bottom: 15px;"><i class="fa fa-id-badge"></i> संपर्क व प्रबंधन</h3>
                <p><strong>Manager:</strong> Ajeet Yadav</p>
                <p><strong>Contact Nos:</strong> 9412874591, 9761805343</p>
                <p><strong>School Campus:</strong> Radha Krishna Mohalla, Aliganj (Etah), Uttar Pradesh</p>
            </div>
        </div>
    </section>

    <!-- ADMIN MODAL PORTAL (jsterminal-admine.in) -->
    <div id="adminModal" class="modal">
        <div class="modal-content">
            <span class="close-btn" onclick="closeAdmin()">&times;</span>
            
            <!-- 4D Animated Hologram Login Step -->
            <div id="admin-login-view" class="boss-login-card">
                
                <div class="hologram-stage-4d">
                    <div class="hologram-ring"></div>
                    <div class="hologram-avatar">
                        <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&w=300&q=80" alt="4D Voice Hostess">
                    </div>
                </div>
                
                <h2 style="color: var(--primary); font-family: 'Orbitron', sans-serif; letter-spacing: 1px; margin-bottom: 2px;">
                    4D JS-TERMINAL PORTAL
                </h2>
                <p style="color: #666; font-size: 0.9rem; margin-bottom: 20px;">
                    Secure Gateway ID: <strong style="color: #0088cc;">jsterminal admine.in</strong>
                </p>

                <div class="form-group" style="max-width: 400px; margin: 0 auto 15px; text-align: left;">
                    <label style="font-weight: bold;"><i class="fa fa-shield-halved"></i> Enter Master Admin Password:</label>
                    <input type="password" id="adminPassword" placeholder="पासवर्ड यहाँ दर्ज करें..." style="box-shadow: 0 0 10px rgba(0,0,0,0.1);">
                </div>
                <button class="btn-submit" style="width: 100%; max-width: 400px; background: linear-gradient(135deg, #111, #8b0000); border: 1px solid #ffd700; color: #ffd700;" onclick="verifyAdmin()">
                    <i class="fa fa-key"></i> Authenticate & Login
                </button>
            </div>

            <!-- Admin Control Dashboard -->
            <div id="admin-dashboard-view" style="display: none;">
                
                <!-- Welcome Mr. Boss Banner -->
                <div class="boss-banner-dashboard">
                    <h2 style="font-family: 'Orbitron', sans-serif;"><i class="fa fa-crown" style="color: #ffd700;"></i> Welcome Mr. Boss!</h2>
                    <p style="color: #fff; font-size: 1rem; margin-top: 4px;">प्रबंधक श्री <strong>Ajeet Yadav</strong> जी, J.S. Vidya Niketan कंट्रोल टर्मिनल में आपका स्वागत है।</p>
                </div>

                <!-- Admin Tabs -->
                <div class="admin-nav-tabs">
                    <button class="tab-btn active" onclick="switchTab('admissions')"><i class="fa fa-user-graduate"></i> नए एडमिशन आवेदन (<span id="adm-count">0</span>)</button>
                    <button class="tab-btn" onclick="switchTab('marksheet')"><i class="fa fa-calculator"></i> मार्कशीट जनरेटर</button>
                    <button class="tab-btn" onclick="switchTab('notice')"><i class="fa fa-bullhorn"></i> नोटिस बोर्ड सेटिंग</button>
                </div>

                <!-- TAB 1: Online Admissions List -->
                <div id="tab-admissions">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px;">
                        <h4 style="color: var(--primary);"><i class="fa fa-list"></i> प्राप्त ऑनलाइन एडमिशन रिकॉर्ड्स</h4>
                        <button onclick="clearAllAdmissions()" style="background: #c62828; color: white; border: none; padding: 6px 12px; border-radius: 4px; cursor: pointer;"><i class="fa fa-trash"></i> Clear All</button>
                    </div>

                    <div style="overflow-x: auto;">
                        <table class="custom-table" id="admissionRecordsTable">
                            <thead>
                                <tr>
                                    <th>#</th>
                                    <th>छात्र का नाम</th>
                                    <th>पिता का नाम</th>
                                    <th>कक्षा</th>
                                    <th>मोबाइल नंबर</th>
                                    <th>हॉस्टल</th>
                                    <th>पता</th>
                                    <th>तारीख</th>
                                </tr>
                            </thead>
                            <tbody id="admissionTableBody">
                            </tbody>
                        </table>
                    </div>
                    <p id="no-admissions-msg" style="text-align: center; color: #888; margin-top: 20px;">अभी तक कोई नया ऑनलाइन एडमिशन फॉर्म नहीं आया है।</p>
                </div>

                <!-- TAB 2: Marksheet Generator (With Grade Column) -->
                <div id="tab-marksheet" style="display: none;">
                    <h4 style="color: var(--primary); margin-bottom: 15px;"><i class="fa fa-file-invoice"></i> मार्कशीट बनाएं और प्रिंट करें</h4>
                    
                    <div class="form-row">
                        <div class="form-group">
                            <label>छात्र का नाम (Student Name):</label>
                            <input type="text" id="stName" placeholder="उदा. Rahul Kumar">
                        </div>
                        <div class="form-group">
                            <label>रोल नंबर (Roll No):</label>
                            <input type="text" id="stRoll" placeholder="उदा. 102">
                        </div>
                        <div class="form-group">
                            <label>कक्षा (Class):</label>
                            <select id="stClass">
                                <option value="Nursery">Nursery</option>
                                <option value="LKG">LKG</option>
                                <option value="UKG">UKG</option>
                                <option value="Class 1">Class 1</option>
                                <option value="Class 2">Class 2</option>
                                <option value="Class 3">Class 3</option>
                                <option value="Class 4">Class 4</option>
                                <option value="Class 5">Class 5</option>
                                <option value="Class 6">Class 6</option>
                                <option value="Class 7">Class 7</option>
                                <option value="Class 8">Class 8</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Overall Grade (कस्टम ग्रेड यदि लागू हो):</label>
                            <select id="stGradeOption">
                                <option value="AUTO">Auto (प्रतिशत से तय होगा)</option>
                                <option value="A+">A+ (Outstanding)</option>
                                <option value="A">A (Excellent)</option>
                                <option value="B+">B+ (Very Good)</option>
                                <option value="B">B (Good)</option>
                                <option value="C">C (Fair)</option>
                                <option value="D">D (Pass)</option>
                                <option value="E">E (Needs Improvement)</option>
                            </select>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label>Hindi (पूर्णांक: 100):</label>
                            <input type="number" id="mHindi" min="0" max="100" placeholder="0-100">
                        </div>
                        <div class="form-group">
                            <label>English (पूर्णांक: 100):</label>
                            <input type="number" id="mEnglish" min="0" max="100" placeholder="0-100">
                        </div>
                        <div class="form-group">
                            <label>Math (पूर्णांक: 100):</label>
                            <input type="number" id="mMath" min="0" max="100" placeholder="0-100">
                        </div>
                        <div class="form-group">
                            <label>Science (पूर्णांक: 100):</label>
                            <input type="number" id="mScience" min="0" max="100" placeholder="0-100">
                        </div>
                        <div class="form-group">
                            <label>Social Science (पूर्णांक: 100):</label>
                            <input type="number" id="mSst" min="0" max="100" placeholder="0-100">
                        </div>
                    </div>

                    <button class="btn-submit" onclick="generateReportCard()"><i class="fa fa-calculator"></i> Calculate & Create Marksheet</button>

                    <!-- Marksheet Document with Dedicated GRADE Column -->
                    <div id="marksheet-preview">
                        <div style="text-align: center; border-bottom: 2px solid #8b0000; padding-bottom: 10px; margin-bottom: 12px;">
                            <h2 style="color: #8b0000; margin: 0;">J.S. VIDYA NIKETAN</h2>
                            <p style="font-size: 0.9rem; font-weight: bold; margin: 0;">RESIDENTIAL SCHOOL, ALIGANJ (ETAH)</p>
                            <p style="font-size: 0.8rem; margin: 0;">Affiliated Curriculum - Nursery to 8th | Contact: 9412874591, 9761805343</p>
                            <h4 style="margin-top: 8px; text-decoration: underline;">ANNUAL STUDENT PROGRESS REPORT</h4>
                        </div>

                        <div style="display: flex; justify-content: space-between; margin-bottom: 10px; font-size: 0.95rem;">
                            <div><strong>Student Name:</strong> <span id="lbl-name"></span></div>
                            <div><strong>Roll No:</strong> <span id="lbl-roll"></span></div>
                            <div><strong>Class:</strong> <span id="lbl-class"></span></div>
                        </div>

                        <!-- Table with Grade Column Added -->
                        <table class="custom-table" style="margin-bottom: 15px;">
                            <thead>
                                <tr>
                                    <th>Subject (विषय)</th>
                                    <th>Max Marks (पूर्णांक)</th>
                                    <th>Marks Obtained (प्राप्तांक)</th>
                                    <th style="background: #e65100;">Grade (ग्रेड)</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr><td>Hindi</td><td>100</td><td id="res-hindi"></td><td id="grd-hindi" style="font-weight: bold;"></td></tr>
                                <tr><td>English</td><td>100</td><td id="res-eng"></td><td id="grd-eng" style="font-weight: bold;"></td></tr>
                                <tr><td>Mathematics</td><td>100</td><td id="res-math"></td><td id="grd-math" style="font-weight: bold;"></td></tr>
                                <tr><td>Science</td><td>100</td><td id="res-sci"></td><td id="grd-sci" style="font-weight: bold;"></td></tr>
                                <tr><td>Social Science</td><td>100</td><td id="res-sst"></td><td id="grd-sst" style="font-weight: bold;"></td></tr>
                                <tr style="font-weight: bold; background: #fafafa;">
                                    <td>Grand Total</td>
                                    <td>500</td>
                                    <td id="res-total"></td>
                                    <td id="lbl-grade-col" style="color: green; font-size: 1.05rem;"></td>
                                </tr>
                            </tbody>
                        </table>

                        <div style="display: flex; justify-content: space-around; margin: 12px 0; font-size: 1.05rem; font-weight: bold;">
                            <div>Percentage: <span id="lbl-percentage" style="color: var(--primary);"></span>%</div>
                            <div>Overall Grade: <span id="lbl-grade" style="color: green;"></span></div>
                            <div>Result Status: <span id="lbl-status"></span></div>
                        </div>

                        <div style="display: flex; justify-content: space-between; margin-top: 35px; padding: 0 15px;">
                            <div>____________________<br><strong>Class Teacher</strong></div>
                            <div>____________________<br><strong>Principal / Manager (Ajeet Yadav)</strong></div>
                        </div>

                        <div class="no-print" style="text-align: center; margin-top: 25px;">
                            <button class="btn-submit" style="background: #2e7d32;" onclick="window.print()"><i class="fa fa-print"></i> Print / Download PDF Marksheet</button>
                        </div>
                    </div>
                </div>

                <!-- TAB 3: Notice Setting -->
                <div id="tab-notice" style="display: none;">
                    <h4 style="color: var(--primary); margin-bottom: 10px;"><i class="fa fa-edit"></i> मुख्य स्क्रॉलिंग सूचना बदलें</h4>
                    <p style="font-size: 0.88rem; color: #666; margin-bottom: 12px;">यहाँ जो भी लिखेंगे वो होमपेज की पट्टी पर लाइव चलने लगेगा:</p>
                    <div style="display: flex; gap: 10px;">
                        <input type="text" id="newNoticeText" placeholder="नया नोटिस यहाँ टाइप करें..." style="flex: 1; padding: 10px; border: 1px solid #ccc; border-radius: 6px;">
                        <button class="btn-submit" onclick="updateNotice()">Save Notice</button>
                    </div>
                </div>

            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 <strong>J.S. Vidya Niketan (Residential School)</strong>, Radha Krishna Mohalla, Aliganj (Etah).</p>
        <p style="font-size: 0.8rem; margin-top: 6px; color: #bbb;">Admin Terminal: jsterminal admine.in | Manager: Ajeet Yadav (9412874591, 9761805343)</p>
    </footer>

    <!-- Script Logic -->
    <script>
        let admissionData = JSON.parse(localStorage.getItem('jsvn_admissions')) || [];

        function renderAdmissions() {
            const tbody = document.getElementById('admissionTableBody');
            const noMsg = document.getElementById('no-admissions-msg');
            const countLabel = document.getElementById('adm-count');
            tbody.innerHTML = "";
            countLabel.innerText = admissionData.length;

            if (admissionData.length === 0) {
                noMsg.style.display = "block";
                return;
            }
            noMsg.style.display = "none";

            admissionData.forEach((item, index) => {
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td>${index + 1}</td>
                    <td><strong>${item.name}</strong></td>
                    <td>${item.father}</td>
                    <td><span style="background: #e0f2fe; color: #0284c7; padding: 2px 8px; border-radius: 4px; font-weight: bold;">${item.sClass}</span></td>
                    <td><a href="tel:${item.mobile}" style="color: #15803d; font-weight: bold;"><i class="fa fa-phone"></i> ${item.mobile}</a></td>
                    <td>${item.hostel === 'Yes' ? '<span style="color: #b91c1c; font-weight: bold;">Hostel</span>' : 'Day Scholar'}</td>
                    <td>${item.address}</td>
                    <td style="font-size: 0.8rem; color: #666;">${item.date}</td>
                `;
                tbody.appendChild(tr);
            });
        }

        function handleAdmissionSubmit(e) {
            e.preventDefault();

            const newEntry = {
                name: document.getElementById('adm_name').value.trim(),
                father: document.getElementById('adm_father').value.trim(),
                mobile: document.getElementById('adm_mobile').value.trim(),
                sClass: document.getElementById('adm_class').value,
                hostel: document.getElementById('adm_hostel').value,
                address: document.getElementById('adm_address').value.trim(),
                date: new Date().toLocaleDateString('hi-IN')
            };

            admissionData.push(newEntry);
            localStorage.setItem('jsvn_admissions', JSON.stringify(admissionData));

            alert("बधाई हो! आपका ऑनलाइन एडमिशन फॉर्म सफलतापूर्वक स्कूल एडमिन के पास जमा हो गया है। विद्यालय प्रबंधक Ajeet Yadav जी आपसे शीघ्र ही संपर्क करेंगे।");
            document.getElementById('studentAdmissionForm').reset();
        }

        function clearAllAdmissions() {
            if (confirm("क्या आप वाकई सभी एडमिशन रिकॉर्ड हटाना चाहते हैं?")) {
                admissionData = [];
                localStorage.removeItem('jsvn_admissions');
                renderAdmissions();
            }
        }

        function openAdmin() {
            document.getElementById('adminModal').style.display = 'flex';
        }
        function closeAdmin() {
            document.getElementById('adminModal').style.display = 'none';
        }

        // Voice AI Function: Speaks "Welcome Mr. Boss"
        function speakWelcome() {
            if ('speechSynthesis' in window) {
                const utterance = new SpeechSynthesisUtterance("Welcome Mr. Boss!");
                utterance.pitch = 1.2;
                utterance.rate = 0.95;
                // Choose female voice if available
                const voices = window.speechSynthesis.getVoices();
                const femaleVoice = voices.find(v => v.name.includes('Female') || v.name.includes('Zira') || v.name.includes('Google UK English Female') || v.lang.includes('en'));
                if (femaleVoice) {
                    utterance.voice = femaleVoice;
                }
                window.speechSynthesis.speak(utterance);
            }
        }

        // 4D Login Verification: jsvnaliganj@123
        function verifyAdmin() {
            const pass = document.getElementById('adminPassword').value;
            if (pass === "jsvnaliganj@123") {
                // Show 4D Hostess Modal
                const overlay = document.getElementById('boss4DGreetingOverlay');
                overlay.style.display = 'flex';
                speakWelcome();
            } else {
                alert("गलत पासवर्ड! कृपया सही एडमिन पासवर्ड दर्ज करें।");
            }
        }

        // Enter Terminal from 4D Greeting Screen
        function enterDashboard() {
            document.getElementById('boss4DGreetingOverlay').style.display = 'none';
            document.getElementById('admin-login-view').style.display = 'none';
            document.getElementById('admin-dashboard-view').style.display = 'block';
            renderAdmissions();
        }

        function switchTab(tabId) {
            document.getElementById('tab-admissions').style.display = (tabId === 'admissions') ? 'block' : 'none';
            document.getElementById('tab-marksheet').style.display = (tabId === 'marksheet') ? 'block' : 'none';
            document.getElementById('tab-notice').style.display = (tabId === 'notice') ? 'block' : 'none';

            const buttons = document.querySelectorAll('.tab-btn');
            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
        }

        function updateNotice() {
            const text = document.getElementById('newNoticeText').value;
            if (text.trim() !== "") {
                document.getElementById('live-marquee').innerText = text;
                alert("नोटिस बोर्ड अपडेट हो चुका है!");
            }
        }

        // Subject Grade Helper Function
        function getSubjectGrade(m) {
            if (m >= 90) return 'A+';
            if (m >= 80) return 'A';
            if (m >= 70) return 'B+';
            if (m >= 60) return 'B';
            if (m >= 50) return 'C';
            if (m >= 33) return 'D';
            return 'E';
        }

        // Marksheet Calculator with Column Grade
        function generateReportCard() {
            const name = document.getElementById('stName').value.trim();
            const roll = document.getElementById('stRoll').value.trim();
            const sClass = document.getElementById('stClass').value;
            const chosenGradeOption = document.getElementById('stGradeOption').value;

            const h = parseFloat(document.getElementById('mHindi').value) || 0;
            const e = parseFloat(document.getElementById('mEnglish').value) || 0;
            const m = parseFloat(document.getElementById('mMath').value) || 0;
            const s = parseFloat(document.getElementById('mScience').value) || 0;
            const ss = parseFloat(document.getElementById('mSst').value) || 0;

            if (!name || !roll) {
                alert("कृपया छात्र का नाम और रोल नंबर अवश्य दर्ज करें!");
                return;
            }

            const total = h + e + m + s + ss;
            const percentage = (total / 500) * 100;

            let finalGrade = '';
            let status = (percentage >= 33) ? 'Passed' : 'Failed / Re-exam';

            if (chosenGradeOption === 'AUTO') {
                if (percentage >= 90) finalGrade = 'A+ (Outstanding)';
                else if (percentage >= 80) finalGrade = 'A (Excellent)';
                else if (percentage >= 70) finalGrade = 'B+ (Very Good)';
                else if (percentage >= 60) finalGrade = 'B (Good)';
                else if (percentage >= 50) finalGrade = 'C (Fair)';
                else if (percentage >= 33) finalGrade = 'D (Satisfactory)';
                else finalGrade = 'E (Needs Improvement)';
            } else {
                finalGrade = chosenGradeOption;
            }

            // Fill Details
            document.getElementById('lbl-name').innerText = name;
            document.getElementById('lbl-roll').innerText = roll;
            document.getElementById('lbl-class').innerText = sClass;

            // Fill Subject Marks
            document.getElementById('res-hindi').innerText = h;
            document.getElementById('res-eng').innerText = e;
            document.getElementById('res-math').innerText = m;
            document.getElementById('res-sci').innerText = s;
            document.getElementById('res-sst').innerText = ss;
            document.getElementById('res-total').innerText = total;

            // Fill Dedicated Grade Column for each subject
            document.getElementById('grd-hindi').innerText = getSubjectGrade(h);
            document.getElementById('grd-eng').innerText = getSubjectGrade(e);
            document.getElementById('grd-math').innerText = getSubjectGrade(m);
            document.getElementById('grd-sci').innerText = getSubjectGrade(s);
            document.getElementById('grd-sst').innerText = getSubjectGrade(ss);
            document.getElementById('lbl-grade-col').innerText = finalGrade.split(' ')[0];

            // Summary Info
            document.getElementById('lbl-percentage').innerText = percentage.toFixed(2);
            document.getElementById('lbl-grade').innerText = finalGrade;
            document.getElementById('lbl-status').innerText = status;
            document.getElementById('lbl-status').style.color = (status === 'Passed') ? '#15803d' : '#b91c1c';

            document.getElementById('marksheet-preview').style.display = 'block';
            document.getElementById('marksheet-preview').scrollIntoView({ behavior: 'smooth' });
        }
    </script>
</body>
</html>
