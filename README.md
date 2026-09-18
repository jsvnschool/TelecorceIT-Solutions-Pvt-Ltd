<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Telecorcel IT Solutions Pvt Ltd | Enterprise Telecom, Software & Digital Stack</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <style>
    @keyframes floatSlow {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.35; transform: scale(1); }
      50% { opacity: 0.65; transform: scale(1.08); }
    }
    @keyframes scrollTicker {
      0% { transform: translateX(0); }
      100% { transform: translateX(-50%); }
    }
    .page-section { display: none; }
    .page-section.active { display: block; }
    .hero-glow { animation: pulseGlow 6s infinite ease-in-out; }
    .floating-card { animation: floatSlow 4s ease-in-out infinite; }
    .ticker-wrapper { display: flex; width: 200%; animation: scrollTicker 30s linear infinite; }
    .ticker-wrapper:hover { animation-play-state: paused; }
    
    #networkCanvas {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      pointer-events: none;
    }
    .brand-glow {
      text-shadow: 0 0 25px rgba(52, 211, 153, 0.45), 0 0 50px rgba(16, 185, 129, 0.25);
    }
    #globeCanvas {
      width: 100%;
      height: 480px;
      outline: none;
      cursor: grab;
    }
    #globeCanvas:active {
      cursor: grabbing;
    }
  </style>
