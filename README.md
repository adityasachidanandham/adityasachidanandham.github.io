<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
    <title>Aditya Sachidanandham | PMP® Portfolio</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap');
        
        :root {
            --eclipse-1: #272757; 
            --eclipse-2: #8686AC; 
            --eclipse-3: #505081; 
            --eclipse-4: #0F0E47; 
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #ffffff;
            color: var(--eclipse-4);
            -webkit-tap-highlight-color: transparent;
            overflow-x: hidden;
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* 5. Scroll Reveal Animation optimized for iPhone */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s cubic-bezier(0.2, 1, 0.3, 1);
            will-change: transform, opacity;
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        .blob {
            position: fixed;
            background: var(--eclipse-2);
            filter: blur(120px);
            border-radius: 50%;
            z-index: -1;
            opacity: 0.1;
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

        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 100;
            background-color: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            height: 72px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 24px;
        }

        .hero-section {
            margin-top: 100px;
            text-align: center;
            width: 100%;
        }

        /* 3. Vertical Space exactly 1mm (~3.8px) */
        .pmp-tag {
            display: inline-flex;
            padding: 1mm 1.5rem; 
            background: rgba(134, 134, 172, 0.1);
            border: 1px solid rgba(134, 134, 172, 0.2);
            border-radius: 99px;
            font-size: 10px;
            font-weight: 900;
            color: var(--eclipse-1);
            text-transform: uppercase;
            letter-spacing: 0.15em;
            margin-bottom: 2rem;
        }

        /* 2. Bolder Name (900 weight) */
        .hero-name {
            font-size: 3.5rem;
            font-weight: 900;
            letter-spacing: -0.06em;
            line-height: 0.85;
            text-transform: uppercase;
            margin-bottom: 2rem;
            color: var(--eclipse-4);
        }

        .section-header {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 2rem;
        }

        .section-title {
            font-size: 1.75rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: -0.05em;
        }

        .section-divider {
            width: 40px;
            height: 4px;
            background-color: var(--eclipse-2);
            margin-top: 0.75rem;
            border-radius: 99px;
            opacity: 0.3;
        }

        .nexus-btn {
            width: 110px; height: 110px;
            transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            display: flex; align-items: center; justify-content: center;
            border-radius: 3rem; cursor: pointer;
            box-shadow: 0 20px 40px rgba(39, 39, 87, 0.2);
            border: none;
            outline: none;
        }
        .nexus-btn:active { transform: scale(0.9); }
        .nexus-btn.active { transform: rotate(90deg); background-color: #ef4444 !important; }

        .exp-container {
            max-height: 0; 
            overflow: hidden;
            transition: all 0.6s ease;
            opacity: 0; 
            width: 100%;
        }
        .exp-container.show { 
            max-height: 2500px; 
            opacity: 1; 
            margin-top: 2rem; 
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(0, 0, 0, 0.03);
            width: 100%;
        }

        .sim-card {
            transition: all 0.4s ease;
            width: 100%;
            border: 1px solid #f1f5f9;
        }
        
        /* 4. Texts under simulators larger by 30% (approx 16px) */
        .sim-problem-text {
            font-size: 16px;
            font-weight: 700;
            color: #1e293b;
            text-transform: uppercase;
            line-height: 1.5;
            min-height: 100px;
            padding: 0 1rem;
        }

        .progress-bar {
            height: 6px;
            background: #f1f5f9;
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

        .pulse-wave { animation: pulse 2s infinite; }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(39, 39, 87, 0.4); }
            70% { box-shadow: 0 0 0 20px rgba(39, 39, 87, 0); }
            100% { box-shadow: 0 0 0 0 rgba(39, 39, 87, 0); }
        }

        .apple-card {
            background: #fbfbfd;
            border-radius: 28px;
            border: 1px solid rgba(0,0,0,0.04);
            transition: all 0.4s ease;
        }

        .pmp-badge-container {
            background: linear-gradient(135deg, var(--eclipse-1) 0%, var(--eclipse-4) 100%);
            width: 70px;
            height: 70px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 10px 20px rgba(39, 39, 87, 0.2);
        }

        /* Fix for 1. top left text artifact */
        #nav-indicator { display: none; }
    </style>
</head>
<body class="pb-24">

    <div class="blob" style="width: 400px; height: 400px; top: -100px; right: -100px;"></div>
    <div class="blob" style="width: 300px; height: 300px; bottom: 10%; left: -100px;"></div>

    <nav>
        <div class="text-[10px] font-black tracking-[0.3em] text-[var(--eclipse-1)]">PMP® CERTIFIED</div>
        <div class="flex gap-3">
            <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" onclick="triggerHaptic(10)" class="w-11 h-11 rounded-2xl bg-white flex items-center justify-center border border-slate-200 text-[var(--eclipse-1)] shadow-sm"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="https://wa.me/qr/NTQZ4PIDDIN3N1" target="_blank" onclick="triggerHaptic(10)" class="w-11 h-11 rounded-2xl bg-white flex items-center justify-center border border-emerald-100 text-emerald-600 shadow-sm"><i class="fa-brands fa-whatsapp text-xl"></i></a>
        </div>
    </nav>

    <main class="main-content">
        <!-- Hero -->
        <section class="hero-section"> 
            <div class="reveal">
                <div class="pmp-tag">Project Management Professional</div>
                <h1 class="hero-name">
                    Aditya<br><span class="text-[var(--eclipse-1)]">Sachidanandham</span>
                </h1>
                <p class="text-[var(--eclipse-3)] text-[14px] font-bold leading-relaxed mb-12 max-w-sm mx-auto">
                    Delivering $50M+ semiconductor automation projects with flawless execution and measurable impact.
                </p>

                <div class="grid grid-cols-3 gap-4 mb-16">
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center">
                        <i class="fa-solid fa-briefcase text-[var(--eclipse-1)] mb-2"></i>
                        <div class="text-2xl font-black">$50M+</div>
                        <div class="text-[8px] font-black opacity-40 uppercase mt-1">Portfolio</div>
                    </div>
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center">
                        <i class="fa-solid fa-circle-check text-[var(--eclipse-4)] mb-2"></i>
                        <div class="text-2xl font-black">98%</div>
                        <div class="text-[8px] font-black opacity-40 uppercase mt-1">On-Time</div>
                    </div>
                    <div class="glass-card p-6 rounded-[2rem] flex flex-col items-center">
                        <i class="fa-solid fa-arrow-trend-up text-[var(--eclipse-1)] mb-2"></i>
                        <div class="text-2xl font-black">11%</div>
                        <div class="text-[8px] font-black opacity-40 uppercase mt-1">Efficiency</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="reveal flex flex-col items-center w-full">
                <div class="section-header">
                    <h2 class="section-title text-[var(--eclipse-1)]">Experience</h2>
                    <div class="section-divider"></div>
                </div>
                
                <!-- 6. Added Haptics to Button -->
                <button id="expBtn" onclick="triggerHaptic(20); toggleSection('exp')" class="nexus-btn bg-[var(--eclipse-1)] pulse-wave">
                    <i id="expIcon" class="fa-solid fa-briefcase text-4xl text-white"></i>
                </button>

                <div id="expContent" class="exp-container space-y-4">
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-[var(--eclipse-1)]">
                        <div class="text-[var(--eclipse-1)] font-black text-[10px] mb-2 uppercase">Mar 2025 — Jan 2026</div>
                        <h3 class="text-xl font-black uppercase text-[var(--eclipse-4)]">Installation Manager</h3>
                        <p class="text-[10px] font-bold text-[var(--eclipse-2)] mb-4 uppercase">STMicroelectronics</p>
                        <p class="text-[13px] text-[var(--eclipse-3)] font-bold uppercase leading-relaxed">• Led $20M automation project coordinating 100+ subcontractors.</p>
                    </div>
                    <div class="glass-card p-8 rounded-[2.5rem] border-l-4 border-slate-200">
                        <div class="text-slate-400 font-black text-[10px] mb-2 uppercase">Aug 2024 — Feb 2025</div>
                        <h3 class="text-xl font-black uppercase text-[var(--eclipse-4)]">Site Manager</h3>
                        <p class="text-[10px] font-bold text-slate-400 mb-4 uppercase">Texas Instruments</p>
                        <p class="text-[13px] text-slate-600 font-bold uppercase leading-relaxed">• $50M On-site execution management with 31% faster resolution.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Simulator -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="reveal flex flex-col items-center w-full">
                <div class="section-header">
                    <h2 class="section-title text-[var(--eclipse-4)]">The Simulator</h2>
                    <div class="section-divider"></div>
                </div>

                <div class="space-y-6 w-full">
                    <!-- Case 1 -->
                    <div id="sim-card-1" class="sim-card glass-card p-10 rounded-[3rem] text-center flex flex-col items-center">
                        <div id="status-icon-1" class="w-16 h-16 rounded-3xl bg-slate-50 text-[var(--eclipse-1)] flex items-center justify-center mb-8">
                            <i class="fa-solid fa-users-gear text-2xl"></i>
                        </div>
                        <h3 class="text-[11px] font-black text-[var(--eclipse-2)] uppercase tracking-widest mb-4">Oversight Dilution</h3>
                        <div id="problem-text-1" class="sim-problem-text">
                            Managing $20M installation with 1:12 manager-to-labor ratio causing communication lag.
                        </div>
                        <div class="progress-bar"><div id="progress-1" class="progress-fill"></div></div>
                        <button onclick="triggerHaptic(20); runSimulation(1, 'Integrated Critical Path Method (CPM) with client flows, securing 98% on-time delivery.')" id="sim-btn-1" class="w-full py-5 bg-[var(--eclipse-4)] text-white rounded-2xl font-black text-[11px] uppercase tracking-widest active:scale-95 transition-all">
                            Resolve Issue
                        </button>
                    </div>

                    <!-- Case 2 -->
                    <div id="sim-card-2" class="sim-card glass-card p-10 rounded-[3rem] text-center flex flex-col items-center">
                        <div id="status-icon-2" class="w-16 h-16 rounded-3xl bg-slate-50 text-[var(--eclipse-1)] flex items-center justify-center mb-8">
                            <i class="fa-solid fa-clock-rotate-left text-2xl"></i>
                        </div>
                        <h3 class="text-[11px] font-black text-[var(--eclipse-2)] uppercase tracking-widest mb-4">Baseline Drift</h3>
                        <div id="problem-text-2" class="sim-problem-text">
                            Scope creep from client design changes delaying cleanroom tool integration by 3 weeks.
                        </div>
                        <div class="progress-bar"><div id="progress-2" class="progress-fill"></div></div>
                        <button onclick="triggerHaptic(20); runSimulation(2, 'Executed change control protocols and optimized buffer activities to reclaim 14 days of lost schedule.')" id="sim-btn-2" class="w-full py-5 bg-[var(--eclipse-4)] text-white rounded-2xl font-black text-[11px] uppercase tracking-widest active:scale-95 transition-all">
                            Resolve Issue
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Academics -->
        <section class="py-12 w-full flex flex-col items-center">
            <div class="reveal flex flex-col items-center w-full">
                <div class="section-header">
                    <h2 class="section-title text-[var(--eclipse-1)]">Academics</h2>
                    <div class="section-divider"></div>
                </div>

                <button id="acadBtn" onclick="triggerHaptic(20); toggleSection('acad')" class="nexus-btn bg-[var(--eclipse-4)] pulse-wave">
                    <i id="acadIcon" class="fa-solid fa-graduation-cap text-4xl text-white"></i>
                </button>

                <div id="acadContent" class="exp-container space-y-4">
                    <div class="glass-card p-10 rounded-[2.5rem] text-center">
                        <h4 class="text-xl font-black uppercase text-[var(--eclipse-4)]">M.Sc Project Management</h4>
                        <p class="text-[10px] font-black text-[var(--eclipse-2)] uppercase mt-2">NTU Singapore | GPA: 4.14</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- PMP Credential -->
        <section class="mt-12 mb-8 w-full">
            <div class="reveal">
                <div class="apple-card w-full p-8 flex flex-col sm:flex-row items-center gap-6">
                    <div class="pmp-badge-container">
                        <i class="fa-solid fa-award text-white text-3xl"></i>
                    </div>
                    <div class="flex-grow text-center sm:text-left">
                        <h3 class="text-xl font-black text-[var(--eclipse-4)] uppercase">PMP® Certified</h3>
                        <p class="text-[11px] text-[var(--eclipse-2)] font-bold uppercase">Cert #4181149 • 2025–2028</p>
                    </div>
                    <a href="https://drive.google.com/file/d/1GSi6xrRhk8LBgboyArKdwgUpK0te4lGS/view?usp=sharing" target="_blank" onclick="triggerHaptic(15)" class="w-12 h-12 rounded-full bg-slate-100 flex items-center justify-center text-[var(--eclipse-4)] hover:bg-[var(--eclipse-1)] hover:text-white transition-all">
                        <i class="fa-solid fa-arrow-up-right-from-square"></i>
                    </a>
                </div>
            </div>
        </section>

        <footer class="py-20 text-center w-full flex flex-col items-center">
            <div class="reveal flex flex-col items-center w-full">
                <h2 class="text-4xl font-black uppercase text-[var(--eclipse-4)] mb-12">Ready to<br><span class="text-[var(--eclipse-1)]">Optimise?</span></h2>
                <div class="flex flex-col gap-4 w-full max-w-xs">
                    <a href="mailto:sachidanandhamaditya@gmail.com" onclick="triggerHaptic(30)" class="py-6 bg-[var(--eclipse-1)] text-white rounded-full font-black text-[11px] uppercase tracking-widest text-center">Connect Now</a>
                    <a href="https://drive.google.com/uc?export=download&id=1ECTxz4eec13It0jeHqNBNY9TgmaTa1JP" onclick="triggerHaptic(30)" class="py-6 bg-[var(--eclipse-4)] text-white rounded-full font-black text-[11px] uppercase tracking-widest text-center">Download CV</a>
                </div>
                <p class="mt-20 text-[9px] font-black text-slate-300 uppercase tracking-[0.4em]">© 2025 Aditya Sachidanandham</p>
            </div>
        </footer>
    </main>

    <script>
        // 6. Haptic Feedback (Vibration API)
        function triggerHaptic(strength = 15) {
            if (window.navigator && window.navigator.vibrate) {
                window.navigator.vibrate(strength);
            }
        }

        // 5. Scroll Reveal with iPhone optimization
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        // UI Logic
        function toggleSection(type) {
            const btn = document.getElementById(type + 'Btn');
            const icon = document.getElementById(type + 'Icon');
            const content = document.getElementById(type + 'Content');
            const isOpen = content.classList.contains('show');
            
            btn.classList.toggle('active');
            content.classList.toggle('show');
            
            if (!isOpen) {
                icon.className = 'fa-solid fa-xmark text-4xl text-white';
                setTimeout(() => content.scrollIntoView({ behavior: 'smooth', block: 'nearest' }), 300);
            } else {
                const original = type === 'exp' ? 'fa-briefcase' : 'fa-graduation-cap';
                icon.className = `fa-solid ${original} text-4xl text-white`;
            }
        }

        // Simulator Logic
        function runSimulation(id, solutionText) {
            const btn = document.getElementById(`sim-btn-${id}`);
            const progress = document.getElementById(`progress-${id}`);
            const text = document.getElementById(`problem-text-${id}`);
            const statusIcon = document.getElementById(`status-icon-${id}`);

            if(btn.innerText === "RESET SIMULATOR") {
                location.reload();
                return;
            }

            btn.disabled = true;
            btn.innerText = "SIMULATING...";
            
            let width = 0;
            const interval = setInterval(() => {
                width += 1.5;
                progress.style.width = width + '%';
                if(Math.floor(width) % 15 === 0) triggerHaptic(5);

                if (width >= 100) {
                    clearInterval(interval);
                    triggerHaptic(40);
                    btn.disabled = false;
                    btn.innerText = "RESET SIMULATOR";
                    btn.style.backgroundColor = "#10b981";
                    text.innerText = solutionText;
                    text.style.color = "#10b981";
                    statusIcon.innerHTML = '<i class="fa-solid fa-check-double text-2xl text-emerald-500"></i>';
                }
            }, 30);
        }
    </script>
</body>
</html>
