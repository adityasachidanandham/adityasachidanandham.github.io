<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Aditya Sachidanandham | PMP® Portfolio</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300;1,600&display=swap');
        
        :root {
            --paper: #f9f7f2;
            --ink: #0f172a;
            --clay: #e0d8cc;
            --accent: #005bb7;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--paper);
            color: var(--ink);
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
            width: 100%;
            text-rendering: optimizeLegibility;
            -webkit-font-smoothing: antialiased;
            display: flex;
            flex-direction: column;
            align-items: center;
            scroll-behavior: smooth;
        }

        .serif { font-family: 'Cormorant Garamond', serif; }

        /* Scroll Reveal Animation */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            filter: blur(4px);
            transition: all 1s cubic-bezier(0.25, 1, 0.5, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
            filter: blur(0px);
        }

        /* Dynamic Background Blobs */
        .blob {
            position: fixed;
            background: var(--clay);
            filter: blur(100px);
            border-radius: 50%;
            z-index: -1;
            opacity: 0.4;
            pointer-events: none;
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
        }

        /* Fixed Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 100;
            background: rgba(249, 247, 242, 0.85);
            backdrop-filter: saturate(180%) blur(20px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            height: 72px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 24px;
        }

        .hero-section {
            margin-top: 140px;
            text-align: center;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
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
            background-color: var(--clay);
            margin-top: 0.75rem;
            border-radius: 99px;
        }

        /* Nexus Button System */
        .nexus-btn {
            width: 110px; height: 110px;
            transition: all 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
            display: flex; align-items: center; justify-content: center;
            border-radius: 3rem; cursor: pointer; z-index: 20;
            touch-action: manipulation;
            box-shadow: 0 25px 50px -12px rgba(0, 91, 183, 0.25);
            border: none;
            outline: none;
            background: var(--ink);
        }
        .nexus-btn:active { transform: scale(0.92); }
        .nexus-btn.active { transform: rotate(90deg); background-color: var(--accent) !important; }

        .exp-container {
            max-height: 0; 
            overflow: hidden;
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
            opacity: 0; 
            width: 100%;
        }
        .exp-container.show { 
            max-height: 2500px; 
            opacity: 1; 
            margin-top: 2.5rem; 
        }

        .glass-card {
            background: #ffffff;
            border: 1px solid rgba(0,0,0,0.06);
            width: 100%;
            box-shadow: 0 4px 20px rgba(0,0,0,0.02);
        }

        .apple-card {
            background: #ffffff;
            border-radius: 28px;
            border: 1px solid rgba(0,0,0,0.08);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .pmp-badge-container {
            background: var(--accent);
            width: 70px;
            height: 70px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            box-shadow: 0 10px 20px rgba(0, 91, 183, 0.25);
        }

        .pulse-wave { animation: pulse 2.5s cubic-bezier(0.4, 0, 0.6, 1) infinite; }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(0, 91, 183, 0.4); }
            70% { box-shadow: 0 0 0 25px rgba(0, 91, 183, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 91, 183, 0); }
        }

        .sim-card {
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            height: auto;
            min-height: 360px;
            display: flex;
            flex-direction: column;
            width: 100%;
        }
        .sim-card.active-solving { 
            border-color: var(--accent); 
            background: #eff6ff; 
            transform: scale(1.02);
        }
        
        .shake-icon { animation: shake 4s ease-in-out infinite; }
        @keyframes shake {
            0%, 80%, 100% { transform: translateX(0); }
            85% { transform: translateX(-3px); }
            90% { transform: translateX(3px); }
        }

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
            background: var(--accent);
            width: 0%;
            transition: width 0.1s linear;
        }

        .no-scrollbar::-webkit-scrollbar { display: none; }
    </style>
