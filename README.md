<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Aditya Sachidanandham | PMP® Portfolio</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');
        
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #ffffff;
            color: #0f172a;
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
            width: 100%;
            text-rendering: optimizeLegibility;
            -webkit-font-smoothing: antialiased;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .main-content {
            width: 100%;
            max-width: 640px;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 0 24px;
        }

        .hero-section {
            margin-top: 76px;
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
        }

        .section-divider {
            width: 48px;
            height: 4px;
            background-color: #e2e8f0;
            margin-top: 0.5rem;
            border-radius: 99px;
        }

        .nexus-btn {
            width: 120px; height: 120px;
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: flex; align-items: center; justify-content: center;
            border-radius: 3.5rem; cursor: pointer; z-index: 20;
            touch-action: manipulation;
            flex-shrink: 0;
            box-shadow: 0 20px 25px -5px rgba(37, 99, 235, 0.1);
        }
        .nexus-btn.active { transform: rotate(90deg); background-color: #ef4444 !important; }

        .exp-container {
            max-height: 0; overflow: hidden;
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
            opacity: 0; width: 100%;
        }
        .exp-container.show { max-height: 4000px; opacity: 1; margin-top: 2.5rem; }

        .glass-card {
            background: rgba(248, 250, 252, 0.95);
            backdrop-filter: blur(12px);
            border: 1px solid #f1f5f9;
            width: 100%;
        }

        /* --- NEW STYLES FROM SOURCE --- */
        .apple-card {
            background: #fbfbfd;
            border-radius: 24px;
            border: 1px solid rgba(0,0,0,0.04);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .apple-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.04);
        }

        .pmp-badge-container {
            background: linear-gradient(135deg, #005bb7 0%, #003e8c 100%);
            width: 70px;
            height: 70px;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            box-shadow: 0 8px 16px rgba(0, 91, 183, 0.2);
        }
        /* --------------------------- */

        .pulse-wave { animation: pulse 2.5s infinite; }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0.3); }
            70% { box-shadow: 0 0 0 20px rgba(37, 99, 235, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0); }
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
        .sim-card.active-solving { border-color: #3b82f6; background: #eff6ff; }
        
        @keyframes icon-shake {
            0%, 85%, 100% { transform: translateX(0); }
            87% { transform: translateX(-4px) rotate(-3deg); }
            90% { transform: translateX(4px) rotate(3deg); }
        }
        .shake-icon { animation: icon-shake 3s ease-in-out infinite; }
    </style>
</head>
<body class="pb-40 no-scrollbar">

    <nav class="px-6 flex justify-between items-center fixed top-0 w-full z-50 bg-white border-b border-slate-100 h-[72px]">
        <div class="text-[9px] font-black tracking-[0.3em] text-blue-600 uppercase">PMP® #4181149</div>
        <div class="flex gap-2">
            <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" class="w-10 h-10 rounded-xl bg-slate-50 flex items-center justify-center border border-slate-200 text-blue-600 active:scale-90 transition-transform">
                <i class="fa-brands fa-linkedin-in text-sm"></i>
            </a>
            <a href="https://wa.me/qr/NTQZ4PIDDIN3N1" target="_blank" class="w-10 h-10 rounded-xl bg-emerald-50 flex items-center justify-center border border-emerald-100 text-emerald-600 active:scale-90 transition-transform">
                <i class="fa-brands fa-whatsapp text-lg"></i>
            </a>
        </div>
    </nav>

    <main class="main-content">
        <!-- Hero Section -->
        <section class="hero-section"> 
            <div class="inline-block px-3 py-1 bg-blue-50 border border-blue-100 rounded-full text-[9px] font-black text-blue-600 uppercase tracking-widest mb-4">
                Project Management Professional
            </div>
            <h1 class="text-4xl sm:text-5xl font-black tracking-tighter uppercase leading-[0.95] mb-6 text-slate-900">
                Aditya<br><span class="text-blue-600">Sachidanandham</span>
            </h1>
            <p class="text-slate-500 text-sm font-bold leading-relaxed mb-10 max-w-xs uppercase">
                3+ years delivering $50M+ automation installation projects for semiconductor leaders.
            </p>

            <div class="grid grid-cols-3 gap-3 mb-16 w-full">
                <div class="glass-card p-5 rounded-3xl flex flex-col items-center justify-center shadow-sm">
                    <i class="fa-solid fa-briefcase text-blue-600 mb-2 text-sm"></i>
                    <div class="text-xl font-black text-slate-900">$50M+</div>
                    <div class="text-[7px] font-bold text-slate-400 uppercase tracking-wider">Portfolio</div>
                </div>
                <div class="glass-card p-5 rounded-3xl flex flex-col items-center justify-center shadow-sm">
                    <i class="fa-solid fa-circle-check text-emerald-500 mb-2 text-sm"></i>
                    <div class="text-xl font-black text-slate-900">98%</div>
                    <div class="text-[7px] font-bold text-slate-400 uppercase tracking-wider">On-Time</div>
                </div>
                <div class="glass-card p-5 rounded-3xl flex flex-col items-center justify-center shadow-sm">
                    <i class="fa-solid fa-arrow-trend-up text-blue-600 mb-2 text-sm"></i>
                    <div class="text-xl font-black text-slate-900">11%</div>
                    <div class="text-[7px] font-bold text-slate-400 uppercase tracking-wider">Efficiency</div>
                </div>
            </div>
        </section>

        <!-- Compact PMP Apple-Style Section -->
        <section class="mb-6 w-full py-6">
            <div class="apple-card w-full p-6 flex items-center gap-6">
                <!-- Badge Icon Reverted to Professional Style -->
                <div class="pmp-badge-container flex-shrink-0">
                    <div class="absolute inset-0 border-2 border-white/20 rounded-2xl"></div>
                    <div class="text-center">
                        <div class="text-[8px] font-black text-white/90 leading-none">PMP</div>
                        <i class="fa-solid fa-award text-white text-xl my-0.5"></i>
                        <div class="text-[6px] font-bold text-white/70 uppercase">Verified</div>
                    </div>
                </div>

                <div class="flex-grow">
                    <div class="flex items-center gap-2 mb-1">
                        <span class="text-[9px] font-bold text-blue-600 uppercase tracking-widest">Credentialed</span>
                        <div class="h-px flex-grow bg-gray-100"></div>
                    </div>
                    <h3 class="text-lg font-bold text-gray-900 leading-tight">Project Management Professional</h3>
                    <p class="text-[11px] text-gray-400 font-medium">Certification #4181149 • Valid until 2028</p>
                </div>

                <a href="https://drive.google.com/file/d/1GSi6xrRhk8LBgboyArKdwgUpK0te4lGS/view?usp=sharing" target="_blank" class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center text-gray-900 hover:bg-gray-200 transition-colors flex-shrink-0">
                    <i class="fa-solid fa-arrow-up-right-from-square text-xs"></i>
                </a>
            </div>
        </section>

        <!-- Experience Section -->
        <section class="pt-4 pb-12 w-full flex flex-col items-center">
            <div class="section-header">
                <h2 class="section-title text-blue-600">Experience</h2>
                <div class="section-divider"></div>
            </div>
            
            <button id="expBtn" onclick="toggleSection('exp')" class="nexus-btn bg-blue-600 pulse-wave">
                <i id="expIcon" class="fa-solid fa-briefcase text-4xl text-white shake-icon"></i>
            </button>

            <div id="expContent" class="exp-container space-y-6">
                <div class="glass-card p-8 rounded-[2rem] border-l-4 border-blue-600">
                    <div class="text-blue-600 font-black text-xs mb-3 uppercase tracking-widest">Mar 2025 — Jan 2026</div>
                    <h3 class="text-2xl font-black uppercase tracking-tight text-slate-900">Installation Manager</h3>
                    <p class="text-sm font-bold text-slate-400 mb-6 uppercase">STMicroelectronics</p>
                    <p class="text-[14px] text-slate-600 font-bold leading-relaxed uppercase">• Led $20M automation project coordinating 100+ subcontractors.</p>
                </div>
                <div class="glass-card p-8 rounded-[2rem] border-l-4 border-slate-200">
                    <div class="text-slate-400 font-black text-xs mb-3 uppercase tracking-widest">Aug 2024 — Feb 2025</div>
                    <h3 class="text-2xl font-black uppercase tracking-tight text-slate-900">Site Manager</h3>
                    <p class="text-sm font-bold text-slate-400 mb-6 uppercase">Texas Instruments</p>
                    <p class="text-[14px] text-slate-600 font-bold leading-relaxed uppercase">• $50M On-site execution management with 31% faster resolution.</p>
                </div>
                <div class="glass-card p-8 rounded-[2rem] border-l-4 border-slate-200">
                    <div class="text-slate-400 font-black text-xs mb-3 uppercase tracking-widest">Jul 2022 — Jul 2024</div>
                    <h3 class="text-2xl font-black uppercase tracking-tight text-slate-900">Engineer</h3>
                    <p class="text-sm font-bold text-slate-400 mb-6 uppercase">UMC, Soitec, Siltronic</p>
                    <p class="text-[14px] text-slate-600 font-bold leading-relaxed uppercase">• Collaborated on 5 complex $12M+ projects leading risk mitigation.</p>
                </div>
            </div>
        </section>

        <!-- Simulator Section -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="section-header">
                <h2 class="section-title text-slate-900">Simulator</h2>
                <div class="section-divider"></div>
                <p class="text-[10px] font-bold text-slate-400 uppercase tracking-[0.2em] mt-3">Interactive Problem Solving</p>
            </div>

            <div class="space-y-6 w-full">
                <div id="sim-card-1" class="sim-card glass-card p-6 py-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                    <div id="status-icon-1" class="w-16 h-16 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-8">
                        <i class="fa-solid fa-users-gear text-2xl"></i>
                    </div>
                    <h3 class="text-[11px] font-black text-blue-600 uppercase tracking-widest mb-3">Oversight Dilution</h3>
                    <div id="problem-text-1" class="text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-2">
                        Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.
                    </div>
                    <div class="w-full bg-slate-100 h-1.5 rounded-full my-8 overflow-hidden">
                        <div id="progress-1" class="bg-blue-600 h-full w-0 transition-all duration-300"></div>
                    </div>
                    <button onclick="handleSimulation(1)" id="sim-btn-1" data-state="initial" class="w-full py-4 bg-slate-900 text-white rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                        Resolve
                    </button>
                </div>

                <div id="sim-card-2" class="sim-card glass-card p-6 py-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                    <div id="status-icon-2" class="w-16 h-16 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-8">
                        <i class="fa-solid fa-microchip text-2xl"></i>
                    </div>
                    <h3 class="text-[11px] font-black text-blue-600 uppercase tracking-widest mb-3">Technical Latency</h3>
                    <div id="problem-text-2" class="text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-2">
                        $50M facility launch delay stalls client revenue-generation and eats capital investment.
                    </div>
                    <div class="w-full bg-slate-100 h-1.5 rounded-full my-8 overflow-hidden">
                        <div id="progress-2" class="bg-blue-600 h-full w-0 transition-all duration-300"></div>
                    </div>
                    <button onclick="handleSimulation(2)" id="sim-btn-2" data-state="initial" class="w-full py-4 bg-slate-900 text-white rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                        Resolve
                    </button>
                </div>

                <div id="sim-card-3" class="sim-card glass-card p-6 py-10 rounded-[2.5rem] text-center flex flex-col items-center shadow-sm">
                    <div id="status-icon-3" class="w-16 h-16 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-8">
                        <i class="fa-solid fa-layer-group text-2xl"></i>
                    </div>
                    <h3 class="text-[11px] font-black text-blue-600 uppercase tracking-widest mb-3">Resource Fragmentation</h3>
                    <div id="problem-text-3" class="text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-2">
                        Directing 5 simultaneous $12M sites creating a "domino effect" where one crisis drains all resources.
                    </div>
                    <div class="w-full bg-slate-100 h-1.5 rounded-full my-8 overflow-hidden">
                        <div id="progress-3" class="bg-blue-600 h-full w-0 transition-all duration-300"></div>
                    </div>
                    <button onclick="handleSimulation(3)" id="sim-btn-3" data-state="initial" class="w-full py-4 bg-slate-900 text-white rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                        Resolve
                    </button>
                </div>
            </div>
        </section>

        <!-- Academics Section -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="section-header">
                <h2 class="section-title text-blue-600">Academics</h2>
                <div class="section-divider"></div>
            </div>

            <button id="acadBtn" onclick="toggleSection('acad')" class="nexus-btn bg-slate-900 shadow-xl pulse-wave">
                <i id="acadIcon" class="fa-solid fa-graduation-cap text-4xl text-white shake-icon"></i>
            </button>

            <div id="acadContent" class="exp-container space-y-6">
                <div class="glass-card p-8 rounded-3xl text-center flex flex-col items-center shadow-sm">
                    <i class="fa-solid fa-graduation-cap text-blue-600 mb-6 text-xl"></i>
                    <h4 class="text-xl font-black uppercase text-slate-900 leading-tight">M.Sc Project Management</h4>
                    <p class="text-[10px] font-black text-slate-400 uppercase mt-4 tracking-widest">NTU Singapore | GPA: 4.14</p>
                </div>
                <div class="glass-card p-8 rounded-3xl text-center flex flex-col items-center shadow-sm">
                    <i class="fa-solid fa-user-graduate text-slate-400 mb-6 text-xl"></i>
                    <h4 class="text-xl font-black uppercase text-slate-900 leading-tight">B.Tech Aerospace</h4>
                    <p class="text-[10px] font-black text-slate-400 uppercase mt-4 tracking-widest">PM Institute | GPA: 4.07</p>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="py-24 text-center w-full flex flex-col items-center">
            <h2 class="text-4xl font-black uppercase tracking-tighter text-slate-900 mb-12 leading-none">Ready to<br><span class="text-blue-600">Optimise?</span></h2>
            <a href="mailto:sachidanandhamaditya@gmail.com" class="px-12 py-5 bg-blue-600 text-white rounded-full font-black text-[11px] uppercase tracking-[0.2em] shadow-xl active:scale-95 transition-all cursor-pointer">
                Let's Connect
            </a>
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
                icon.className = 'fa-solid fa-xmark text-4xl text-white';
                setTimeout(() => {
                    content.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }, 400);
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
                    btn.className = "w-full py-4 bg-emerald-500 text-white rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all";
                    text.innerText = solutions[id];
                    text.className = "text-xs font-bold text-emerald-600 uppercase leading-relaxed flex items-center justify-center min-h-[80px] px-2";
                    statusIcon.className = "w-16 h-16 rounded-full bg-emerald-50 text-emerald-500 flex items-center justify-center mb-8 transition-colors duration-500";
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
            btn.className = "w-full py-4 bg-slate-900 text-white rounded-2xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all";
            progress.style.width = '0%';
            text.innerText = initialProblems[id].text;
            text.className = "text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px] px-2";
            statusIcon.className = "w-16 h-16 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-8";
            statusIcon.innerHTML = `<i class="fa-solid ${initialProblems[id].icon} text-2xl"></i>`;
        }
    </script>
</body>
</html>
