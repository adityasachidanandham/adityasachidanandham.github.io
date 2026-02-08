<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Aditya Sachidanandham | PMP® Portfolio</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800;900&display=swap');
        
        :root {
            /* Deeper Lilac & Pearl Mix (+10% intensity) */
            --lilac: #CDB4DB;
            --deep-lilac: #7B2CBF;
            --pearl-white: #F8F7FF;
            --electric-purple: #9D4EDD; 
            --surface: rgba(245, 235, 255, 0.5);
            --text-main: #240046;
            --text-dim: #5A189A;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--pearl-white);
            color: var(--text-main);
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
            width: 100%;
            text-rendering: optimizeLegibility;
            -webkit-font-smoothing: antialiased;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        /* Intensified Mesh Gradient */
        .bg-mesh {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: -1;
            background: radial-gradient(at 0% 0%, var(--lilac) 0px, transparent 60%),
                        radial-gradient(at 100% 0%, #E0AAFF 0px, transparent 60%),
                        radial-gradient(at 100% 100%, #ffffff 0px, transparent 60%),
                        radial-gradient(at 0% 100%, #BE95C4 0px, transparent 60%);
            filter: blur(80px);
            opacity: 0.8;
        }

        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 100;
            background: rgba(248, 247, 255, 0.7);
            backdrop-filter: blur(24px);
            border-bottom: 1px solid rgba(123, 44, 191, 0.15);
            height: 72px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 24px;
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

        .hero-section {
            margin-top: 100px;
            text-align: center;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 4px;
        }

        .section-header {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            width: 100%;
            margin-bottom: 2.5rem;
        }

        .section-title {
            font-size: 1.875rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: -0.05em;
            line-height: 1.2;
            color: var(--text-main);
        }

        .section-divider {
            width: 48px;
            height: 4px;
            background-color: var(--electric-purple);
            margin-top: 0.75rem;
            border-radius: 99px;
            opacity: 0.8;
        }

        .nexus-btn {
            width: 120px; height: 120px;
            transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
            display: flex; align-items: center; justify-content: center;
            border-radius: 3.5rem; cursor: pointer; z-index: 20;
            touch-action: manipulation;
            flex-shrink: 0;
            background: rgba(255, 255, 255, 0.9);
            border: 2px solid rgba(157, 78, 221, 0.3);
            box-shadow: 0 20px 40px rgba(123, 44, 191, 0.15);
        }
        .nexus-btn.active { transform: rotate(90deg); background-color: #ef4444 !important; border-color: transparent; }

        .exp-container {
            max-height: 0; overflow: hidden;
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
            opacity: 0; width: 100%;
        }
        .exp-container.show { max-height: 4000px; opacity: 1; margin-top: 2.5rem; }

        .glass-card {
            background: var(--surface);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(123, 44, 191, 0.15);
            width: 100%;
            transition: all 0.3s ease;
        }
        .glass-card:hover {
            border-color: rgba(123, 44, 191, 0.4);
            background: rgba(245, 235, 255, 0.7);
        }

        .apple-card {
            background: var(--surface);
            backdrop-filter: blur(12px);
            border-radius: 24px;
            border: 1px solid rgba(123, 44, 191, 0.15);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .pmp-badge-container {
            background: #ffffff;
            width: 70px;
            height: 70px;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            border: 1px solid rgba(157, 78, 221, 0.3);
        }

        .pulse-wave { animation: pulse 2.5s infinite; }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(157, 78, 221, 0.3); }
            70% { box-shadow: 0 0 0 20px rgba(157, 78, 221, 0); }
            100% { box-shadow: 0 0 0 0 rgba(157, 78, 221, 0); }
        }

        .no-scrollbar::-webkit-scrollbar { display: none; }

        .sim-card {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            height: auto;
            min-height: 340px;
            display: flex;
            flex-direction: column;
            width: 100%;
        }
        .sim-card.active-solving { border-color: var(--electric-purple); background: rgba(235, 200, 255, 0.4); }
        
        @keyframes icon-shake {
            0%, 85%, 100% { transform: translateX(0); }
            87% { transform: translateX(-4px) rotate(-3deg); }
            90% { transform: translateX(4px) rotate(3deg); }
        }
        .shake-icon { animation: icon-shake 3s ease-in-out infinite; }

        .btn-primary {
            background: #3C096C;
            color: #ffffff;
            transition: all 0.3s ease;
        }
        .btn-primary:hover {
            background: var(--deep-lilac);
            transform: translateY(-1px);
        }

        .text-gradient {
            background: linear-gradient(to bottom, var(--text-main) 0%, var(--electric-purple) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .sim-btn-style {
            background-color: #3C096C;
            color: #ffffff !important;
        }
        .sim-btn-style.success {
            background-color: #10b981;
            color: #ffffff !important;
        }
    </style>
</head>
<body class="pb-40 no-scrollbar">
    <div class="bg-mesh"></div>

    <nav>
        <div class="text-[9px] font-black tracking-[0.3em] text-purple-900/40 uppercase">PMP® CERTIFIED</div>
        <div class="flex gap-2">
            <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" class="w-10 h-10 rounded-xl bg-white/80 flex items-center justify-center border border-purple-100 text-purple-700 active:scale-90 transition-transform shadow-sm">
                <i class="fa-brands fa-linkedin-in text-sm"></i>
            </a>
            <a href="https://wa.me/qr/NTQZ4PIDDIN3N1" target="_blank" class="w-10 h-10 rounded-xl bg-white/80 flex items-center justify-center border border-purple-100 text-purple-700 active:scale-90 transition-transform shadow-sm">
                <i class="fa-brands fa-whatsapp text-lg"></i>
            </a>
        </div>
    </nav>

    <main class="main-content">
        <!-- Hero Section -->
        <section class="hero-section"> 
            <div class="inline-block px-3 py-1 bg-purple-100/50 border border-purple-200 rounded-full text-[9px] font-black text-deep-lilac uppercase tracking-widest mb-4 shadow-sm">
                Project Management Professional
            </div>
            <h1 class="text-4xl sm:text-5xl font-black tracking-tighter uppercase leading-[0.95] mb-6 text-gradient">
                Aditya<br>Sachidanandham
            </h1>
            <p class="text-text-dim text-sm font-bold leading-relaxed mb-10 max-w-xs uppercase">
                3+ years delivering $50M+ automation installation projects for semiconductor leaders.
            </p>

            <div class="grid grid-cols-3 gap-3 mb-16 w-full">
                <div class="glass-card p-5 rounded-3xl flex flex-col items-center justify-center shadow-sm">
                    <i class="fa-solid fa-briefcase text-electric-purple mb-2 text-sm"></i>
                    <div class="text-xl font-black text-purple-900">$50M+</div>
                    <div class="text-[7px] font-bold text-text-dim uppercase tracking-wider">Portfolio</div>
                </div>
                <div class="glass-card p-5 rounded-3xl flex flex-col items-center justify-center shadow-sm">
                    <i class="fa-solid fa-circle-check text-electric-purple mb-2 text-sm"></i>
                    <div class="text-xl font-black text-purple-900">98%</div>
                    <div class="text-[7px] font-bold text-text-dim uppercase tracking-wider">On-Time</div>
                </div>
                <div class="glass-card p-5 rounded-3xl flex flex-col items-center justify-center shadow-sm">
                    <i class="fa-solid fa-arrow-trend-up text-electric-purple mb-2 text-sm"></i>
                    <div class="text-xl font-black text-purple-900">11%</div>
                    <div class="text-[7px] font-bold text-text-dim uppercase tracking-wider">Efficiency</div>
                </div>
            </div>
        </section>

        <!-- Experience Section -->
        <section class="pt-4 pb-12 w-full flex flex-col items-center">
            <div class="section-header">
                <h2 class="section-title">Experience</h2>
                <div class="section-divider"></div>
            </div>
            
            <button id="expBtn" onclick="toggleSection('exp')" class="nexus-btn pulse-wave">
                <i id="expIcon" class="fa-solid fa-briefcase text-4xl text-electric-purple shake-icon"></i>
            </button>

            <div id="expContent" class="exp-container space-y-6">
                <div class="glass-card p-8 rounded-[2rem] border-l-4 border-deep-lilac">
                    <div class="text-deep-lilac/70 font-black text-xs mb-3 uppercase tracking-widest">Mar 2025 — Jan 2026</div>
                    <h3 class="text-2xl font-black uppercase tracking-tight text-purple-950">Installation Manager</h3>
                    <p class="text-sm font-bold text-text-dim mb-6 uppercase">STMicroelectronics</p>
                    <p class="text-[14px] text-purple-900/80 font-bold leading-relaxed uppercase">• Led $20M automation project coordinating 100+ subcontractors.</p>
                </div>
                <div class="glass-card p-8 rounded-[2rem] border-l-4 border-purple-200">
                    <div class="text-text-dim font-black text-xs mb-3 uppercase tracking-widest">Aug 2024 — Feb 2025</div>
                    <h3 class="text-2xl font-black uppercase tracking-tight text-purple-950">Site Manager</h3>
                    <p class="text-sm font-bold text-text-dim mb-6 uppercase">Texas Instruments</p>
                    <p class="text-[14px] text-purple-900/80 font-bold leading-relaxed uppercase">• $50M On-site execution management with 31% faster resolution.</p>
                </div>
                <div class="glass-card p-8 rounded-[2rem] border-l-4 border-purple-200">
                    <div class="text-text-dim font-black text-xs mb-3 uppercase tracking-widest">Jul 2022 — Jul 2024</div>
                    <h3 class="text-2xl font-black uppercase tracking-tight text-purple-950">Engineer</h3>
                    <p class="text-sm font-bold text-text-dim mb-6 uppercase">UMC, Soitec, Siltronic</p>
                    <p class="text-[14px] text-purple-900/80 font-bold leading-relaxed uppercase">• Collaborated on 5 complex $12M+ projects leading risk mitigation.</p>
                </div>
            </div>
        </section>

        <!-- Simulator Section -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="section-header">
                <h2 class="section-title">Simulator</h2>
                <div class="section-divider"></div>
                <p class="text-[10px] font-bold text-text-dim uppercase tracking-[0.2em] mt-3">Interactive Problem Solving</p>
            </div>

            <div class="space-y-6 w-full">
                <div id="sim-card-1" class="sim-card glass-card p-6 py-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                    <div id="status-icon-1" class="w-16 h-16 rounded-full bg-white text-electric-purple flex items-center justify-center mb-8 border border-purple-100 shadow-sm">
                        <i class="fa-solid fa-users-gear text-2xl"></i>
                    </div>
                    <h3 class="text-[11px] font-black text-deep-lilac uppercase tracking-widest mb-3">Oversight Dilution</h3>
                    <div id="problem-text-1" class="text-xs font-bold text-purple-900/90 uppercase leading-relaxed min-h-[60px] px-2">
                        Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.
                    </div>
                    <div class="w-full bg-purple-200 h-1.5 rounded-full my-8 overflow-hidden">
                        <div id="progress-1" class="bg-deep-lilac h-full w-0 transition-all duration-300"></div>
                    </div>
                    <button onclick="handleSimulation(1)" id="sim-btn-1" data-state="initial" class="w-full py-4 sim-btn-style rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                        Resolve
                    </button>
                </div>

                <div id="sim-card-2" class="sim-card glass-card p-6 py-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                    <div id="status-icon-2" class="w-16 h-16 rounded-full bg-white text-electric-purple flex items-center justify-center mb-8 border border-purple-100 shadow-sm">
                        <i class="fa-solid fa-microchip text-2xl"></i>
                    </div>
                    <h3 class="text-[11px] font-black text-deep-lilac uppercase tracking-widest mb-3">Technical Latency</h3>
                    <div id="problem-text-2" class="text-xs font-bold text-purple-900/90 uppercase leading-relaxed min-h-[60px] px-2">
                        $50M facility launch delay stalls client revenue-generation and eats capital investment.
                    </div>
                    <div class="w-full bg-purple-200 h-1.5 rounded-full my-8 overflow-hidden">
                        <div id="progress-2" class="bg-deep-lilac h-full w-0 transition-all duration-300"></div>
                    </div>
                    <button onclick="handleSimulation(2)" id="sim-btn-2" data-state="initial" class="w-full py-4 sim-btn-style rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                        Resolve
                    </button>
                </div>

                <div id="sim-card-3" class="sim-card glass-card p-6 py-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                    <div id="status-icon-3" class="w-16 h-16 rounded-full bg-white text-electric-purple flex items-center justify-center mb-8 border border-purple-100 shadow-sm">
                        <i class="fa-solid fa-layer-group text-2xl"></i>
                    </div>
                    <h3 class="text-[11px] font-black text-deep-lilac uppercase tracking-widest mb-3">Resource Fragmentation</h3>
                    <div id="problem-text-3" class="text-xs font-bold text-purple-900/90 uppercase leading-relaxed min-h-[60px] px-2">
                        Directing 5 simultaneous $12M sites creating a "domino effect" where one crisis drains all resources.
                    </div>
                    <div class="w-full bg-purple-200 h-1.5 rounded-full my-8 overflow-hidden">
                        <div id="progress-3" class="bg-deep-lilac h-full w-0 transition-all duration-300"></div>
                    </div>
                    <button onclick="handleSimulation(3)" id="sim-btn-3" data-state="initial" class="w-full py-4 sim-btn-style rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                        Resolve
                    </button>
                </div>
            </div>
        </section>

        <!-- Academics Section -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="section-header">
                <h2 class="section-title">Academics</h2>
                <div class="section-divider"></div>
            </div>

            <button id="acadBtn" onclick="toggleSection('acad')" class="nexus-btn shadow-xl pulse-wave">
                <i id="acadIcon" class="fa-solid fa-graduation-cap text-4xl text-electric-purple shake-icon"></i>
            </button>

            <div id="acadContent" class="exp-container space-y-6">
                <div class="glass-card p-8 rounded-3xl text-center flex flex-col items-center shadow-sm">
                    <i class="fa-solid fa-graduation-cap text-electric-purple mb-6 text-xl"></i>
                    <h4 class="text-xl font-black uppercase text-purple-950 leading-tight">M.Sc Project Management</h4>
                    <p class="text-[10px] font-black text-text-dim uppercase mt-4 tracking-widest">NTU Singapore | GPA: 4.14</p>
                </div>
                <div class="glass-card p-8 rounded-3xl text-center flex flex-col items-center shadow-sm">
                    <i class="fa-solid fa-user-graduate text-text-dim mb-6 text-xl"></i>
                    <h4 class="text-xl font-black uppercase text-purple-950 leading-tight">B.Tech Aerospace</h4>
                    <p class="text-[10px] font-black text-text-dim uppercase mt-4 tracking-widest">PM Institute | GPA: 4.07</p>
                </div>
            </div>
        </section>

        <!-- Compact PMP Section -->
        <section class="mb-6 w-full py-2">
            <div class="apple-card w-full p-6 flex items-center gap-6 shadow-sm">
                <div class="pmp-badge-container flex-shrink-0 shadow-sm">
                    <div class="absolute inset-0 border-2 border-purple-50 rounded-2xl"></div>
                    <div class="text-center">
                        <div class="text-[8px] font-black text-electric-purple leading-none">PMP</div>
                        <i class="fa-solid fa-award text-purple-900 text-xl my-0.5"></i>
                        <div class="text-[6px] font-bold text-text-dim uppercase">Verified</div>
                    </div>
                </div>

                <div class="flex-grow">
                    <div class="flex items-center gap-2 mb-1">
                        <span class="text-[9px] font-bold text-deep-lilac uppercase tracking-widest">Credentialed</span>
                        <div class="h-px flex-grow bg-purple-200"></div>
                    </div>
                    <h3 class="text-lg font-bold text-purple-950 leading-tight">Project Management Professional</h3>
                    <p class="text-[11px] text-text-dim font-medium">Certification #4181149 • Valid until 2028</p>
                </div>

                <a href="https://drive.google.com/file/d/1GSi6xrRhk8LBgboyArKdwgUpK0te4lGS/view?usp=sharing" target="_blank" class="w-10 h-10 rounded-full bg-white border border-purple-100 flex items-center justify-center text-purple-700 hover:bg-purple-50 transition-colors flex-shrink-0 shadow-sm">
                    <i class="fa-solid fa-arrow-up-right-from-square text-xs"></i>
                </a>
            </div>
        </section>

        <!-- Footer -->
        <footer class="py-12 text-center w-full flex flex-col items-center">
            <h2 class="text-4xl font-black uppercase tracking-tighter text-purple-950 mb-12 leading-none">Ready to<br><span class="text-electric-purple">Optimise?</span></h2>
            <div class="flex gap-4 flex-wrap justify-center w-full">
                <a href="mailto:sachidanandhamaditya@gmail.com" class="flex-1 min-w-[200px] py-5 btn-primary rounded-full font-black text-[11px] uppercase tracking-[0.2em] shadow-lg active:scale-95 text-center">
                    Let's Connect
                </a>
                <a href="https://drive.google.com/uc?export=download&id=1ECTxz4eec13It0jeHqNBNY9TgmaTa1JP" download="Aditya_Sachidanandham_CV.pdf" class="flex-1 min-w-[200px] py-5 bg-white border border-purple-200 text-purple-900 rounded-full font-black text-[11px] uppercase tracking-[0.2em] shadow-lg active:scale-95 text-center">
                    CV Download
                </a>
            </div>
        </footer>
    </main>

    <script>
        const initialProblems = {
            1: { text: "Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.", icon: 'fa-users-gear' },
            2: { text: "$50M facility launch delay stalls client revenue-generation and eats capital investment.", icon: 'fa-microchip' },
            3: { text: "Directing 5 simultaneous $12M sites creating a \"domino effect\" where one crisis drains all resources.", icon: 'fa-layer-group' }
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
                icon.className = 'fa-solid fa-xmark text-4xl text-purple-900';
                setTimeout(() => {
                    content.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }, 400);
            } else {
                icon.className = `fa-solid ${originalIcons[type]} text-4xl text-electric-purple shake-icon`;
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

            const solutions = {
                1: "Integrated Critical Path Method (CPM) with client production flows, securing a 98% on-time delivery rate.",
                2: "Deployed data-driven Root Cause Analysis (RCA), cutting issue response time by 31%.",
                3: "Centralized portfolio-wide scheduling to ensure all 5 sites met integration standards without resource shortages."
            };

            card.classList.add('active-solving');
            btn.disabled = true;
            btn.innerText = "SIMULATING...";

            let width = 0;
            const interval = setInterval(() => {
                width += 5;
                progress.style.width = width + '%';
                if (width >= 100) {
                    clearInterval(interval);
                    btn.disabled = false;
                    btn.innerText = "RESET SIMULATOR";
                    btn.setAttribute('data-state', 'deployed');
                    btn.classList.add('success');
                    text.innerText = solutions[id];
                    text.className = "text-xs font-bold text-emerald-700 uppercase leading-relaxed flex items-center justify-center min-h-[80px] px-2";
                    statusIcon.className = "w-16 h-16 rounded-full bg-emerald-500/10 text-emerald-600 flex items-center justify-center mb-8 border border-emerald-500/20 transition-colors duration-500 shadow-sm";
                    statusIcon.innerHTML = '<i class="fa-solid fa-check-double text-2xl"></i>';
                }
            }, 50);
        }

        function resetSimulation(id) {
            const card = document.getElementById(`sim-card-${id}`);
            const btn = document.getElementById(`sim-btn-${id}`);
            const progress = document.getElementById(`progress-${id}`);
            const text = document.getElementById(`problem-text-${id}`);
            const statusIcon = document.getElementById(`status-icon-${id}`);

            card.classList.remove('active-solving');
            btn.innerText = "Resolve";
            btn.setAttribute('data-state', 'initial');
            btn.classList.remove('success');
            progress.style.width = '0%';
            text.innerText = initialProblems[id].text;
            text.className = "text-xs font-bold text-purple-900/90 uppercase leading-relaxed min-h-[60px] px-2";
            statusIcon.className = "w-16 h-16 rounded-full bg-white text-electric-purple flex items-center justify-center mb-8 border border-purple-100 shadow-sm";
            statusIcon.innerHTML = `<i class="fa-solid ${initialProblems[id].icon} text-2xl"></i>`;
        }
    </script>
</body>
</html>
