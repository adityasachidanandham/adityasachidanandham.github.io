<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Aditya Sachidanandham | PMP® Portfolio</title>
    
    <!-- Preload critical resources -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="preconnect" href="https://cdn.tailwindcss.com">
    <link rel="preconnect" href="https://cdnjs.cloudflare.com">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap');
        
        /* Optimize rendering */
        html {
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }
        
        :root {
            /* Blue Eclipse Palette */
            --eclipse-1: #272757; /* Primary */
            --eclipse-2: #8686AC; /* Light */
            --eclipse-3: #505081; /* Medium */
            --eclipse-4: #0F0E47; /* Deep */
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #ffffff;
            color: var(--eclipse-4);
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
            width: 100%;
            text-rendering: optimizeLegibility;
            -webkit-font-smoothing: antialiased;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 72px;
        }

        /* Restoration: Scroll Reveal Animation - Optimized */
        .reveal {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.8s cubic-bezier(0.2, 1, 0.3, 1);
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Show hero content immediately */
        .reveal-immediate {
            opacity: 1 !important;
            transform: translateY(0) !important;
        }

        /* Restoration: Background Blobs */
        .blob {
            position: fixed;
            background: var(--eclipse-2);
            filter: blur(100px);
            border-radius: 50%;
            z-index: -1;
            opacity: 0.12;
            pointer-events: none;
            will-change: transform;
            transform: translate3d(0, 0, 0);
        }

        .main-content {
            width: 100%;
            max-width: 640px;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 0 24px;
            position: relative;
            z-index: 1;
            isolation: isolate;
        }

        /* Fixed Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 9999;
            background-color: rgba(255, 255, 255, 0.98);
            backdrop-filter: saturate(180%) blur(20px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            height: 72px;
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 0 24px;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            overflow: hidden;
        }

        .nav-inner {
            width: 100%;
            max-width: 640px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-badge {
            text-align: left;
            flex-shrink: 0;
        }

        .hero-section {
            margin-top: 50px;
            text-align: center;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            z-index: 1;
        }
        
        .hero-section .reveal {
            will-change: auto;
        }

        .section-header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            width: 100%;
            margin-bottom: 2rem;
        }

        .section-title {
            font-size: 1.75rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: -0.05em;
            line-height: 1.1;
        }

        .section-divider {
            width: 40px;
            height: 4px;
            background-color: var(--eclipse-2);
            margin-top: 0.75rem;
            border-radius: 99px;
            opacity: 0.3;
        }

        /* FIX 3: Reduced spacing for PMP badge */
        .pmp-badge-hero {
            padding-top: 1mm;
            padding-bottom: 1mm;
        }

        /* Nexus Button System */
        .nexus-btn {
            width: 110px; height: 110px;
            transition: all 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
            display: flex; align-items: center; justify-content: center;
            border-radius: 3rem; cursor: pointer; z-index: 20;
            touch-action: manipulation;
            box-shadow: 0 25px 50px -12px rgba(39, 39, 87, 0.25);
            border: none;
            outline: none;
        }
        .nexus-btn:active { transform: scale(0.92); }
        .nexus-btn.active { transform: rotate(90deg); background-color: #ef4444 !important; box-shadow: 0 25px 50px -12px rgba(239, 68, 68, 0.25); }

        .exp-container {
            max-height: 0; 
            overflow: hidden;
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
            opacity: 0; 
            width: 100%;
            pointer-events: none;
        }
        .exp-container.show { 
            max-height: 2500px; 
            opacity: 1; 
            margin-top: 2.5rem; 
            pointer-events: auto;
        }

        .glass-card {
            background: rgba(248, 250, 252, 0.8);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(241, 245, 249, 1);
            width: 100%;
            transition: transform 0.3s ease;
        }

        .apple-card {
            background: #fbfbfd;
            border-radius: 28px;
            border: 1px solid rgba(0,0,0,0.04);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .apple-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.06);
        }

        .pmp-badge-container {
            background: linear-gradient(135deg, var(--eclipse-1) 0%, var(--eclipse-4) 100%);
            width: 70px;
            height: 70px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            box-shadow: 0 10px 20px rgba(39, 39, 87, 0.25);
        }

        .pulse-wave { animation: pulse 2.5s cubic-bezier(0.4, 0, 0.6, 1) infinite; }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(39, 39, 87, 0.4); }
            70% { box-shadow: 0 0 0 25px rgba(39, 39, 87, 0); }
            100% { box-shadow: 0 0 0 0 rgba(39, 39, 87, 0); }
        }

        .no-scrollbar::-webkit-scrollbar { display: none; }

        .sim-card {
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            height: auto;
            min-height: 360px;
            display: flex;
            flex-direction: column;
            width: 100%;
            border: 1px solid #f1f5f9;
        }
        .sim-card.active-solving { 
            border-color: var(--eclipse-1); 
            background: #f0f0ff; 
            transform: scale(1.02);
        }
        
        @keyframes icon-shake {
            0%, 80%, 100% { transform: translateX(0); }
            85% { transform: translateX(-3px) rotate(-2deg); }
            90% { transform: translateX(3px) rotate(2deg); }
            95% { transform: translateX(-2px) rotate(-1deg); }
        }
        .shake-icon { animation: icon-shake 4s ease-in-out infinite; }

        .progress-bar {
            height: 6px;
            background: #e2e8f0;
            border-radius: 99px;
            overflow: hidden;
            margin: 2rem 0;
            width: 100%;
        }

        .progress-fill {
            height: 100%;
            background: var(--eclipse-1);
            width: 0%;
            transition: width 0.1s linear;
        }

        /* FIX 4: Larger simulator text (30% increase) */
        .simulator-text {
            font-size: 15.6px; /* 12px * 1.3 */
        }

        .simulator-problem-text {
            font-size: 15.6px; /* 12px * 1.3 */
        }
    </style>