</head>
<body class="pb-24 no-scrollbar">

    <!-- Background Elements -->
    <div class="blob" id="blob-1" style="width: 400px; height: 400px; top: -100px; right: -100px;"></div>
    <div class="blob" id="blob-2" style="width: 300px; height: 300px; bottom: 10%; left: -100px;"></div>

    <nav>
        <div class="text-[10px] font-black tracking-[0.3em] text-[var(--accent)] uppercase">PMP® CERTIFIED</div>
        <div class="flex gap-3">
            <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" class="w-11 h-11 rounded-2xl bg-white flex items-center justify-center border border-slate-200 text-blue-600 active:scale-90 transition-all shadow-sm">
                <i class="fa-brands fa-linkedin-in text-base"></i>
            </a>
            <a href="https://wa.me/qr/NTQZ4PIDDIN3N1" target="_blank" class="w-11 h-11 rounded-2xl bg-white flex items-center justify-center border border-emerald-100 text-emerald-600 active:scale-90 transition-all shadow-sm">
                <i class="fa-brands fa-whatsapp text-xl"></i>
            </a>
        </div>
    </nav>

    <main class="main-content">
        <!-- Hero -->
        <section class="hero-section"> 
            <div class="reveal">
                <div class="inline-flex px-4 py-1.5 bg-blue-50 border border-blue-100 rounded-full text-[10px] font-black text-[var(--accent)] uppercase tracking-[0.15em] mb-6">
                    Project Management Professional
                </div>
                <h1 class="text-5xl sm:text-6xl font-black tracking-tighter uppercase leading-[0.9] mb-8 text-slate-900">
                    Aditya<br><span class="text-[var(--accent)]">Sachidanandham</span>
                </h1>
                <p class="text-slate-700 text-[13px] font-bold leading-relaxed mb-12 max-w-sm uppercase tracking-tight mx-auto">
                    3+ years delivering $50M+ automation installation projects for semiconductor leaders.
                </p>

                <div class="grid grid-cols-3 gap-4 mb-16 w-full">
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center justify-center shadow-sm">
                        <i class="fa-solid fa-briefcase text-[var(--accent)] mb-2.5 text-base"></i>
                        <div class="text-2xl font-black text-slate-900 leading-none">$50M+</div>
                        <div class="text-[8px] font-black text-slate-400 uppercase tracking-widest mt-2">Portfolio</div>
                    </div>
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center justify-center shadow-sm">
                        <i class="fa-solid fa-circle-check text-emerald-600 mb-2.5 text-base"></i>
                        <div class="text-2xl font-black text-slate-900 leading-none">98%</div>
                        <div class="text-[8px] font-black text-slate-400 uppercase tracking-widest mt-2">On-Time</div>
                    </div>
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center justify-center shadow-sm">
                        <i class="fa-solid fa-arrow-trend-up text-[var(--accent)] mb-2.5 text-base"></i>
                        <div class="text-2xl font-black text-slate-900 leading-none">11%</div>
                        <div class="text-[8px] font-black text-slate-400 uppercase tracking-widest mt-2">Efficiency</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience -->
        <section class="pt-4 pb-16 w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <div class="section-header">
                    <h2 class="section-title text-[var(--accent)]">Experience</h2>
                    <div class="section-divider"></div>
                </div>
                
                <button id="expBtn" onclick="toggleSection('exp')" class="nexus-btn pulse-wave">
                    <i id="expIcon" class="fa-solid fa-briefcase text-4xl text-white shake-icon"></i>
                </button>

                <div id="expContent" class="exp-container space-y-6">
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-[var(--accent)]">
                        <div class="text-[var(--accent)] font-black text-[10px] mb-4 uppercase tracking-[0.2em]">Mar 2025 — Jan 2026</div>
                        <h3 class="text-2xl font-black uppercase tracking-tight text-slate-900">Installation Manager</h3>
                        <p class="text-xs font-bold text-slate-400 mb-6 uppercase">STMicroelectronics</p>
                        <p class="text-[14px] text-slate-700 font-bold leading-relaxed uppercase">• Led $20M automation project coordinating 100+ subcontractors.</p>
                    </div>
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-slate-200">
                        <div class="text-slate-400 font-black text-[10px] mb-4 uppercase tracking-[0.2em]">Aug 2024 — Feb 2025</div>
                        <h3 class="text-2xl font-black uppercase tracking-tight text-slate-900">Site Manager</h3>
                        <p class="text-xs font-bold text-slate-400 mb-6 uppercase">Texas Instruments</p>
                        <p class="text-[14px] text-slate-700 font-bold leading-relaxed uppercase">• $50M On-site execution management with 31% faster resolution.</p>
                    </div>
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-slate-200">
                        <div class="text-slate-400 font-black text-[10px] mb-4 uppercase tracking-[0.2em]">Jul 2022 — Jul 2024</div>
                        <h3 class="text-2xl font-black uppercase tracking-tight text-slate-900">Engineer</h3>
                        <p class="text-xs font-bold text-slate-400 mb-6 uppercase">UMC, Soitec, Siltronic</p>
                        <p class="text-[14px] text-slate-700 font-bold leading-relaxed uppercase">• Collaborated on 5 complex $12M+ projects leading risk mitigation.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Simulator -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <div class="section-header">
                    <h2 class="section-title text-slate-900">The Simulator</h2>
                    <div class="section-divider"></div>
                    <p class="text-[11px] font-black text-slate-500 uppercase tracking-[0.25em] mt-4">Interactive Problem Solving</p>
                </div>

                <div class="space-y-6 w-full">
                    <!-- Sim 1 -->
                    <div id="sim-card-1" class="sim-card glass-card p-8 py-12 rounded-[3rem] text-center flex flex-col items-center shadow-sm">
                        <div id="status-icon-1" class="w-16 h-16 rounded-3xl bg-amber-50 text-amber-600 flex items-center justify-center mb-10 transition-all duration-500">
                            <i class="fa-solid fa-users-gear text-2xl"></i>
                        </div>
                        <h3 class="text-[12px] font-black text-[var(--accent)] uppercase tracking-[0.2em] mb-4">Oversight Dilution</h3>
                        <div id="problem-text-1" class="text-xs font-bold text-slate-900 uppercase leading-relaxed min-h-[60px] px-4">
                            Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.
                        </div>
                        <div class="progress-bar">
                            <div id="progress-1" class="progress-fill"></div>
                        </div>
                        <button onclick="handleSimulation(1)" id="sim-btn-1" data-state="initial" class="w-full py-5 bg-slate-900 text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg">
                            Resolve Issue
                        </button>
                    </div>

                    <!-- Sim 2 -->
                    <div id="sim-card-2" class="sim-card glass-card p-8 py-12 rounded-[3rem] text-center flex flex-col items-center shadow-sm">
                        <div id="status-icon-2" class="w-16 h-16 rounded-3xl bg-amber-50 text-amber-600 flex items-center justify-center mb-10 transition-all duration-500">
                            <i class="fa-solid fa-microchip text-2xl"></i>
                        </div>
                        <h3 class="text-[12px] font-black text-[var(--accent)] uppercase tracking-[0.2em] mb-4">Technical Latency</h3>
                        <div id="problem-text-2" class="text-xs font-bold text-slate-900 uppercase leading-relaxed min-h-[60px] px-4">
                            $50M facility launch delay stalls client revenue-generation and eats capital investment.
                        </div>
                        <div class="progress-bar">
                            <div id="progress-2" class="progress-fill"></div>
                        </div>
                        <button onclick="handleSimulation(2)" id="sim-btn-2" data-state="initial" class="w-full py-5 bg-slate-900 text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg">
                            Resolve Issue
                        </button>
                    </div>

                    <!-- Sim 3 -->
                    <div id="sim-card-3" class="sim-card glass-card p-8 py-12 rounded-[3rem] text-center flex flex-col items-center shadow-sm">
                        <div id="status-icon-3" class="w-16 h-16 rounded-3xl bg-amber-50 text-amber-600 flex items-center justify-center mb-10 transition-all duration-500">
                            <i class="fa-solid fa-layer-group text-2xl"></i>
                        </div>
                        <h3 class="text-[12px] font-black text-[var(--accent)] uppercase tracking-[0.2em] mb-4">Resource Fragmentation</h3>
                        <div id="problem-text-3" class="text-xs font-bold text-slate-900 uppercase leading-relaxed min-h-[60px] px-4">
                            Directing 5 simultaneous $12M sites creating a "domino effect" where one crisis drains all resources.
                        </div>
                        <div class="progress-bar">
                            <div id="progress-3" class="progress-fill"></div>
                        </div>
                        <button onclick="handleSimulation(3)" id="sim-btn-3" data-state="initial" class="w-full py-5 bg-slate-900 text-white rounded-[1.25rem] font-black text-[11px] uppercase tracking-[0.2em] active:scale-95 transition-all shadow-lg">
                            Resolve Issue
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Academics -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <div class="section-header">
                    <h2 class="section-title text-[var(--accent)]">Academics</h2>
                    <div class="section-divider"></div>
                </div>

                <button id="acadBtn" onclick="toggleSection('acad')" class="nexus-btn pulse-wave">
                    <i id="acadIcon" class="fa-solid fa-graduation-cap text-4xl text-white shake-icon"></i>
                </button>

                <div id="acadContent" class="exp-container space-y-6">
                    <div class="glass-card p-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                        <i class="fa-solid fa-graduation-cap text-[var(--accent)] mb-6 text-2xl"></i>
                        <h4 class="text-2xl font-black uppercase text-slate-900 leading-tight">M.Sc Project Management</h4>
                        <p class="text-[11px] font-black text-slate-500 uppercase mt-4 tracking-[0.25em]">NTU Singapore | GPA: 4.14</p>
                    </div>
                    <div class="glass-card p-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                        <i class="fa-solid fa-user-graduate text-slate-400 mb-6 text-2xl"></i>
                        <h4 class="text-2xl font-black uppercase text-slate-900 leading-tight">B.Tech Aerospace</h4>
                        <p class="text-[11px] font-black text-slate-500 uppercase mt-4 tracking-[0.25em]">PM Institute | GPA: 4.07</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- PMP Apple Section -->
        <section class="mt-12 mb-8 w-full">
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
                            <span class="text-[10px] font-black text-[var(--accent)] uppercase tracking-[0.2em]">Credentialed</span>
                            <div class="hidden sm:block h-[1px] flex-grow bg-slate-100"></div>
                        </div>
                        <h3 class="text-xl font-black text-slate-900 uppercase leading-tight mb-2">Project Management Professional</h3>
                        <p class="text-[11px] text-slate-500 font-bold uppercase tracking-wider">Cert #4181149 • 2025–2028</p>
                    </div>

                    <a href="https://drive.google.com/file/d/1GSi6xrRhk8LBgboyArKdwgUpK0te4lGS/view?usp=sharing" target="_blank" class="w-12 h-12 rounded-full bg-slate-100 flex items-center justify-center text-slate-900 hover:bg-blue-600 hover:text-white transition-all flex-shrink-0">
                        <i class="fa-solid fa-arrow-up-right-from-square text-sm"></i>
                    </a>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="py-20 text-center w-full flex flex-col items-center">
            <div class="reveal w-full flex flex-col items-center">
                <h2 class="text-5xl font-black uppercase tracking-tighter text-slate-900 mb-16 leading-[0.9]">Ready to<br><span class="text-[var(--accent)]">Optimise?</span></h2>
                <div class="flex flex-col sm:flex-row gap-6 w-full max-w-sm">
                    <a href="mailto:sachidanandhamaditya@gmail.com" class="flex-1 py-6 bg-[var(--accent)] text-white rounded-full font-black text-[11px] uppercase tracking-[0.25em] shadow-2xl shadow-blue-500/30 active:scale-95 transition-all text-center">
                        Let's Connect
                    </a>
                    <a href="https://drive.google.com/uc?export=download&id=1ECTxz4eec13It0jeHqNBNY9TgmaTa1JP" download class="flex-1 py-6 bg-slate-900 text-white rounded-full font-black text-[11px] uppercase tracking-[0.25em] shadow-2xl shadow-slate-900/30 active:scale-95 transition-all text-center">
                        CV Download
                    </a>
                </div>
                <p class="mt-24 text-[9px] font-black text-slate-400 uppercase tracking-[0.4em]">© 2025 Aditya Sachidanandham</p>
            </div>
        </footer>
    </main>

    <script>
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

        // Scroll Reveal Observer
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('active');
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        // Parallax Blobs
        window.addEventListener('scroll', () => {
            const scroll = window.pageYOffset;
            document.getElementById('blob-1').style.transform = `translate(${scroll * 0.04}px, ${scroll * 0.04}px)`;
            document.getElementById('blob-2').style.transform = `translate(${-scroll * 0.03}px, ${-scroll * 0.01}px)`;
        });

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
                    content.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }, 500);
            } else {
                icon.className = `fa-solid ${originalIcons[type]} text-4xl text-white shake-icon`;
            }
        }

        function handleSimulation(id) {
            const btn = document.getElementById(`sim-btn-${id}`);
            const state = btn.getAttribute('data-state');
            if (state === 'initial') runSimulation(id);
            else resetSimulation(id);
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
            const interval = setInterval(() => {
                width += 2;
                progress.style.width = width + '%';
                
                if (width >= 100) {
                    clearInterval(interval);
                    btn.disabled = false;
                    btn.innerText = "RESET SIMULATOR";
                    btn.setAttribute('data-state', 'deployed');
                    btn.style.background = '#059669';
                    
                    text.innerText = solutions[id];
                    text.classList.remove('text-slate-900');
                    text.classList.add('text-emerald-700', 'font-black');
                    
                    statusIcon.className = "w-16 h-16 rounded-3xl bg-emerald-50 text-emerald-600 flex items-center justify-center mb-10 transition-all duration-500";
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
            btn.style.background = 'var(--ink)';
            
            progress.style.width = '0%';
            text.innerText = initialProblems[id].text;
            text.classList.remove('text-emerald-700', 'font-black');
            text.classList.add('text-slate-900');
            
            statusIcon.className = "w-16 h-16 rounded-3xl bg-amber-50 text-amber-600 flex items-center justify-center mb-10";
            statusIcon.innerHTML = `<i class="fa-solid ${initialProblems[id].icon} text-2xl"></i>`;
        }
    </script>
</body>
</html>