</head>
<body class="font-sans text-slate-800 bg-[#040810] flex flex-col min-h-screen relative selection:bg-emerald-500 selection:text-slate-950">

  <!-- Floating Right Quick Action Dock -->
  <aside class="fixed right-4 bottom-6 md:bottom-auto md:top-1/3 z-50 flex flex-col gap-3">
    <a href="tel:+919012574505" title="Call Us: +91 9012574505" class="group relative flex items-center justify-center w-12 h-12 rounded-full bg-slate-900/90 border border-emerald-500/40 text-emerald-400 hover:bg-emerald-500 hover:text-slate-950 shadow-xl backdrop-blur transition-all duration-300">
      <i class="fa-solid fa-phone text-lg"></i>
      <span class="absolute right-14 bg-slate-900 text-white text-xs font-semibold py-1.5 px-3 rounded-lg border border-slate-700 whitespace-nowrap opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none shadow-lg">
        +91 9012574505 / 7678519164
      </span>
    </a>

    <a href="mailto:telecorcelitsolutionshelp@gmail.com" title="Email Us" class="group relative flex items-center justify-center w-12 h-12 rounded-full bg-slate-900/90 border border-emerald-500/40 text-emerald-400 hover:bg-emerald-500 hover:text-slate-950 shadow-xl backdrop-blur transition-all duration-300">
      <i class="fa-solid fa-envelope text-lg"></i>
      <span class="absolute right-14 bg-slate-900 text-white text-xs font-semibold py-1.5 px-3 rounded-lg border border-slate-700 whitespace-nowrap opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none shadow-lg">
        telecorcelitsolutionshelp@gmail.com
      </span>
    </a>

    <a href="https://wa.me/919012574505" target="_blank" title="WhatsApp Chat" class="group relative flex items-center justify-center w-12 h-12 rounded-full bg-slate-900/90 border border-emerald-500/40 text-emerald-400 hover:bg-emerald-500 hover:text-slate-950 shadow-xl backdrop-blur transition-all duration-300">
      <i class="fa-brands fa-whatsapp text-xl"></i>
      <span class="absolute right-14 bg-slate-900 text-white text-xs font-semibold py-1.5 px-3 rounded-lg border border-slate-700 whitespace-nowrap opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none shadow-lg">
        Direct WhatsApp Desk
      </span>
    </a>

    <button onclick="showPage('contact')" title="Direct Inquiries" class="group relative flex items-center justify-center w-12 h-12 rounded-full bg-emerald-500 text-slate-950 hover:bg-emerald-400 shadow-xl transition-all duration-300">
      <i class="fa-solid fa-headset text-lg"></i>
      <span class="absolute right-14 bg-slate-900 text-white text-xs font-semibold py-1.5 px-3 rounded-lg border border-slate-700 whitespace-nowrap opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none shadow-lg">
        24x7 NOC Support
      </span>
    </button>
  </aside>

  <!-- Clean Corporate Header with Selected Logo -->
  <header class="bg-[#070e1a]/90 backdrop-blur-md sticky top-0 z-40 border-b border-slate-800/80">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-3 flex justify-between items-center">
      <div class="flex items-center gap-3.5 cursor-pointer" onclick="showPage('home')">
        <div class="bg-white p-1 rounded-xl shadow-md flex items-center justify-center border border-emerald-500/30 h-13 w-13 sm:h-14 sm:w-14 overflow-hidden">
          <img 
            src="Gemini_Generated_Image_wr9725wr9725wr97.jpg" 
            alt="Telecorcel IT Solutions Logo" 
            class="h-full w-full object-contain"
            onerror="this.onerror=null; this.src='telecorcel logo_2.jpeg';"
          />
        </div>
        <div class="flex flex-col">
          <span class="text-xl sm:text-2xl font-black tracking-tight text-white leading-none brand-glow">
            TELECORCEL
          </span>
          <span class="text-[11px] sm:text-xs text-emerald-400 font-bold tracking-widest uppercase mt-0.5">
            IT SOLUTIONS PVT LTD
          </span>
        </div>
      </div>

      <nav class="hidden md:flex items-center gap-8 text-sm font-semibold text-slate-300">
        <button onclick="showPage('home')" class="hover:text-emerald-400 transition">Home</button>
        <button onclick="showPage('services')" class="hover:text-emerald-400 transition">Services</button>
        <button onclick="showPage('pricing')" class="hover:text-emerald-400 transition">Pricing</button>
        <button onclick="showPage('about')" class="hover:text-emerald-400 transition">About Us</button>
        <button onclick="showPage('contact')" class="hover:text-emerald-400 transition">Contact Us</button>
      </nav>

      <button onclick="showPage('contact')" class="bg-emerald-500 hover:bg-emerald-400 text-slate-950 text-xs sm:text-sm font-black px-5 py-2.5 rounded-lg shadow-lg shadow-emerald-500/25 transition transform hover:-translate-y-0.5">
        Get Started
      </button>
    </div>
  </header>

  <!-- Live Enterprise Capabilities Scrolling Ticker -->
  <div class="bg-emerald-950/40 border-y border-emerald-500/20 text-emerald-300 text-xs py-2 overflow-hidden select-none">
    <div class="ticker-wrapper font-medium tracking-wide">
      <div class="flex gap-8 items-center px-4">
        <span><i class="fa-solid fa-bolt text-emerald-400 mr-2"></i>Bulk SMS</span>
        <span>•</span>
        <span>Transactional & OTP SMS</span>
        <span>•</span>
        <span>WhatsApp Business Cloud API</span>
        <span>•</span>
        <span>RCS Messaging</span>
        <span>•</span>
        <span>Voice / IVR & Missed Call</span>
        <span>•</span>
        <span>DLT Support & Templates</span>
        <span>•</span>
        <span>Full-Stack Web Development</span>
        <span>•</span>
        <span>Android & iOS Apps</span>
        <span>•</span>
        <span>Custom CRM & ERP Software</span>
        <span>•</span>
        <span>Performance Marketing & SEO</span>
      </div>
      <div class="flex gap-8 items-center px-4">
        <span><i class="fa-solid fa-bolt text-emerald-400 mr-2"></i>Bulk SMS</span>
        <span>•</span>
        <span>Transactional & OTP SMS</span>
        <span>•</span>
        <span>WhatsApp Business Cloud API</span>
        <span>•</span>
        <span>RCS Messaging</span>
        <span>•</span>
        <span>Voice / IVR & Missed Call</span>
        <span>•</span>
        <span>DLT Support & Templates</span>
        <span>•</span>
        <span>Full-Stack Web Development</span>
        <span>•</span>
        <span>Android & iOS Apps</span>
        <span>•</span>
        <span>Custom CRM & ERP Software</span>
        <span>•</span>
        <span>Performance Marketing & SEO</span>
      </div>
    </div>
  </div>

  <!-- PAGE 1: HOME -->
  <main id="home" class="page-section active flex-grow">
    <!-- Hero Banner with Network Canvas Background -->
    <section class="relative min-h-[580px] sm:min-h-[660px] flex items-center justify-center overflow-hidden bg-gradient-to-b from-[#050b14] via-[#071120] to-[#040810] text-white">
      <canvas id="networkCanvas"></canvas>
      <div class="absolute -top-24 left-1/2 -translate-x-1/2 w-[600px] h-[600px] bg-emerald-500/15 rounded-full blur-3xl hero-glow pointer-events-none"></div>

      <div class="max-w-7xl mx-auto px-4 sm:px-6 py-16 sm:py-24 relative z-10 grid md:grid-cols-12 gap-10 items-center">
        <div class="md:col-span-7 space-y-6">
          <div class="inline-flex items-center gap-2 bg-emerald-500/10 border border-emerald-500/30 text-emerald-300 text-xs px-3.5 py-1.5 rounded-full font-bold tracking-wider uppercase">
            <span class="h-2 w-2 rounded-full bg-emerald-400 animate-pulse"></span> Omnichannel Telecom & IT Stack
          </div>

          <div class="space-y-2">
            <h2 class="text-xs uppercase tracking-[0.3em] font-extrabold text-slate-400">Next-Gen Communication & Custom Tech</h2>
            <h1 class="text-3xl sm:text-5xl lg:text-6xl font-black leading-none tracking-tight text-white">
              <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 via-teal-200 to-white brand-glow">
                TELECORCEL IT SOLUTIONS
              </span>
              <span class="block text-2xl sm:text-4xl text-slate-200 mt-2 font-bold">
                PVT LTD
              </span>
            </h1>
          </div>

          <p class="text-slate-300 text-sm sm:text-base leading-relaxed max-w-xl">
            Clean High-Throughput Bulk SMS, OTP Routes, RCS & WhatsApp Business API, Custom Software Development, Mobile Apps, aur Performance Marketing. Supporting over 20,000+ businesses with SLA guarantee and sub-second carrier delivery.
          </p>

          <div class="flex flex-wrap gap-4 pt-2">
            <button onclick="showPage('services')" class="bg-emerald-500 hover:bg-emerald-400 text-slate-950 font-bold px-7 py-3 rounded-lg shadow-xl shadow-emerald-500/25 transition transform hover:-translate-y-0.5">
              Explore All Services
            </button>
            <button onclick="showPage('pricing')" class="border border-slate-700 bg-slate-900/60 hover:bg-slate-800 text-slate-200 px-7 py-3 rounded-lg font-semibold transition">
              View Pricing Cards
            </button>
          </div>
        </div>

        <div class="md:col-span-5 grid grid-cols-2 gap-4">
          <div class="floating-card rounded-xl border border-slate-700/80 bg-slate-900/80 p-2 shadow-2xl backdrop-blur overflow-hidden">
            <img 
              src="telecorcel8.jpeg" 
              alt="Bulk SMS Service" 
              class="rounded-lg h-36 sm:h-44 w-full object-cover"
              onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1551836022-d5d88e9218df?w=600&auto=format&fit=crop&q=80';"
            />
          </div>
          <div class="floating-card rounded-xl border border-slate-700/80 bg-slate-900/80 p-2 shadow-2xl backdrop-blur overflow-hidden" style="animation-delay: 1.2s;">
            <img 
              src="telecorcel9.jpeg" 
              alt="Telecorcel Team" 
              class="rounded-lg h-36 sm:h-44 w-full object-cover"
              onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1522071820081-009f0129c71c?w=600&auto=format&fit=crop&q=80';"
            />
          </div>
          <div class="floating-card rounded-xl border border-slate-700/80 bg-slate-900/80 p-2 shadow-2xl backdrop-blur overflow-hidden" style="animation-delay: 0.6s;">
            <img 
              src="telecorcel4.jpeg" 
              alt="OTP Route" 
              class="rounded-lg h-36 sm:h-44 w-full object-cover"
              onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1563986768609-322da13575f3?w=600&auto=format&fit=crop&q=80';"
            />
          </div>
          <div class="floating-card rounded-xl border border-slate-700/80 bg-slate-900/80 p-2 shadow-2xl backdrop-blur overflow-hidden" style="animation-delay: 1.8s;">
            <img 
              src="telecorcel11.jpeg" 
              alt="SMS Campaign" 
              class="rounded-lg h-36 sm:h-44 w-full object-cover"
              onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1516321318423-f06f85e504b3?w=600&auto=format&fit=crop&q=80';"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Interactive Solutions Matrix (6 Core Pillars) -->
    <section class="py-16 max-w-7xl mx-auto px-4 sm:px-6 text-white">
      <div class="text-center mb-12">
        <span class="text-emerald-400 text-xs uppercase tracking-widest font-black">Everything Under One Roof</span>
        <h2 class="text-2xl sm:text-4xl font-extrabold mt-1">Our Comprehensive Services Portfolio</h2>
        <p class="text-slate-400 text-xs sm:text-sm mt-2 max-w-2xl mx-auto">
          High-throughput telecom infrastructure se lekar modern cloud web applications aur automated marketing funnels tak complete technology delivery.
        </p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Pillar 1: Bulk SMS & Telecom Routes -->
        <div class="p-6 rounded-2xl bg-slate-900/70 border border-slate-800 hover:border-emerald-500/60 transition group flex flex-col justify-between">
          <div>
            <div class="h-12 w-12 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl mb-4 group-hover:scale-110 transition">
              <i class="fa-solid fa-message"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-100 mb-2">Bulk SMS & Telecom Routing</h3>
            <p class="text-xs text-slate-400 mb-4">Dedicated carrier routes for zero-latency OTP, Transactional and high-volume Promotional SMS.</p>
            <div class="flex flex-wrap gap-1.5 mb-6">
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Promotional</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Transactional</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">OTP SMS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Flash SMS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Unicode/Regional</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">International SMS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">SMS API</span>
            </div>
          </div>
          <button onclick="showPage('services')" class="text-emerald-400 text-xs font-bold uppercase tracking-wider flex items-center gap-1.5 hover:text-emerald-300">
            View Details <i class="fa-solid fa-arrow-right text-[10px]"></i>
          </button>
        </div>

        <!-- Pillar 2: Omnichannel Messaging & IVR -->
        <div class="p-6 rounded-2xl bg-slate-900/70 border border-slate-800 hover:border-emerald-500/60 transition group flex flex-col justify-between">
          <div>
            <div class="h-12 w-12 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl mb-4 group-hover:scale-110 transition">
              <i class="fa-brands fa-whatsapp"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-100 mb-2">WhatsApp, RCS & Voice/IVR</h3>
            <p class="text-xs text-slate-400 mb-4">Official WhatsApp Business Cloud APIs, interactive RCS Rich Messaging, aur intelligent Voice IVR flows.</p>
            <div class="flex flex-wrap gap-1.5 mb-6">
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">WhatsApp API</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">RCS Messaging</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Voice SMS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">IVR Systems</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Missed Call</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Email API</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Short/Long Code</span>
            </div>
          </div>
          <button onclick="showPage('services')" class="text-emerald-400 text-xs font-bold uppercase tracking-wider flex items-center gap-1.5 hover:text-emerald-300">
            View Details <i class="fa-solid fa-arrow-right text-[10px]"></i>
          </button>
        </div>

        <!-- Pillar 3: DLT & Carrier Compliance -->
        <div class="p-6 rounded-2xl bg-slate-900/70 border border-slate-800 hover:border-emerald-500/60 transition group flex flex-col justify-between">
          <div>
            <div class="h-12 w-12 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl mb-4 group-hover:scale-110 transition">
              <i class="fa-solid fa-shield-halved"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-100 mb-2">DLT & Telecom Compliance</h3>
            <p class="text-xs text-slate-400 mb-4">Complete regulatory onboarding, Sender ID registration, and instant template approvals across Indian telcos.</p>
            <div class="flex flex-wrap gap-1.5 mb-6">
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">DLT Registration</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Sender ID</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">SMS Templates</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">PE Onboarding</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Consent Support</span>
            </div>
          </div>
          <button onclick="showPage('services')" class="text-emerald-400 text-xs font-bold uppercase tracking-wider flex items-center gap-1.5 hover:text-emerald-300">
            View Details <i class="fa-solid fa-arrow-right text-[10px]"></i>
          </button>
        </div>

        <!-- Pillar 4: Website Development -->
        <div class="p-6 rounded-2xl bg-slate-900/70 border border-slate-800 hover:border-emerald-500/60 transition group flex flex-col justify-between">
          <div>
            <div class="h-12 w-12 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl mb-4 group-hover:scale-110 transition">
              <i class="fa-solid fa-globe"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-100 mb-2">Website & Portal Development</h3>
            <p class="text-xs text-slate-400 mb-4">Responsive, high-converting business websites, custom web apps, and enterprise marketplace portals.</p>
            <div class="flex flex-wrap gap-1.5 mb-6">
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Corporate Websites</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">E-Commerce</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Landing Pages</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">CMS Portals</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">UI/UX Design</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">SSL & Hosting</span>
            </div>
          </div>
          <button onclick="showPage('services')" class="text-emerald-400 text-xs font-bold uppercase tracking-wider flex items-center gap-1.5 hover:text-emerald-300">
            View Details <i class="fa-solid fa-arrow-right text-[10px]"></i>
          </button>
        </div>

        <!-- Pillar 5: App Development -->
        <div class="p-6 rounded-2xl bg-slate-900/70 border border-slate-800 hover:border-emerald-500/60 transition group flex flex-col justify-between">
          <div>
            <div class="h-12 w-12 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl mb-4 group-hover:scale-110 transition">
              <i class="fa-solid fa-mobile-screen-button"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-100 mb-2">Mobile App Engineering</h3>
            <p class="text-xs text-slate-400 mb-4">Native and cross-platform mobile apps for iOS and Android with custom admin panels and push pipelines.</p>
            <div class="flex flex-wrap gap-1.5 mb-6">
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Android & iOS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Flutter</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">React Native</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Fintech Apps</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Booking & Delivery</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Admin Panels</span>
            </div>
          </div>
          <button onclick="showPage('services')" class="text-emerald-400 text-xs font-bold uppercase tracking-wider flex items-center gap-1.5 hover:text-emerald-300">
            View Details <i class="fa-solid fa-arrow-right text-[10px]"></i>
          </button>
        </div>

        <!-- Pillar 6: Software, SaaS & Marketing -->
        <div class="p-6 rounded-2xl bg-slate-900/70 border border-slate-800 hover:border-emerald-500/60 transition group flex flex-col justify-between">
          <div>
            <div class="h-12 w-12 rounded-xl bg-emerald-500/10 flex items-center justify-center text-emerald-400 text-2xl mb-4 group-hover:scale-110 transition">
              <i class="fa-solid fa-cubes"></i>
            </div>
            <h3 class="text-lg font-bold text-slate-100 mb-2">Custom Software & Digital Ads</h3>
            <p class="text-xs text-slate-400 mb-4">Enterprise Billing, Inventory, ERP/CRM suites with result-driven SEO and Performance Marketing.</p>
            <div class="flex flex-wrap gap-1.5 mb-6">
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Custom SaaS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">CRM / ERP</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Billing Software</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">HRMS / POS</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">Google Ads</span>
              <span class="text-[11px] bg-slate-950 border border-slate-800 px-2 py-0.5 rounded text-emerald-300">SEO & Lead Gen</span>
            </div>
          </div>
          <button onclick="showPage('services')" class="text-emerald-400 text-xs font-bold uppercase tracking-wider flex items-center gap-1.5 hover:text-emerald-300">
            View Details <i class="fa-solid fa-arrow-right text-[10px]"></i>
          </button>
        </div>
      </div>
    </section>

    <!-- SECTION: 3D Global Interactive Customer Network (iEnergizer Style) -->
    <section class="py-16 bg-[#03070f] border-t border-slate-800 relative overflow-hidden text-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6">
        <div class="text-center max-w-3xl mx-auto mb-10">
          <span class="text-emerald-400 text-xs uppercase tracking-widest font-black">Live 3D Customer Footprint</span>
          <h2 class="text-2xl sm:text-4xl font-extrabold mt-1">Telecorcel Global Network & Client Spread</h2>
          <p class="text-slate-400 text-xs sm:text-sm mt-2">
            Noida Sector 62 Headquarters se interconnected global high-speed carrier routes. Drag karke 3D Globe rotate karke live client nodes check karein.
          </p>
        </div>

        <div class="grid lg:grid-cols-12 gap-8 items-center bg-slate-900/50 border border-slate-800/90 rounded-2xl p-6 backdrop-blur shadow-2xl">
          <!-- 3D ThreeJS Interactive Globe -->
          <div class="lg:col-span-7 relative flex items-center justify-center">
            <div id="globeCanvasContainer" class="w-full h-[460px] flex items-center justify-center relative">
              <canvas id="globeCanvas"></canvas>
              <div class="absolute bottom-3 left-4 bg-slate-950/80 border border-slate-800 text-[11px] text-emerald-400 px-3 py-1.5 rounded-full pointer-events-none">
                <i class="fa-solid fa-arrows-spin mr-1"></i> Drag to rotate globe view
              </div>
            </div>
          </div>

          <!-- Customer Network Distribution Details -->
          <div class="lg:col-span-5 space-y-4">
            <div class="p-4 bg-slate-950/80 border border-emerald-500/30 rounded-xl">
              <div class="flex items-center justify-between">
                <span class="text-sm font-bold text-white"><i class="fa-solid fa-location-dot text-emerald-400 mr-2"></i>Noida HQ (India Hub)</span>
                <span class="text-[10px] bg-emerald-500/20 text-emerald-300 font-bold px-2 py-0.5 rounded">Origin Node</span>
              </div>
              <p class="text-xs text-slate-400 mt-1">Sector 62, Noida Carrier Switch & Primary Datacenter</p>
            </div>

            <div class="p-3.5 bg-slate-950/60 border border-slate-800 rounded-xl">
              <div class="flex justify-between items-center text-xs text-slate-300 font-semibold">
                <span><i class="fa-solid fa-satellite text-emerald-400 mr-2"></i>Americas (US East / West)</span>
                <span class="text-emerald-400 font-bold">2,400+ Enterprise Users</span>
              </div>
            </div>

            <div class="p-3.5 bg-slate-950/60 border border-slate-800 rounded-xl">
              <div class="flex justify-between items-center text-xs text-slate-300 font-semibold">
                <span><i class="fa-solid fa-satellite text-emerald-400 mr-2"></i>Europe & UK</span>
                <span class="text-emerald-400 font-bold">3,800+ Clients</span>
              </div>
            </div>

            <div class="p-3.5 bg-slate-950/60 border border-slate-800 rounded-xl">
              <div class="flex justify-between items-center text-xs text-slate-300 font-semibold">
                <span><i class="fa-solid fa-satellite text-emerald-400 mr-2"></i>Middle East (UAE / Saudi)</span>
                <span class="text-emerald-400 font-bold">4,200+ Retail & Gaming</span>
              </div>
            </div>

            <div class="p-3.5 bg-slate-950/60 border border-slate-800 rounded-xl">
              <div class="flex justify-between items-center text-xs text-slate-300 font-semibold">
                <span><i class="fa-solid fa-satellite text-emerald-400 mr-2"></i>APAC (Singapore / Australia)</span>
                <span class="text-emerald-400 font-bold">5,000+ Active Nodes</span>
              </div>
            </div>

            <div class="pt-2 text-center sm:text-left">
              <button onclick="showPage('contact')" class="w-full bg-emerald-500 hover:bg-emerald-400 text-slate-950 font-bold text-xs py-3 rounded-lg uppercase tracking-wider transition">
                Start Route Onboarding
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION: Embedded Google Map for Noida HQ -->
    <section class="py-14 bg-[#040810] border-t border-slate-800 text-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6">
        <div class="flex flex-col sm:flex-row sm:items-end justify-between mb-8">
          <div>
            <span class="text-emerald-400 text-xs uppercase tracking-widest font-black">Official Location Map</span>
            <h2 class="text-2xl sm:text-3xl font-black mt-1">Visit Telecorcel IT Solutions On Google Maps</h2>
            <p class="text-xs text-slate-400 mt-1">Block A, Industrial Area, Sector 62, Noida, Uttar Pradesh 201309</p>
          </div>
          <a href="https://maps.google.com/?q=Block+A,+Sector+62,+Noida,+Uttar+Pradesh+201309" target="_blank" class="mt-4 sm:mt-0 inline-flex items-center gap-2 text-xs font-bold text-slate-950 bg-emerald-400 hover:bg-emerald-300 px-4 py-2.5 rounded-lg transition">
            <i class="fa-solid fa-map-location-dot"></i> Open Full Google Maps
          </a>
        </div>

        <div class="rounded-2xl overflow-hidden border border-slate-800 shadow-2xl h-80 sm:h-96 w-full">
          <iframe 
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d14008.260465223035!2d77.36214532695537!3d28.627771749870197!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390ce5456ef36d9f%3A0x3b7191b1286136c8!2sSector%2062%2C%20Noida%2C%20Uttar%20Pradesh%20201309!5e0!3m2!1sen!2sin!4v1700000000000!5m2!1sen!2sin" 
            width="100%" 
            height="100%" 
            style="border:0; filter: invert(90%) hue-rotate(180deg);" 
            allowfullscreen="" 
            loading="lazy" 
            referrerpolicy="no-referrer-when-downgrade">
          </iframe>
        </div>
      </div>
    </section>
  </main>

  <!-- PAGE 2: SERVICES (DETAILED ENTERPRISE DIRECTORY) -->
  <main id="services" class="page-section flex-grow py-14 max-w-7xl mx-auto px-4 sm:px-6 text-white">
    <div class="text-center mb-12">
      <span class="text-emerald-400 text-xs uppercase tracking-widest font-black">All Vertical Capabilities</span>
      <h2 class="text-3xl sm:text-4xl font-black mt-1">Complete Services & Solutions Directory</h2>
      <p class="text-slate-400 text-xs sm:text-sm mt-2">Enterprise Communication, Software Architecture, Mobile Apps & Digital Growth</p>
    </div>

    <div class="space-y-10">
      <!-- 1. Bulk SMS & Messaging Infrastructure -->
      <div class="bg-slate-900/60 border border-slate-800 p-6 sm:p-8 rounded-2xl">
        <div class="flex items-center gap-3 border-b border-slate-800 pb-4 mb-6">
          <i class="fa-solid fa-comment-sms text-2xl text-emerald-400"></i>
          <div>
            <h3 class="text-xl font-bold text-white">1. Bulk SMS & Telecom Gateway Infrastructure</h3>
            <p class="text-xs text-slate-400">Direct carrier routing with real-time DLR and ultra-low latency</p>
          </div>
        </div>
        <div class="grid sm:grid-cols-2 md:grid-cols-4 gap-4 text-xs">
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Transactional SMS</h4>
            <p class="text-slate-400">24x7 instant OTP, banking alerts, booking confirmations, order delivery tracking.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Promotional SMS</h4>
            <p class="text-slate-400">High-volume sales offers, marketing discounts, event broadcasts with scheduling.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">OTP & Flash SMS</h4>
            <p class="text-slate-400">Sub-3-second priority delivery routes and direct screen popup Flash messaging.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Unicode & International</h4>
            <p class="text-slate-400">Hindi and all regional Indian languages, along with global worldwide SMS termination.</p>
          </div>
        </div>
      </div>

      <!-- 2. Omnichannel Communication & Voice -->
      <div class="bg-slate-900/60 border border-slate-800 p-6 sm:p-8 rounded-2xl">
        <div class="flex items-center gap-3 border-b border-slate-800 pb-4 mb-6">
          <i class="fa-solid fa-headset text-2xl text-emerald-400"></i>
          <div>
            <h3 class="text-xl font-bold text-white">2. WhatsApp, RCS, Voice/IVR & Cloud Communication</h3>
            <p class="text-xs text-slate-400">Interactive modern messaging channels and automated calling</p>
          </div>
        </div>
        <div class="grid sm:grid-cols-2 md:grid-cols-4 gap-4 text-xs">
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">WhatsApp Business API</h4>
            <p class="text-slate-400">Official Meta verified API, dynamic catalog sync, automated customer chatbots.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">RCS Messaging</h4>
            <p class="text-slate-400">Rich Communication Services with brand verification, carousels, and action buttons.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Voice SMS & IVR Flows</h4>
            <p class="text-slate-400">Automated bulk voice broadcasting, dynamic DTMF multi-level keypad IVR logic.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Missed Call & Numbers</h4>
            <p class="text-slate-400">Automated missed call lead capture, Virtual Numbers, Short Code & Long Code APIs.</p>
          </div>
        </div>
      </div>

      <!-- 3. Web & Application Development -->
      <div class="bg-slate-900/60 border border-slate-800 p-6 sm:p-8 rounded-2xl">
        <div class="flex items-center gap-3 border-b border-slate-800 pb-4 mb-6">
          <i class="fa-solid fa-laptop-code text-2xl text-emerald-400"></i>
          <div>
            <h3 class="text-xl font-bold text-white">3. Web, Mobile App & Portal Engineering</h3>
            <p class="text-xs text-slate-400">Modern reactive frameworks, cloud deployments, and intuitive UI/UX</p>
          </div>
        </div>
        <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-4 text-xs">
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Website Development</h4>
            <p class="text-slate-400">Business Websites, Corporate Portals, E-Commerce, Custom Landing Pages, CMS systems, Booking Platforms, Marketplace architectures, UI/UX design, Domain, Hosting & SSL security.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Mobile App Development</h4>
            <p class="text-slate-400">Native Android & iOS Apps, Flutter & React Native cross-platform apps, Fintech apps, Booking & Delivery applications, Admin Control panels, Push notifications, and continuous store maintenance.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">API Integrations</h4>
            <p class="text-slate-400">RESTful APIs, SMPP connections, Webhook callbacks, Delivery-status monitoring, and developer SDKs for Node, Python, PHP, and Java.</p>
          </div>
        </div>
      </div>

      <!-- 4. Enterprise Software & Digital Marketing -->
      <div class="bg-slate-900/60 border border-slate-800 p-6 sm:p-8 rounded-2xl">
        <div class="flex items-center gap-3 border-b border-slate-800 pb-4 mb-6">
          <i class="fa-solid fa-chart-line text-2xl text-emerald-400"></i>
          <div>
            <h3 class="text-xl font-bold text-white">4. Enterprise Software, DLT & Digital Marketing</h3>
            <p class="text-xs text-slate-400">Automation platforms, compliance support, and growth marketing</p>
          </div>
        </div>
        <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-4 text-xs">
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Custom Software & SaaS</h4>
            <p class="text-slate-400">Custom Business CRM, ERP Systems, Billing Software, Inventory Management, POS, HRMS, School Management Suites, and centralized analytics dashboards.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">DLT Regulatory Services</h4>
            <p class="text-slate-400">DLT Principal Entity registration handholding, Sender ID / Header registration, SMS Template submission, compliance audits, and renewal management.</p>
          </div>
          <div class="p-3.5 bg-slate-950/70 border border-slate-800/80 rounded-xl">
            <h4 class="font-bold text-emerald-400 mb-1">Digital Marketing & Ads</h4>
            <p class="text-slate-400">Search Engine Optimization (SEO), Google Ads, Social Media Marketing (Facebook/Instagram), B2B Lead Generation, Performance Marketing, Graphic Design & Branding.</p>
          </div>
        </div>
      </div>
    </div>
  </main>

  <!-- PAGE 3: PRICING -->
  <main id="pricing" class="page-section flex-grow py-14 max-w-7xl mx-auto px-4 sm:px-6 text-white">
    <div class="text-center mb-12">
      <span class="text-emerald-400 text-xs uppercase tracking-widest font-black">Transparent Pricing</span>
      <h2 class="text-3xl sm:text-4xl font-black mt-1">Flexible Enterprise Pricing Plans</h2>
      <p class="text-slate-400 text-xs sm:text-sm mt-2">Direct carrier interconnects with no hidden setup charges</p>
    </div>

    <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl text-center">
        <h3 class="font-bold text-base text-slate-200">Promotional SMS</h3>
        <p class="text-xs text-slate-400 mt-1 mb-4">Marketing & Mass Outreach</p>
        <div class="text-2xl font-black text-emerald-400 mb-3">Bulk Tier Rates</div>
        <p class="text-xs text-slate-400 mb-6">Clean routes, direct dynamic routing, real-time portal access included.</p>
        <button onclick="showPage('contact')" class="w-full bg-slate-800 hover:bg-slate-700 py-2.5 rounded text-xs font-bold uppercase tracking-wider transition">Inquire Rates</button>
      </div>

      <div class="bg-slate-900/90 border-2 border-emerald-500 p-6 rounded-xl text-center relative shadow-xl shadow-emerald-500/10">
        <span class="absolute -top-3 left-1/2 -translate-x-1/2 bg-emerald-500 text-slate-950 font-black text-[10px] uppercase px-2.5 py-0.5 rounded-full">Top Choice</span>
        <h3 class="font-bold text-base text-slate-200 mt-1">Transactional & OTP</h3>
        <p class="text-xs text-slate-400 mt-1 mb-4">High Priority Delivery</p>
        <div class="text-2xl font-black text-emerald-400 mb-3">Sub-Second Delivery</div>
        <p class="text-xs text-slate-400 mb-6">99.98% delivery success, dedicated carrier pipes with failover routing.</p>
        <button onclick="showPage('contact')" class="w-full bg-emerald-500 hover:bg-emerald-400 text-slate-950 py-2.5 rounded text-xs font-bold uppercase tracking-wider transition">Inquire Rates</button>
      </div>

      <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl text-center">
        <h3 class="font-bold text-base text-slate-200">WhatsApp & RCS</h3>
        <p class="text-xs text-slate-400 mt-1 mb-4">Official Meta & Telco APIs</p>
        <div class="text-2xl font-black text-emerald-400 mb-3">Pay Per Session</div>
        <p class="text-xs text-slate-400 mb-6">Rich multimedia templates, green tick assistance, chatbot support.</p>
        <button onclick="showPage('contact')" class="w-full bg-slate-800 hover:bg-slate-700 py-2.5 rounded text-xs font-bold uppercase tracking-wider transition">Inquire Rates</button>
      </div>

      <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl text-center">
        <h3 class="font-bold text-base text-slate-200">Email & Voice/IVR</h3>
        <p class="text-xs text-slate-400 mt-1 mb-4">Outbound Automation</p>
        <div class="text-2xl font-black text-emerald-400 mb-3">Custom Plans</div>
        <p class="text-xs text-slate-400 mb-6">Smart retry mechanisms, high reputation SMTP IPs, detailed logs.</p>
        <button onclick="showPage('contact')" class="w-full bg-slate-800 hover:bg-slate-700 py-2.5 rounded text-xs font-bold uppercase tracking-wider transition">Inquire Rates</button>
      </div>

      <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl text-center">
        <h3 class="font-bold text-base text-slate-200">Web, App & Custom SaaS</h3>
        <p class="text-xs text-slate-400 mt-1 mb-4">Tailor-Made Development</p>
        <div class="text-2xl font-black text-emerald-400 mb-3">Milestone Based</div>
        <p class="text-xs text-slate-400 mb-6">Full code ownership, free maintenance period, enterprise UI/UX.</p>
        <button onclick="showPage('contact')" class="w-full bg-slate-800 hover:bg-slate-700 py-2.5 rounded text-xs font-bold uppercase tracking-wider transition">Inquire Rates</button>
      </div>

      <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl text-center">
        <h3 class="font-bold text-base text-slate-200">Carrier APIs & DLT</h3>
        <p class="text-xs text-slate-400 mt-1 mb-4">REST & SMPP Endpoints</p>
        <div class="text-2xl font-black text-emerald-400 mb-3">Developer Ready</div>
        <p class="text-xs text-slate-400 mb-6">SDKs for Python, Node, PHP, Java with instant callback webhooks.</p>
        <button onclick="showPage('contact')" class="w-full bg-slate-800 hover:bg-slate-700 py-2.5 rounded text-xs font-bold uppercase tracking-wider transition">Inquire Rates</button>
      </div>
    </div>
  </main>

  <!-- PAGE 4: ABOUT US -->
  <main id="about" class="page-section flex-grow py-14 max-w-7xl mx-auto px-4 sm:px-6 text-white">
    <div class="grid md:grid-cols-2 gap-10 items-center">
      <div>
        <span class="text-emerald-400 text-xs uppercase tracking-wider font-bold">About Telecorcel</span>
        <h2 class="text-3xl sm:text-4xl font-extrabold mt-1 mb-4">Pioneering High-Quality Telecom & Enterprise IT</h2>
        <p class="text-slate-300 text-sm leading-relaxed mb-6">
          Telecorcel IT Solutions Pvt Ltd provides high-throughput telecom routing, automated messaging gateways, and bespoke web/software solutions. Operating since 2013, we serve over 20,000+ satisfied clients across multiple verticals.
        </p>

        <div class="grid sm:grid-cols-2 gap-4 mb-6">
          <div class="p-4 bg-slate-900/80 border border-slate-800 rounded-lg">
            <span class="text-[11px] text-emerald-400 uppercase font-bold block">Chief Executive Officer</span>
            <span class="text-base font-bold text-slate-100">Satyam Sharma</span>
          </div>
          <div class="p-4 bg-slate-900/80 border border-slate-800 rounded-lg">
            <span class="text-[11px] text-emerald-400 uppercase font-bold block">Sales Manager</span>
            <span class="text-base font-bold text-slate-100">Shivam Sharma</span>
          </div>
        </div>
      </div>

      <div class="border border-slate-800 rounded-xl overflow-hidden p-2 bg-slate-900/60 shadow-2xl">
        <img 
          src="telecorcel9.jpeg" 
          alt="Team at Work" 
          class="rounded-lg w-full object-cover"
          onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1522071820081-009f0129c71c?w=700&auto=format&fit=crop&q=80';"
        />
      </div>
    </div>
  </main>

  <!-- PAGE 5: CONTACT US -->
  <main id="contact" class="page-section flex-grow py-14 max-w-7xl mx-auto px-4 sm:px-6 text-white">
    <div class="text-center mb-12">
      <h2 class="text-3xl sm:text-4xl font-black">Direct Inquiry & NOC Desk</h2>
      <p class="text-slate-400 text-sm mt-2">Sector 62, Noida Headquarters & Carrier Route Operations</p>
    </div>

    <div class="grid md:grid-cols-2 gap-10">
      <div class="space-y-6">
        <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl">
          <h3 class="text-base font-bold text-white mb-4 border-b border-slate-800 pb-2">Registered Corporate Facility</h3>
          <p class="text-xs sm:text-sm text-slate-300 leading-relaxed mb-4">
            <strong>Headquarters:</strong> Block A, Industrial Area, Sector 62, Noida, Uttar Pradesh 201309.<br/>
            <span class="text-xs text-slate-400">(Additional presence listings around Sector 44 / Wazidpur in Noida)</span>
          </p>
          <div class="space-y-3 text-xs sm:text-sm text-slate-300">
            <p><i class="fa-solid fa-phone text-emerald-400 mr-2"></i> +91 9012574505</p>
            <p><i class="fa-solid fa-phone text-emerald-400 mr-2"></i> +91 7678519164</p>
            <p><i class="fa-solid fa-envelope text-emerald-400 mr-2"></i> telecorcelitsolutionshelp@gmail.com</p>
          </div>
        </div>
      </div>

      <div class="bg-slate-900/80 border border-slate-800 p-6 rounded-xl">
        <h3 class="text-base font-bold text-white mb-4">Request Live Pipeline / Pricing</h3>
        <form onsubmit="event.preventDefault(); alert('Message send ho gaya hai! Team turant contact karegi.');" class="space-y-4 text-xs sm:text-sm">
          <div>
            <label class="block text-slate-300 mb-1">Aapka Naam / Company</label>
            <input type="text" required class="w-full bg-slate-950 border border-slate-800 rounded p-2.5 text-white focus:border-emerald-500 outline-none" placeholder="Enter name" />
          </div>
          <div>
            <label class="block text-slate-300 mb-1">Contact Number</label>
            <input type="tel" required class="w-full bg-slate-950 border border-slate-800 rounded p-2.5 text-white focus:border-emerald-500 outline-none" placeholder="+91 XXXXXXXXXX" />
          </div>
          <div>
            <label class="block text-slate-300 mb-1">Service Required</label>
            <select class="w-full bg-slate-950 border border-slate-800 rounded p-2.5 text-white focus:border-emerald-500 outline-none">
              <option>Bulk SMS (Transactional / OTP / Promotional)</option>
              <option>WhatsApp API & RCS Messaging</option>
              <option>Voice SMS, IVR & Missed Call Solutions</option>
              <option>Website & Custom Web Applications</option>
              <option>Mobile App Development (Android / iOS)</option>
              <option>Enterprise CRM, ERP & Billing Software</option>
              <option>DLT Registration & Template Support</option>
              <option>Digital Marketing, SEO & Google Ads</option>
            </select>
          </div>
          <button type="submit" class="w-full bg-emerald-500 hover:bg-emerald-400 text-slate-950 font-bold py-3 rounded uppercase tracking-wider text-xs transition">Submit Inquiry</button>
        </form>
      </div>
    </div>
  </main>

  <!-- Clean Minimalist Footer -->
  <footer class="bg-[#02050a] text-slate-400 py-8 border-t border-slate-900 text-xs mt-auto">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 flex flex-col sm:flex-row justify-between items-center gap-4 text-center sm:text-left">
      <div>
        <span class="text-white font-extrabold tracking-wider">TELECORCEL IT SOLUTIONS PVT LTD</span>
        <p class="text-[11px] text-slate-500 mt-1">Sector 62, Noida, UP 201309 | CEO: Satyam Sharma | Sales Manager: Shivam Sharma</p>
      </div>
      <p class="text-[11px] text-slate-500">&copy; 2026 Telecorcel IT Solutions Pvt Ltd. All rights reserved.</p>
    </div>
  </footer>

  <!-- Scripts -->
  <script>
    function showPage(pageId) {
      document.querySelectorAll('.page-section').forEach(sec => sec.classList.remove('active'));
      const target = document.getElementById(pageId);
      if (target) {
        target.classList.add('active');
        window.scrollTo({ top: 0, behavior: 'smooth' });
      }
    }

    // Dynamic Network Canvas Hero Animation
    const canvas = document.getElementById('networkCanvas');
    const ctx = canvas.getContext('2d');
    let width, height;
    let particles = [];

    function resizeCanvas() {
      width = canvas.width = canvas.parentElement.offsetWidth;
      height = canvas.height = canvas.parentElement.offsetHeight;
    }
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    class Particle {
      constructor() {
        this.x = Math.random() * width;
        this.y = Math.random() * height;
        this.vx = (Math.random() - 0.5) * 0.9;
        this.vy = (Math.random() - 0.5) * 0.9;
        this.radius = Math.random() * 2 + 1;
      }
      update() {
        this.x += this.vx;
        this.y += this.vy;
        if (this.x < 0 || this.x > width) this.vx *= -1;
        if (this.y < 0 || this.y > height) this.vy *= -1;
      }
      draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
        ctx.fillStyle = 'rgba(52, 211, 153, 0.7)';
        ctx.fill();
      }
    }

    const particleCount = Math.min(width > 768 ? 60 : 25, 70);
    for (let i = 0; i < particleCount; i++) {
      particles.push(new Particle());
    }

    function animateNetwork() {
      ctx.clearRect(0, 0, width, height);
      for (let i = 0; i < particles.length; i++) {
        particles[i].update();
        particles[i].draw();
        for (let j = i + 1; j < particles.length; j++) {
          const dx = particles[i].x - particles[j].x;
          const dy = particles[i].y - particles[j].y;
          const dist = Math.sqrt(dx * dx + dy * dy);
          if (dist < 125) {
            ctx.beginPath();
            ctx.moveTo(particles[i].x, particles[i].y);
            ctx.lineTo(particles[j].x, particles[j].y);
            ctx.strokeStyle = `rgba(16, 185, 129, ${0.22 * (1 - dist / 125)})`;
            ctx.lineWidth = 0.8;
            ctx.stroke();
          }
        }
      }
      requestAnimationFrame(animateNetwork);
    }
    animateNetwork();

    // -------------------------------------------------------------
    // THREE.JS 3D INTERACTIVE GLOBE
    // -------------------------------------------------------------
    const globeContainer = document.getElementById('globeCanvasContainer');
    const globeCanvas = document.getElementById('globeCanvas');
    const scene = new THREE.Scene();

    const camera = new THREE.PerspectiveCamera(45, globeContainer.offsetWidth / globeContainer.offsetHeight, 0.1, 1000);
    camera.position.z = 210;

    const renderer = new THREE.WebGLRenderer({ canvas: globeCanvas, alpha: true, antialias: true });
    renderer.setSize(globeContainer.offsetWidth, globeContainer.offsetHeight);
    renderer.setPixelRatio(window.devicePixelRatio);

    const globeRadius = 68;
    const globeGroup = new THREE.Group();
    scene.add(globeGroup);

    const sphereGeo = new THREE.SphereGeometry(globeRadius, 36, 36);
    const sphereMat = new THREE.MeshBasicMaterial({
      color: 0x064e3b,
      wireframe: true,
      transparent: true,
      opacity: 0.18
    });
    const globeMesh = new THREE.Mesh(sphereGeo, sphereMat);
    globeGroup.add(globeMesh);

    const innerGeo = new THREE.SphereGeometry(globeRadius - 0.8, 32, 32);
    const innerMat = new THREE.MeshBasicMaterial({
      color: 0x02161e,
      transparent: true,
      opacity: 0.75
    });
    globeGroup.add(new THREE.Mesh(innerGeo, innerMat));

    function latLonToVector3(lat, lon, radius) {
      const phi = (90 - lat) * (Math.PI / 180);
      const theta = (lon + 180) * (Math.PI / 180);
      const x = -(radius * Math.sin(phi) * Math.cos(theta));
      const z = radius * Math.sin(phi) * Math.sin(theta);
      const y = radius * Math.cos(phi);
      return new THREE.Vector3(x, y, z);
    }

    const locations = {
      noida: { lat: 28.62, lon: 77.36, name: "India HQ" },
      usEast: { lat: 40.71, lon: -74.00, name: "US East" },
      uk: { lat: 51.50, lon: -0.12, name: "London UK" },
      dubai: { lat: 25.20, lon: 55.27, name: "UAE" },
      singapore: { lat: 1.35, lon: 103.81, name: "Singapore" },
      sydney: { lat: -33.86, lon: 151.20, name: "Australia" }
    };

    Object.keys(locations).forEach(key => {
      const loc = locations[key];
      const pos = latLonToVector3(loc.lat, loc.lon, globeRadius + 0.5);
      const markerGeo = new THREE.SphereGeometry(key === 'noida' ? 2.5 : 1.6, 16, 16);
      const markerMat = new THREE.MeshBasicMaterial({ 
        color: key === 'noida' ? 0x10b981 : 0x34d399 
      });
      const marker = new THREE.Mesh(markerGeo, markerMat);
      marker.position.copy(pos);
      globeGroup.add(marker);
    });

    function createArc(p1, p2) {
      const distance = p1.distanceTo(p2);
      const mid = p1.clone().lerp(p2, 0.5);
      const midLength = mid.length();
      mid.normalize();
      mid.multiplyScalar(midLength + distance * 0.28);

      const curve = new THREE.QuadraticBezierCurve3(p1, mid, p2);
      const points = curve.getPoints(45);
      const geometry = new THREE.BufferGeometry().setFromPoints(points);
      const material = new THREE.LineBasicMaterial({
        color: 0x34d399,
        transparent: true,
        opacity: 0.55
      });
      return new THREE.Line(geometry, material);
    }

    const noidaPos = latLonToVector3(locations.noida.lat, locations.noida.lon, globeRadius);
    ['usEast', 'uk', 'dubai', 'singapore', 'sydney'].forEach(key => {
      const destPos = latLonToVector3(locations[key].lat, locations[key].lon, globeRadius);
      globeGroup.add(createArc(noidaPos, destPos));
    });

    let isDragging = false;
    let previousMousePosition = { x: 0, y: 0 };

    globeCanvas.addEventListener('mousedown', () => isDragging = true);
    window.addEventListener('mouseup', () => isDragging = false);

    globeCanvas.addEventListener('mousemove', (e) => {
      if (isDragging) {
        const deltaX = e.clientX - previousMousePosition.x;
        const deltaY = e.clientY - previousMousePosition.y;
        globeGroup.rotation.y += deltaX * 0.007;
        globeGroup.rotation.x += deltaY * 0.007;
      }
      previousMousePosition = { x: e.clientX, y: e.clientY };
    });

    globeCanvas.addEventListener('touchstart', (e) => {
      isDragging = true;
      previousMousePosition = { x: e.touches[0].clientX, y: e.touches[0].clientY };
    });
    window.addEventListener('touchend', () => isDragging = false);
    globeCanvas.addEventListener('touchmove', (e) => {
      if (isDragging && e.touches.length > 0) {
        const deltaX = e.touches[0].clientX - previousMousePosition.x;
        const deltaY = e.touches[0].clientY - previousMousePosition.y;
        globeGroup.rotation.y += deltaX * 0.007;
        globeGroup.rotation.x += deltaY * 0.007;
        previousMousePosition = { x: e.touches[0].clientX, y: e.touches[0].clientY };
      }
    });

    window.addEventListener('resize', () => {
      if (!globeContainer) return;
      camera.aspect = globeContainer.offsetWidth / globeContainer.offsetHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(globeContainer.offsetWidth, globeContainer.offsetHeight);
    });

    function renderGlobe() {
      requestAnimationFrame(renderGlobe);
      if (!isDragging) {
        globeGroup.rotation.y += 0.0035;
      }
      renderer.render(scene, camera);
    }
    renderGlobe();
  </script>
</body>
</html>