</head>
<body class="pb-24 no-scrollbar">

    <!-- Restoration: Background blobs -->
    <div class="blob" style="width: 450px; height: 450px; top: -150px; right: -150px;"></div>
    <div class="blob" style="width: 350px; height: 350px; bottom: 5%; left: -120px;"></div>

    <nav>
        <div class="nav-inner">
            <div class="nav-badge text-[10px] font-black tracking-[0.3em] text-[var(--eclipse-1)] uppercase">PMP® CERTIFIED</div>
            <div class="flex gap-3">
                <!-- UPDATED: LinkedIn Link -->
                <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" rel="noopener noreferrer" class="haptic-btn w-11 h-11 rounded-2xl bg-white flex items-center justify-center border border-slate-200 text-[var(--eclipse-1)] active:scale-90 transition-all shadow-sm">
                    <i class="fa-brands fa-linkedin-in text-base"></i>
                </a>
                <!-- UPDATED: WhatsApp Link -->
                <a href="https://wa.me/qr/NTQZ4PIDDIN3N1" target="_blank" rel="noopener noreferrer" class="haptic-btn w-11 h-11 rounded-2xl bg-white flex items-center justify-center border border-emerald-100 text-emerald-600 active:scale-90 transition-all shadow-sm">
                    <i class="fa-brands fa-whatsapp text-xl"></i>
                </a>
            </div>
        </div>
    </nav>

    <main class="main-content">
        <!-- Hero (Wrapped in reveal) -->
        <section class="hero-section"> 
            <div class="reveal reveal-immediate">
                <div class="pmp-badge-hero inline-flex px-4 py-1.5 bg-[var(--eclipse-2)]/10 border border-[var(--eclipse-2)]/20 rounded-full text-[10px] font-black text-[var(--eclipse-1)] uppercase tracking-[0.15em] mb-6">
                    Project Management Professional
                </div>
                <!-- FIX 2: Made name bolder with font-weight: 950 equivalent -->
                <h1 class="text-5xl sm:text-6xl tracking-tighter uppercase leading-[0.9] mb-8 text-[var(--eclipse-4)]" style="font-weight: 950;">
                    Aditya<br><span class="text-[var(--eclipse-1)]">Sachidanandham</span>
                </h1>
                <!-- UPDATED: Text layout adjusted for 2 rows -->
                <p class="text-[var(--eclipse-3)] text-[14px] font-bold leading-relaxed mb-12 max-w-md tracking-tight mx-auto">
                    Delivering $50M+ semiconductor automation projects with<br>flawless execution and measurable impact.
                </p>

                <div class="grid grid-cols-3 gap-4 mb-16 w-full">
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center justify-center shadow-sm">
                        <i class="fa-solid fa-briefcase text-[var(--eclipse-1)] mb-2.5 text-base"></i>
                        <div class="text-2xl font-black text-[var(--eclipse-4)] leading-none">$50M+</div>
                        <div class="text-[8px] font-black text-[var(--eclipse-2)] uppercase tracking-widest mt-2">Portfolio</div>
                    </div>
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center justify-center shadow-sm">
                        <!-- UPDATED: Changed icon color from emerald-500 to var(--eclipse-4) to match text -->
                        <i class="fa-solid fa-circle-check text-[var(--eclipse-4)] mb-2.5 text-base"></i>
                        <div class="text-2xl font-black text-[var(--eclipse-4)] leading-none">98%</div>
                        <div class="text-[8px] font-black text-[var(--eclipse-2)] uppercase tracking-widest mt-2">On-Time</div>
                    </div>
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center justify-center shadow-sm">
                        <i class="fa-solid fa-arrow-trend-up text-[var(--eclipse-1)] mb-2.5 text-base"></i>
                        <div class="text-2xl font-black text-[var(--eclipse-4)] leading-none">11%</div>
                        <div class="text-[8px] font-black text-[var(--eclipse-2)] uppercase tracking-widest mt-2">Efficiency</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience -->
        <section class="pt-4 pb-8 w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <div class="section-header">
                    <h2 class="section-title text-[var(--eclipse-1)]">Experience</h2>
                    <div class="section-divider"></div>
                </div>
                
                <button id="expBtn" onclick="toggleSection('exp')" class="haptic-btn nexus-btn bg-[var(--eclipse-1)] pulse-wave">
                    <i id="expIcon" class="fa-solid fa-briefcase text-4xl text-white shake-icon"></i>
                </button>

                <div id="expContent" class="exp-container space-y-6">
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-[var(--eclipse-1)] shadow-lg shadow-[var(--eclipse-4)]/5">
                        <div class="text-[var(--eclipse-1)] font-black text-[10px] mb-4 uppercase tracking-[0.2em]">Mar 2025 — Jan 2026</div>
                        <h3 class="text-2xl font-black uppercase tracking-tight text-[var(--eclipse-4)]">Installation Manager</h3>
                        <p class="text-xs font-bold text-[var(--eclipse-2)] mb-6 uppercase">STMicroelectronics</p>
                        <p class="text-[14px] text-[var(--eclipse-3)] font-bold leading-relaxed uppercase">• Led $20M automation project coordinating 100+ subcontractors.</p>
                    </div>
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-slate-200 shadow-sm">
                        <div class="text-slate-400 font-black text-[10px] mb-4 uppercase tracking-[0.2em]">Aug 2024 — Feb 2025</div>
                        <h3 class="text-2xl font-black uppercase tracking-tight text-[var(--eclipse-4)]">Site Manager</h3>
                        <p class="text-xs font-bold text-slate-400 mb-6 uppercase">Texas Instruments</p>
                        <p class="text-[14px] text-slate-600 font-bold leading-relaxed uppercase">• $50M On-site execution management with 31% faster resolution.</p>
                    </div>
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-slate-200 shadow-sm">
                        <div class="text-slate-400 font-black text-[10px] mb-4 uppercase tracking-[0.2em]">Jul 2022 — Jul 2024</div>
                        <h3 class="text-2xl font-black uppercase tracking-tight text-[var(--eclipse-4)]">Engineer</h3>
                        <p class="text-xs font-bold text-slate-400 mb-6 uppercase">UMC, Soitec, Siltronic</p>
                        <p class="text-[14px] text-slate-600 font-bold leading-relaxed uppercase">• Collaborated on 5 complex $12M+ projects leading risk mitigation.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Simulator -->
        <section class="py-6 w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <div class="section-header">
                    <h2 class="section-title text-[var(--eclipse-4)]">The Simulator</h2>
                    <div class="section-divider"></div>
                    <p class="simulator-text text-[11px] font-black text-[var(--eclipse-2)] uppercase tracking-[0.25em] mt-4">Interactive Problem Solving</p>
                </div>

                <div class="space-y-6 w-full">
                    <!-- Sim 1 -->
                    <div id="sim-card-1" class="sim-card glass-card p-8 py-12 rounded-[3rem] text-center flex flex-col items-center shadow-sm">
                        <div id="status-icon-1" class="w-16 h-16 rounded-3xl bg-amber-50 text-amber-500 flex items-center justify-center mb-10 transition-all duration-500">
                            <i class="fa-solid fa-users-gear text-2xl"></i>
                        </div>
                        <h3 class="simulator-text font-black text-[var(--eclipse-1)] uppercase tracking-[0.2em] mb-4">Oversight Dilution</h3>
                        <div id="problem-text-1" class="simulator-problem-text font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-4">
                            Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.
                        </div>
                        <div class="progress-bar">
                            <div id="progress-1" class="progress-fill"></div>
                        </div>
                        <button onclick="handleSimulation(1)" id="sim-btn-1" data-state="initial" class="haptic-btn w-full py-5 bg-[var(--eclipse-4)] text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg">
                            Resolve Issue
                        </button>
                    </div>

                    <!-- Sim 2 -->
                    <div id="sim-card-2" class="sim-card glass-card p-8 py-12 rounded-[3rem] text-center flex flex-col items-center shadow-sm">
                        <div id="status-icon-2" class="w-16 h-16 rounded-3xl bg-amber-50 text-amber-500 flex items-center justify-center mb-10 transition-all duration-500">
                            <i class="fa-solid fa-microchip text-2xl"></i>
                        </div>
                        <h3 class="simulator-text font-black text-[var(--eclipse-1)] uppercase tracking-[0.2em] mb-4">Technical Latency</h3>
                        <div id="problem-text-2" class="simulator-problem-text font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-4">
                            $50M facility launch delay stalls client revenue-generation and eats capital investment.
                        </div>
                        <div class="progress-bar">
                            <div id="progress-2" class="progress-fill"></div>
                        </div>
                        <button onclick="handleSimulation(2)" id="sim-btn-2" data-state="initial" class="haptic-btn w-full py-5 bg-[var(--eclipse-4)] text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg">
                            Resolve Issue
                        </button>
                    </div>

                    <!-- Sim 3 -->
                    <div id="sim-card-3" class="sim-card glass-card p-8 py-12 rounded-[3rem] text-center flex flex-col items-center shadow-sm">
                        <div id="status-icon-3" class="w-16 h-16 rounded-3xl bg-amber-50 text-amber-500 flex items-center justify-center mb-10 transition-all duration-500">
                            <i class="fa-solid fa-layer-group text-2xl"></i>
                        </div>
                        <h3 class="simulator-text font-black text-[var(--eclipse-1)] uppercase tracking-[0.2em] mb-4">Resource Fragmentation</h3>
                        <div id="problem-text-3" class="simulator-problem-text font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-4">
                            Directing 5 simultaneous $12M sites creating a "domino effect" where one crisis drains all resources.
                        </div>
                        <div class="progress-bar">
                            <div id="progress-3" class="progress-fill"></div>
                        </div>
                        <button onclick="handleSimulation(3)" id="sim-btn-3" data-state="initial" class="haptic-btn w-full py-5 bg-[var(--eclipse-4)] text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg">
                            Resolve Issue
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Academics -->
        <section class="py-6 w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <div class="section-header">
                    <h2 class="section-title text-[var(--eclipse-1)]">Academics</h2>
                    <div class="section-divider"></div>
                </div>

                <button id="acadBtn" onclick="toggleSection('acad')" class="haptic-btn nexus-btn bg-[var(--eclipse-4)] pulse-wave">
                    <i id="acadIcon" class="fa-solid fa-graduation-cap text-4xl text-white shake-icon"></i>
                </button>

                <div id="acadContent" class="exp-container space-y-6">
                    <div class="glass-card p-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                        <i class="fa-solid fa-graduation-cap text-[var(--eclipse-1)] mb-6 text-2xl"></i>
                        <h4 class="text-2xl font-black uppercase text-[var(--eclipse-4)] leading-tight">M.Sc Project Management</h4>
                        <p class="text-[11px] font-black text-[var(--eclipse-2)] uppercase mt-4 tracking-[0.25em]">NTU Singapore | GPA: 4.14</p>
                    </div>
                    <div class="glass-card p-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                        <i class="fa-solid fa-user-graduate text-slate-400 mb-6 text-2xl"></i>
                        <h4 class="text-2xl font-black uppercase text-[var(--eclipse-4)] leading-tight">B.Tech Aerospace</h4>
                        <p class="text-[11px] font-black text-slate-400 uppercase mt-4 tracking-[0.25em]">PM Institute | GPA: 4.07</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- PMP Apple Section -->
        <section class="mt-6 mb-4 w-full">
            <div class="reveal">
                <div class="apple-card w-full p-8 flex flex-col sm:flex-row items-center gap-8">
                    <div class="pmp-badge-container flex-shrink-0">
                        <div class="absolute inset-0 border-2 border-white/20 rounded-2xl"></div>
                        <div class="text-center">
                            <div class="text-[10px] font-black text-white/90 leading-none">PMP</div>
                            <i class="fa-solid fa-award text-white text-2xl my-1"></i>
                            <div class="text-[7px] font-bold text-white/70 uppercase">Verified</div>
                        </div>
                    </div>

                    <div class="flex-grow text-center sm:text-left">
                        <div class="flex items-center justify-center sm:justify-start gap-3 mb-2">
                            <span class="text-[10px] font-black text-[var(--eclipse-1)] uppercase tracking-[0.2em]">Credentialed</span>
                            <div class="hidden sm:block h-[1px] flex-grow bg-slate-100"></div>
                        </div>
                        <h3 class="text-xl font-black text-[var(--eclipse-4)] uppercase leading-tight mb-2">Project Management Professional</h3>
                        <p class="text-[11px] text-[var(--eclipse-2)] font-bold uppercase tracking-wider">Cert #4181149 • 2025–2028</p>
                    </div>

                    <a href="https://drive.google.com/file/d/1GSi6xrRhk8LBgboyArKdwgUpK0te4lGS/view?usp=sharing" target="_blank" rel="noopener noreferrer" class="haptic-btn w-12 h-12 rounded-full bg-slate-100 flex items-center justify-center text-[var(--eclipse-4)] hover:bg-[var(--eclipse-1)] hover:text-white transition-all flex-shrink-0">
                        <i class="fa-solid fa-arrow-up-right-from-square text-sm"></i>
                    </a>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="py-12 text-center w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <h2 class="text-5xl font-black uppercase tracking-tighter text-[var(--eclipse-4)] mb-10 leading-[0.9]">Ready to<br><span class="text-[var(--eclipse-1)]">Optimise?</span></h2>
                <div class="flex flex-col sm:flex-row gap-6 w-full max-w-sm">
                    <!-- UPDATED: Let's Connect Email -->
                    <a href="mailto:sachidanandhamaditya@gmail.com" class="haptic-btn flex-1 py-6 bg-[var(--eclipse-1)] text-white rounded-full font-black text-[11px] uppercase tracking-[0.25em] shadow-2xl shadow-[var(--eclipse-1)]/30 active:scale-95 transition-all text-center">
                        Let's Connect
                    </a>
                    <!-- UPDATED: CV Download Link -->
                    <a href="https://drive.google.com/uc?export=download&id=1ECTxz4eec13It0jeHqNBNY9TgmaTa1JP" download target="_blank" class="haptic-btn flex-1 py-6 bg-[var(--eclipse-4)] text-white rounded-full font-black text-[11px] uppercase tracking-[0.25em] shadow-2xl shadow-[var(--eclipse-4)]/30 active:scale-95 transition-all text-center">
                        CV Download
                    </a>
                </div>
                <p class="mt-20 text-[9px] font-black text-slate-300 uppercase tracking-[0.4em]">© 2025 Aditya Sachidanandham</p>
            </div>
        </footer>
    </main>

    <script>
        // Optimize initial page load - defer non-critical scripts
        window.addEventListener('load', function() {
            initializeAnimations();
        });

        function initializeAnimations() {
            // FIX 6: Haptic feedback for all clickable buttons
            function triggerHaptic() {
                if (window.navigator && window.navigator.vibrate) {
                    window.navigator.vibrate(10); // 10ms vibration
                }
            }

            // Add haptic feedback to all buttons with haptic-btn class
            const hapticElements = document.querySelectorAll('.haptic-btn, button, a[href]');
            hapticElements.forEach(element => {
                element.addEventListener('touchstart', triggerHaptic, { passive: true });
                element.addEventListener('click', triggerHaptic);
            });

            // FIX 5: Restoration: Intersection Observer for Scroll Reveal Animation (works on iPhone)
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('active');
                    }
                });
            }, { threshold: 0.1, rootMargin: '0px' });

            document.querySelectorAll('.reveal:not(.reveal-immediate)').forEach(el => observer.observe(el));
        }

        // Critical functions available immediately
        const initialProblems = {
            1: { text: "Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.", icon: 'fa-users-gear' },
            2: { text: "$50M facility launch delay stalls client revenue-generation and eats capital investment.", icon: 'fa-microchip' },
            3: { text: "Directing 5 simultaneous $12M sites creating a \"domino effect\" where one crisis drains all resources.", icon: 'fa-layer-group' }
        };

        const solutions = {
            1: "Integrated Critical Path Method (CPM) with client production flows, securing a 98% on-time delivery rate.",
            2: "Deployed data-driven Root Cause Analysis (RCA), cutting issue response time by 31%.",
            3: "Centralized portfolio-wide scheduling to ensure all 5 sites met integration standards without resource shortages."
        };

        function toggleSection(type) {
            const btn = document.getElementById(type + 'Btn');
            const icon = document.getElementById(type + 'Icon');
            const content = document.getElementById(type + 'Content');
            const isClosing = btn.classList.contains('active');
            
            btn.classList.toggle('active');
            content.classList.toggle('show');
            
            const originalIcons = { exp: 'fa-briefcase', acad: 'fa-graduation-cap' };
            if (!isClosing) {
                icon.className = 'fa-solid fa-xmark text-4xl text-white';
                setTimeout(() => {
                    content.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' });
                }, 500);
            } else {
                icon.className = `fa-solid ${originalIcons[type]} text-4xl text-white shake-icon`;
            }
        }

        function handleSimulation(id) {
            const btn = document.getElementById(`sim-btn-${id}`);
            const state = btn.getAttribute('data-state');
            if (state === 'initial') runSimulation(id);
            else if (state === 'deployed') resetSimulation(id);
        }

        function runSimulation(id) {
            const card = document.getElementById(`sim-card-${id}`);
            const btn = document.getElementById(`sim-btn-${id}`);
            const progress = document.getElementById(`progress-${id}`);
            const text = document.getElementById(`problem-text-${id}`);
            const statusIcon = document.getElementById(`status-icon-${id}`);

            card.classList.add('active-solving');
            btn.disabled = true;
            btn.innerText = "SIMULATING...";

            let width = 0;
            const step = 2; 
            const interval = setInterval(() => {
                width += step;
                progress.style.width = width + '%';
                
                if (width >= 100) {
                    clearInterval(interval);
                    btn.disabled = false;
                    btn.innerText = "RESET SIMULATOR";
                    btn.setAttribute('data-state', 'deployed');
                    btn.className = "haptic-btn w-full py-5 bg-emerald-500 text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg";
                    
                    text.innerText = solutions[id];
                    text.className = "simulator-problem-text font-black text-emerald-600 uppercase leading-relaxed flex items-center justify-center min-h-[80px] px-4";
                    
                    statusIcon.className = "w-16 h-16 rounded-3xl bg-emerald-50 text-emerald-500 flex items-center justify-center mb-10 transition-all duration-500";
                    statusIcon.innerHTML = '<i class="fa-solid fa-check-double text-2xl"></i>';
                }
            }, 30);
        }

        function resetSimulation(id) {
            const card = document.getElementById(`sim-card-${id}`);
            const btn = document.getElementById(`sim-btn-${id}`);
            const progress = document.getElementById(`progress-${id}`);
            const text = document.getElementById(`problem-text-${id}`);
            const statusIcon = document.getElementById(`status-icon-${id}`);

            card.classList.remove('active-solving');
            btn.innerText = "Resolve Issue";
            btn.setAttribute('data-state', 'initial');
            btn.className = "haptic-btn w-full py-5 bg-[var(--eclipse-4)] text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg";
            
            progress.style.width = '0%';
            text.innerText = initialProblems[id].text;
            text.className = "simulator-problem-text font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-4";
            
            statusIcon.className = "w-16 h-16 rounded-3xl bg-amber-50 text-amber-500 flex items-center justify-center mb-10";
            statusIcon.innerHTML = `<i class="fa-solid ${initialProblems[id].icon} text-2xl"></i>`;
        }
    </script>
</body>
</html>
