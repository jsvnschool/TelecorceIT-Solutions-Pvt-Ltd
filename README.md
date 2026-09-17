<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telicorcel IT Solution Pvt. Ltd. | Enterprise IT & Digital Solutions</title>
    <!-- Google Fonts & Font Awesome Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #0052cc;
            --primary-dark: #0747a6;
            --secondary: #172b4d;
            --accent: #00b8d9;
            --light-bg: #f8fafc;
            --text: #334155;
            --text-light: #64748b;
            --white: #ffffff;
            --border: #e2e8f0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            color: var(--text);
            background-color: var(--white);
            line-height: 1.6;
        }

        /* Top Bar */
        .top-bar {
            background-color: var(--secondary);
            color: #cbd5e1;
            padding: 8px 5%;
            font-size: 0.85rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .top-bar a {
            color: #cbd5e1;
            text-decoration: none;
            margin-right: 15px;
        }

        .top-bar a:hover {
            color: var(--accent);
        }

        /* Navigation */
        nav {
            position: sticky;
            top: 0;
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.06);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 18px 5%;
            z-index: 1000;
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--secondary);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .logo span {
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 24px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--primary);
        }

        .btn-header {
            background: var(--primary);
            color: var(--white);
            padding: 8px 18px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s;
        }

        .btn-header:hover {
            background: var(--primary-dark);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(7,71,166,0.95), rgba(23,43,77,0.95)), url('https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=1600&q=80') center/cover;
            color: var(--white);
            padding: 100px 5%;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            font-weight: 700;
        }

        .hero p {
            font-size: 1.15rem;
            max-width: 700px;
            margin: 0 auto 30px;
            color: #e2e8f0;
        }

        .hero .btn {
            background: var(--accent);
            color: var(--secondary);
            padding: 12px 28px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            box-shadow: 0 4px 14px rgba(0,184,217,0.3);
            display: inline-block;
        }

        /* Common Section Styling */
        section {
            padding: 80px 5%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-header h2 {
            font-size: 2.2rem;
            color: var(--secondary);
            margin-bottom: 10px;
        }

        .section-header p {
            color: var(--text-light);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
        }

        .service-card {
            background: var(--white);
            border: 1px solid var(--border);
            padding: 30px;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.07);
            border-color: var(--primary);
        }

        .service-icon {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 1.25rem;
            margin-bottom: 12px;
            color: var(--secondary);
        }

        /* Leadership Section */
        .leadership-bg {
            background: var(--light-bg);
        }

        .leadership-grid {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
        }

        .leader-card {
            background: var(--white);
            border-radius: 12px;
            overflow: hidden;
            width: 320px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border: 1px solid var(--border);
        }

        .leader-img {
            background: #e2e8f0;
            height: 220px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #94a3b8;
            font-size: 4rem;
        }

        .leader-info {
            padding: 24px;
        }

        .leader-info h3 {
            color: var(--secondary);
            font-size: 1.25rem;
            margin-bottom: 5px;
        }

        .leader-info .designation {
            color: var(--primary);
            font-weight: 600;
            font-size: 0.95rem;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Locations */
        .locations-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
        }

        .location-card {
            border: 1px solid var(--border);
            padding: 25px;
            border-radius: 8px;
            background: var(--light-bg);
            border-left: 4px solid var(--primary);
        }

        .location-card h3 {
            color: var(--secondary);
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info-list {
            list-style: none;
            margin-top: 20px;
        }

        .contact-info-list li {
            margin-bottom: 20px;
            display: flex;
            gap: 15px;
            align-items: flex-start;
        }

        .contact-info-list i {
            font-size: 1.2rem;
            color: var(--primary);
            margin-top: 4px;
        }

        .contact-form {
            background: var(--light-bg);
            padding: 35px;
            border-radius: 10px;
            border: 1px solid var(--border);
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 6px;
            font-weight: 500;
            font-size: 0.9rem;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px 14px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-size: 0.95rem;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .submit-btn {
            background: var(--primary);
            color: var(--white);
            border: none;
            padding: 12px 24px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            width: 100%;
            transition: background 0.3s;
        }

        .submit-btn:hover {
            background: var(--primary-dark);
        }

        /* Footer */
        footer {
            background: var(--secondary);
            color: #94a3b8;
            padding: 40px 5% 20px;
            text-align: center;
            font-size: 0.9rem;
        }

        footer hr {
            border: none;
            border-top: 1px solid #334155;
            margin: 20px 0;
        }

        @media (max-width: 768px) {
            .contact-container {
                grid-template-columns: 1fr;
            }
            nav ul {
                display: none;
            }
            .top-bar {
                flex-direction: column;
                gap: 5px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Header Top Bar -->
    <div class="top-bar">
        <div>
            <i class="fa-solid fa-location-dot"></i> Sector 62, Noida | Greater Noida / NCR Region
        </div>
        <div>
            <a href="tel:9012574505"><i class="fa-solid fa-phone"></i> +91 9012574505</a>
            <a href="tel:7678519164"><i class="fa-solid fa-phone"></i> +91 7678519164</a>
        </div>
    </div>

    <!-- Navigation -->
    <nav>
        <div class="logo">Telicorcel <span>IT Solution</span></div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#leadership">Leadership</a></li>
            <li><a href="#locations">Presence</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <a href="#contact" class="btn-header">Enquire Now</a>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <h1>Transforming Enterprises With Cutting-Edge IT Solutions</h1>
        <p>Telicorcel IT Solution Pvt. Ltd. delivers custom enterprise software, cloud operations, network infrastructure, and digital consulting to drive your business growth.</p>
        <a href="#contact" class="btn">Connect With Sales</a>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="section-header">
            <h2>Our Core Expertise</h2>
            <p>Reliable, scalable, and secure technology services tailored for startups to enterprise businesses.</p>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon"><i class="fa-solid fa-laptop-code"></i></div>
                <h3>Custom Software Development</h3>
                <p>Bespoke web applications, SaaS products, and robust backend architectures designed around your workflows.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fa-solid fa-network-wired"></i></div>
                <h3>IT Infrastructure & Networking</h3>
                <p>Complete enterprise networking setup, hardware management, local network operations, and maintenance.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fa-solid fa-cloud"></i></div>
                <h3>Cloud Migration & Security</h3>
                <p>Zero-downtime server migrations, automated backups, and advanced cybersecurity audits.</p>
            </div>
            <div class="service-card">
                <div class="service-icon"><i class="fa-solid fa-headset"></i></div>
                <h3>Managed IT Support</h3>
                <p>24/7 technical monitoring, dedicated on-site assistance, and helpdesk support for business continuity.</p>
            </div>
        </div>
    </section>

    <!-- Leadership Section -->
    <section class="leadership-bg" id="leadership">
        <div class="section-header">
            <h2>Executive Leadership</h2>
            <p>Guided by industry veterans committed to delivering excellence and driving sustainable value.</p>
        </div>
        <div class="leadership-grid">
            <!-- CEO -->
            <div class="leader-card">
                <div class="leader-img">
                    <i class="fa-solid fa-user-tie"></i>
                </div>
                <div class="leader-info">
                    <h3>Satyam Sharma</h3>
                    <div class="designation">Chief Executive Officer (CEO)</div>
                    <p>Spearheading company strategy, innovation, and strategic partnerships at Telicorcel IT Solution Pvt. Ltd.</p>
                </div>
            </div>

            <!-- Sales Manager -->
            <div class="leader-card">
                <div class="leader-img">
                    <i class="fa-solid fa-user-tie"></i>
                </div>
                <div class="leader-info">
                    <h3>Shivam Sharma</h3>
                    <div class="designation">Sales Manager</div>
                    <p>Managing corporate sales, enterprise client relations, and strategic account growth across key regions.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Regional Presence & Offices -->
    <section id="locations">
        <div class="section-header">
            <h2>Our Operational Presence</h2>
            <p>Headquartered in Noida's central IT corridor with localized enterprise support coverage.</p>
        </div>
        <div class="locations-grid">
            <div class="location-card">
                <h3><i class="fa-solid fa-building"></i> Corporate Registered Office</h3>
                <p><strong>Telicorcel IT Solution Pvt. Ltd.</strong></p>
                <p>Block A, Industrial Area, Sector 62</p>
                <p>Noida, Uttar Pradesh – 201309</p>
            </div>
            <div class="location-card">
                <h3><i class="fa-solid fa-map-pin"></i> Local Service Unit (Sector 44)</h3>
                <p>Dedicated customer support & regional representative network serving commercial units and residential clusters around <strong>Sector 44, Noida</strong>.</p>
            </div>
            <div class="location-card">
                <h3><i class="fa-solid fa-map-pin"></i> Operations Support (Wazidpur)</h3>
                <p>Local field team & field support operations stationed to cater to clients around the <strong>Wazidpur, Noida</strong> area.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="leadership-bg" id="contact">
        <div class="section-header">
            <h2>Get In Touch</h2>
            <p>Speak to our sales leadership directly or send us an inquiry regarding your IT requirements.</p>
        </div>
        <div class="contact-container">
            <div>
                <h3>Direct Assistance</h3>
                <p style="margin-top: 10px; color: var(--text-light);">We are readily available to discuss your technical challenges, RFP requests, and consulting contracts.</p>

                <ul class="contact-info-list">
                    <li>
                        <i class="fa-solid fa-phone"></i>
                        <div>
                            <strong>Direct Helpline / Sales:</strong><br>
                            <a href="tel:9012574505" style="color: var(--primary); text-decoration: none;">+91 9012574505</a><br>
                            <a href="tel:7678519164" style="color: var(--primary); text-decoration: none;">+91 7678519164</a>
                        </div>
                    </li>
                    <li>
                        <i class="fa-solid fa-location-dot"></i>
                        <div>
                            <strong>Corporate Address:</strong><br>
                            Block A, Industrial Area, Sector 62,<br>
                            Noida, Uttar Pradesh - 201309, India
                        </div>
                    </li>
                    <li>
                        <i class="fa-solid fa-clock"></i>
                        <div>
                            <strong>Business Hours:</strong><br>
                            Monday – Saturday: 9:30 AM – 6:30 PM
                        </div>
                    </li>
                </ul>
            </div>

            <div class="contact-form">
                <form action="#" method="POST" onsubmit="event.preventDefault(); alert('Inquiry Sent! Our sales team will get back to you shortly.');">
                    <div class="form-group">
                        <label>Your Name / Company Name</label>
                        <input type="text" required placeholder="Enter full name or firm name">
                    </div>
                    <div class="form-group">
                        <label>Phone Number</label>
                        <input type="tel" required placeholder="Enter phone number">
                    </div>
                    <div class="form-group">
                        <label>Service Requirement</label>
                        <input type="text" placeholder="e.g. Web Development, IT Support">
                    </div>
                    <div class="form-group">
                        <label>Message / Description</label>
                        <textarea rows="4" placeholder="Briefly describe your requirements..."></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Send Message to Sales</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p><strong>Telicorcel IT Solution Pvt. Ltd.</strong> — Empowering Business with Scalable Technology</p>
        <p>Corporate Office: Block A, Industrial Area, Sector 62, Noida, UP 201309 | Serving Noida, Wazidpur, Sector 44 & NCR</p>
        <hr>
        <p>&copy; 2026 Telicorcel IT Solution Pvt. Ltd. All rights reserved.</p>
    </footer>

</body>
</html>
