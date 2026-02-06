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
       }

       :root { --nav-height: 72px; }

       .nexus-btn {
           width: 112px; height: 96px;
           transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
           display: flex; align-items: center; justify-content: center;
           border-radius: 2.5rem; cursor: pointer; z-index: 20;
           touch-action: manipulation;
       }
       .nexus-btn.active { transform: rotate(90deg); background-color: #ef4444 !important; }

       .exp-container {
           max-height: 0; overflow: hidden;
           transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
           opacity: 0; width: 100%;
       }
       .exp-container.show { max-height: 4000px; opacity: 1; margin-top: 1.5rem; }

       .glass-card {
           background: rgba(248, 250, 252, 0.95);
           backdrop-filter: blur(12px);
           border: 1px solid #f1f5f9;
       }

       .pulse-wave { animation: pulse 2s infinite; }
       @keyframes pulse {
           0% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0.4); }
           70% { box-shadow: 0 0 0 15px rgba(37, 99, 235, 0); }
           100% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0); }
       }

       .no-scrollbar::-webkit-scrollbar { display: none; }

       .sim-card {
           transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
           height: auto;
           min-height: 480px;
           display: flex;
           flex-direction: column;
       }
       .sim-card.active-solving { border-color: #3b82f6; background: #eff6ff; }
       .problem-content { flex-grow: 1; display: flex; flex-direction: column; justify-content: center; }

       @keyframes icon-shake {
           0%, 85%, 100% { transform: translateX(0); }
           87% { transform: translateX(-4px) rotate(-3deg); }
           90% { transform: translateX(4px) rotate(3deg); }
       }
       .shake-icon { animation: icon-shake 3s ease-in-out infinite; }
       
       button, a { touch-action: manipulation; }
   </style>
</head>
<body class="pb-40 no-scrollbar">

   <!-- Header Navigation -->
   <nav class="px-4 py-4 md:px-6 flex justify-between items-center fixed top-0 w-full z-50 bg-white/90 backdrop-blur-md border-b border-slate-100 h-[72px]">
       <div class="text-[9px] font-black tracking-[0.3em] text-blue-600 uppercase">PMP® CERTIFIED</div>
       <div class="flex gap-2 md:gap-3">
           <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" class="w-10 h-10 rounded-xl bg-slate-50 flex items-center justify-center border border-slate-200 text-blue-600 active:scale-90 transition-transform">
               <i class="fa-brands fa-linkedin-in text-sm"></i>
           </a>
           <a href="https://wa.me/qr/NTQZ4PIDDIN3N1" target="_blank" class="w-10 h-10 rounded-xl bg-emerald-50 flex items-center justify-center border border-emerald-100 text-emerald-600 active:scale-90 transition-transform">
               <i class="fa-brands fa-whatsapp text-lg"></i>
           </a>
       </div>
   </nav>

   <!-- Hero Section -->
   <section class="mt-[84px] px-6 text-center">
       <div class="inline-block px-3 py-1 bg-blue-50 border border-blue-100 rounded-full text-[9px] font-black text-blue-600 uppercase tracking-widest mb-3">
           Project Management Professional
       </div>
       <h1 class="text-4xl sm:text-5xl font-black tracking-tighter uppercase leading-[0.9] mb-5 text-slate-900 mt-0">
           Aditya<br><span class="text-blue-600">Sachidanandham</span>
       </h1>
       <p class="text-slate-500 text-sm font-bold leading-relaxed mb-8 max-w-xs mx-auto uppercase">
           3+ years delivering $50M+ automation installation projects for semiconductor leaders.
       </p>

       <!-- Skill Radar -->
       <div class="glass-card p-4 py-8 rounded-[2.5rem] mb-10 max-w-sm mx-auto overflow-visible shadow-sm">
           <div class="text-[10px] font-black text-blue-600 uppercase tracking-[0.2em] mb-8 text-center">Core Competencies</div>
           <div class="w-full max-w-[320px] mx-auto min-h-[260px] overflow-visible flex items-center justify-center">
               <svg viewBox="-40 -30 280 260" class="w-full h-auto max-h-[260px] overflow-visible">
                   <circle cx="100" cy="100" r="80" fill="none" stroke="#e2e8f0" stroke-dasharray="2,2" />
                   <circle cx="100" cy="100" r="50" fill="none" stroke="#e2e8f0" stroke-dasharray="2,2" />
                   <text x="100" y="-15" text-anchor="middle" class="text-[11px] font-black fill-blue-600 uppercase">CPM Scheduling</text>
                   <text x="100" y="215" text-anchor="middle" class="text-[12px] font-black fill-slate-500 uppercase">Root Cause (RCA)</text>
                   <text x="215" y="104" text-anchor="end" class="text-[10px] font-black fill-slate-500 uppercase">ROI Optimization</text>
                   <text x="-15" y="104" text-anchor="start" class="text-[10px] font-black fill-slate-500 uppercase">Risk Mitigation</text>
                   <polygon points="100,20 175,100 100,165 35,100" fill="rgba(37, 99, 235, 0.2)" stroke="#2563eb" stroke-width="2.5" />
                   <circle cx="100" cy="20" r="4" fill="#2563eb" />
                   <circle cx="175" cy="100" r="4" fill="#2563eb" />
                   <circle cx="100" cy="165" r="4" fill="#2563eb" />
                   <circle cx="35" cy="100" r="4" fill="#2563eb" />
               </svg>
           </div>
       </div>

       <!-- Metrics -->
       <div class="grid grid-cols-3 gap-2 mb-10">
           <div class="glass-card p-4 rounded-2xl flex flex-col items-center justify-center">
               <i class="fa-solid fa-briefcase text-blue-600 mb-2 text-sm"></i>
               <div class="text-lg sm:text-xl font-black text-slate-900">$50M+</div>
               <div class="text-[7px] font-bold text-slate-400 uppercase">Portfolio</div>
           </div>
           <div class="glass-card p-4 rounded-2xl flex flex-col items-center justify-center">
               <i class="fa-solid fa-circle-check text-emerald-500 mb-2 text-sm"></i>
               <div class="text-lg sm:text-xl font-black text-slate-900">98%</div>
               <div class="text-[7px] font-bold text-slate-400 uppercase">On-Time</div>
           </div>
           <div class="glass-card p-4 rounded-2xl flex flex-col items-center justify-center">
               <i class="fa-solid fa-arrow-trend-up text-blue-600 mb-2 text-sm"></i>
               <div class="text-lg sm:text-xl font-black text-slate-900">11%</div>
               <div class="text-[7px] font-bold text-slate-400 uppercase">Efficiency</div>
           </div>
       </div>
   </section>

   <!-- Experience -->
   <section class="px-6 py-4 flex flex-col items-center">
       <h2 class="text-3xl font-black text-blue-600 uppercase tracking-tighter mb-4 text-center">Experience</h2>
       <button id="expBtn" onclick="toggleSection('exp')" class="nexus-btn bg-blue-600 shadow-xl shadow-blue-200 pulse-wave mb-1">
           <i id="expIcon" class="fa-solid fa-briefcase text-3xl text-white shake-icon"></i>
       </button>

       <div id="expContent" class="exp-container space-y-6">
           <div class="glass-card p-8 rounded-[2rem] border-l-4 border-blue-600 mt-2">
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

   <!-- Simulator -->
   <section class="px-6 py-8">
       <div class="text-center mb-8">
           <h2 class="text-3xl font-black text-slate-800 uppercase tracking-tighter">Simulator</h2>
           <p class="text-[10px] font-bold text-slate-400 uppercase tracking-[0.2em] mt-2">Interactive Problem Solving</p>
       </div>

       <div class="space-y-6 max-w-lg mx-auto">
           <div id="sim-card-1" class="sim-card glass-card p-8 rounded-[2.5rem] text-center">
               <div class="problem-content">
                   <div id="status-icon-1" class="w-14 h-14 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-6 mx-auto">
                       <i class="fa-solid fa-users-gear text-xl"></i>
                   </div>
                   <h3 class="text-[10px] font-black text-blue-600 uppercase tracking-widest mb-3">Oversight Dilution</h3>
                   <div id="problem-text-1" class="text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px]">
                       Managing $20M installation with 1:12 manager-to-labor ratio (100+ personnel) causing communication lag.
                   </div>
               </div>
               <div class="mt-6">
                   <div class="w-full bg-slate-100 h-1.5 rounded-full mb-6 overflow-hidden">
                       <div id="progress-1" class="bg-blue-600 h-full w-0 transition-all duration-300"></div>
                   </div>
                   <button onclick="handleSimulation(1)" id="sim-btn-1" data-state="initial" class="w-full py-4 bg-slate-900 text-white rounded-xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                       Resolve
                   </button>
               </div>
           </div>

           <div id="sim-card-2" class="sim-card glass-card p-8 rounded-[2.5rem] text-center">
               <div class="problem-content">
                   <div id="status-icon-2" class="w-14 h-14 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-6 mx-auto">
                       <i class="fa-solid fa-microchip text-xl"></i>
                   </div>
                   <h3 class="text-[10px] font-black text-blue-600 uppercase tracking-widest mb-3">Technical Latency</h3>
                   <div id="problem-text-2" class="text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px]">
                       $50M facility launch delay stalls client revenue-generation and eats capital investment.
                   </div>
               </div>
               <div class="mt-6">
                   <div class="w-full bg-slate-100 h-1.5 rounded-full mb-6 overflow-hidden">
                       <div id="progress-2" class="bg-blue-600 h-full w-0 transition-all duration-300"></div>
                   </div>
                   <button onclick="handleSimulation(2)" id="sim-btn-2" data-state="initial" class="w-full py-4 bg-slate-900 text-white rounded-xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                       Resolve
                   </button>
               </div>
           </div>

           <div id="sim-card-3" class="sim-card glass-card p-8 rounded-[2.5rem] text-center">
               <div class="problem-content">
                   <div id="status-icon-3" class="w-14 h-14 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-6 mx-auto">
                       <i class="fa-solid fa-layer-group text-xl"></i>
                   </div>
                   <h3 class="text-[10px] font-black text-blue-600 uppercase tracking-widest mb-3">Resource Fragmentation</h3>
                   <div id="problem-text-3" class="text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px]">
                       Directing 5 simultaneous $12M sites creating a "domino effect" where one crisis drains all resources.
                   </div>
               </div>
               <div class="mt-6">
                   <div class="w-full bg-slate-100 h-1.5 rounded-full mb-6 overflow-hidden">
                       <div id="progress-3" class="bg-blue-600 h-full w-0 transition-all duration-300"></div>
                   </div>
                   <button onclick="handleSimulation(3)" id="sim-btn-3" data-state="initial" class="w-full py-4 bg-slate-900 text-white rounded-xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all">
                       Resolve
                   </button>
               </div>
           </div>
       </div>
   </section>

   <!-- Academics -->
   <section class="px-6 py-4 flex flex-col items-center">
       <h2 class="text-3xl font-black text-blue-600 uppercase tracking-tighter mb-4 text-center">Academics</h2>
       <button id="acadBtn" onclick="toggleSection('acad')" class="nexus-btn bg-slate-900 shadow-xl pulse-wave mb-1">
           <i id="acadIcon" class="fa-solid fa-graduation-cap text-3xl text-white shake-icon"></i>
       </button>

       <div id="acadContent" class="exp-container space-y-6">
           <div class="glass-card p-8 rounded-3xl text-center mt-2">
               <i class="fa-solid fa-graduation-cap text-blue-600 mb-6 text-xl"></i>
               <h4 class="text-xl font-black uppercase text-slate-900 leading-tight">M.Sc Project Management</h4>
               <p class="text-[10px] font-black text-slate-400 uppercase mt-4 tracking-widest">NTU Singapore | GPA: 4.14</p>
           </div>
           <div class="glass-card p-8 rounded-3xl text-center">
               <i class="fa-solid fa-user-graduate text-slate-400 mb-6 text-xl"></i>
               <h4 class="text-xl font-black uppercase text-slate-900 leading-tight">B.Tech Aerospace</h4>
               <p class="text-[10px] font-black text-slate-400 uppercase mt-4 tracking-widest">PM Institute | GPA: 4.07</p>
           </div>
       </div>
   </section>

   <!-- Footer -->
   <footer class="px-6 py-20 text-center">
       <h2 class="text-4xl font-black uppercase tracking-tighter text-slate-900 mb-10 leading-none">Ready to<br><span class="text-blue-600">Optimise?</span></h2>
       <div class="flex justify-center">
           <a href="mailto:sachidanandhamaditya@gmail.com" class="px-12 py-4 bg-blue-600 text-white rounded-full font-black text-[10px] uppercase tracking-[0.2em] shadow-lg active:scale-95 transition-all cursor-pointer inline-block">
               Let's Connect
           </a>
       </div>
   </footer>

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
               icon.className = 'fa-solid fa-xmark text-3xl text-white';
               setTimeout(() => {
                   content.scrollIntoView({ behavior: 'smooth', block: 'start' });
               }, 400);
           } else {
               icon.className = `fa-solid ${originalIcons[type]} text-3xl text-white shake-icon`;
           }
       }

       function handleSimulation(id) {
           const btn = document.getElementById(`sim-btn-${id}`);
           const state = btn.getAttribute('data-state');

           if (state === 'initial') {
               runSimulation(id);
           } else if (state === 'deployed') {
               resetSimulation(id);
           }
       }

       function runSimulation(id) {
           const card = document.getElementById(`sim-card-${id}`);
           const btn = document.getElementById(`sim-btn-${id}`);
           const progress = document.getElementById(`progress-${id}`);
           const text = document.getElementById(`problem-text-${id}`);
           const statusIcon = document.getElementById(`status-icon-${id}`);

           const solutions = {
               1: "Integrated Critical Path Method (CPM) with client production flows, securing a 98% on-time delivery rate and an 11% efficiency gain.",
               2: "Deployed data-driven Root Cause Analysis (RCA), cutting issue response time by 31% and schedule delays by 21%.",
               3: "Centralized portfolio-wide scheduling and risk identification to ensure all 5 sites met integration standards without resource shortages."
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
                   btn.className = "w-full py-4 bg-emerald-500 text-white rounded-xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all";
                   text.innerText = solutions[id];
                   text.className = "text-xs font-bold text-emerald-600 uppercase leading-relaxed flex items-center justify-center min-h-[80px]";
                   statusIcon.className = "w-14 h-14 rounded-full bg-emerald-50 text-emerald-500 flex items-center justify-center mb-6 mx-auto transition-colors duration-500";
                   statusIcon.innerHTML = '<i class="fa-solid fa-check-double text-xl"></i>';
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
           btn.className = "w-full py-4 bg-slate-900 text-white rounded-xl font-black text-[10px] uppercase tracking-widest active:scale-95 transition-all";
           
           progress.style.width = '0%';
           
           text.innerText = initialProblems[id].text;
           text.className = "text-xs font-bold text-slate-800 uppercase leading-relaxed min-h-[60px]";
           
           statusIcon.className = "w-14 h-14 rounded-full bg-amber-50 text-amber-500 flex items-center justify-center mb-6 mx-auto";
           statusIcon.innerHTML = `<i class="fa-solid ${initialProblems[id].icon} text-xl"></i>`;
       }
   </script>
</body>
</html>
