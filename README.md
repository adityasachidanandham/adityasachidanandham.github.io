<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
   <title>Aditya Sachidanandham | PMP®</title>
   <script src="https://cdn.tailwindcss.com"></script>
   <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
   <style>
       @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');
       
       body {
           font-family: 'Inter', sans-serif;
           background-color: #ffffff;
           color: #0f172a;
           -webkit-tap-highlight-color: transparent;
           overflow-x: hidden;
       }

       /* Unified Shake Animation for Interactive Icons */
       @keyframes icon-shake {
           0%, 85%, 100% { transform: translateX(0); }
           87% { transform: translateX(-4px) rotate(-3deg); }
           90% { transform: translateX(4px) rotate(3deg); }
           93% { transform: translateX(-4px) rotate(-3deg); }
           96% { transform: translateX(4px) rotate(3deg); }
       }

       .shake-icon {
           animation: icon-shake 3s ease-in-out infinite;
       }

       /* Nexus Button Design */
       .nexus-btn {
           width: 112px; 
           height: 96px;
           transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
           display: flex;
           align-items: center;
           justify-content: center;
           border-radius: 2.5rem;
           cursor: pointer;
           z-index: 20;
       }
       
       .nexus-btn.active {
           transform: rotate(90deg);
           background-color: #ef4444 !important;
           box-shadow: none !important;
           animation: none !important;
       }

       /* Expandable Container Logic */
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
           margin-top: 2rem;
       }

       /* Modern Glass UI */
       .glass-card {
           background: rgba(248, 250, 252, 0.8);
           backdrop-filter: blur(8px);
           border: 1px solid #f1f5f9;
           box-shadow: 0 4px 20px -5px rgba(0, 0, 0, 0.05);
       }

       /* Pulse Animation for CTA Buttons */
       .pulse-wave {
           animation: pulse 2s infinite;
       }

       @keyframes pulse {
           0% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0.4); }
           70% { box-shadow: 0 0 0 15px rgba(37, 99, 235, 0); }
           100% { box-shadow: 0 0 0 0 rgba(37, 99, 235, 0); }
       }

       .no-scrollbar::-webkit-scrollbar { display: none; }
   </style>
</head>
<body class="pb-40 no-scrollbar">

   <!-- Navigation -->
   <nav class="p-6 flex justify-between items-center fixed top-0 w-full z-50 bg-white/80 backdrop-blur-md border-b border-slate-100">
       <div class="text-[9px] font-black tracking-[0.3em] text-blue-600 uppercase">PMP® CERTIFIED</div>
       <div class="flex gap-3">
           <a href="https://www.linkedin.com/in/aditya-sachidanandham" target="_blank" class="w-9 h-9 rounded-xl bg-slate-50 flex items-center justify-center border border-slate-200 text-blue-600 active:scale-90 transition-transform">
               <i class="fa-brands fa-linkedin-in text-sm"></i>
           </a>
           <button onclick="window.location.href='mailto:sachidanandhamaditya@gmail.com'" class="w-9 h-9 rounded-xl bg-slate-50 flex items-center justify-center border border-slate-200 text-slate-600 active:scale-90 transition-transform cursor-pointer">
               <i class="fa-solid fa-envelope text-sm"></i>
           </button>
       </div>
   </nav>

   <!-- Hero Content -->
   <section class="pt-32 px-6 text-center">
       <div class="inline-block px-3 py-1 bg-blue-50 border border-blue-100 rounded-full text-[9px] font-black text-blue-600 uppercase tracking-widest mb-6">
           Project Management Professional
       </div>
       <h1 class="text-5xl font-black tracking-tighter uppercase leading-[0.9] mb-8 text-slate-900">
           Aditya<br><span class="text-blue-600">Sachidanandham</span>
       </h1>
       <p class="text-slate-500 text-sm font-bold leading-relaxed mb-12 max-w-xs mx-auto uppercase">
           PMP-Certified project management professional with 3+ years delivering $50M+ automation installation projects for semiconductor leaders.
       </p>

       <!-- Dynamic Metrics -->
       <div class="grid grid-cols-3 gap-2 mb-16">
           <div class="glass-card p-4 rounded-2xl">
               <i class="fa-solid fa-briefcase text-blue-600 mb-2 text-sm"></i>
               <div class="text-xl font-black text-slate-900">$50M+</div>
               <div class="text-[7px] font-bold text-slate-400 uppercase">Portfolio Value</div>
           </div>
           <div class="glass-card p-4 rounded-2xl">
               <i class="fa-solid fa-circle-check text-emerald-500 mb-2 text-sm"></i>
               <div class="text-xl font-black text-slate-900">98%</div>
               <div class="text-[7px] font-bold text-slate-400 uppercase">On-Time</div>
           </div>
           <div class="glass-card p-4 rounded-2xl">
               <i class="fa-solid fa-arrow-trend-up text-blue-600 mb-2 text-sm"></i>
               <div class="text-xl font-black text-slate-900">11%</div>
               <div class="text-[7px] font-bold text-slate-400 uppercase">Efficiency</div>
           </div>
       </div>
   </section>

   <!-- Experience Timeline Interaction -->
   <section class="px-6 py-10 flex flex-col items-center">
       <h2 class="text-3xl font-black text-blue-600 uppercase tracking-tighter mb-10 text-center">Experience</h2>
       <button id="expBtn" onclick="toggleSection('exp')" class="nexus-btn bg-blue-600 shadow-xl shadow-blue-200 pulse-wave">
           <i id="expIcon" class="fa-solid fa-briefcase text-3xl text-white shake-icon"></i>
       </button>

       <div id="expContent" class="exp-container space-y-4">
           <div class="glass-card p-6 rounded-[2rem] border-l-4 border-blue-600 mt-4">
               <div class="text-blue-600 font-black text-[9px] mb-2 uppercase tracking-widest">Mar 2025 — Jan 2026</div>
               <h3 class="text-xl font-black uppercase tracking-tight text-slate-900">Installation Manager</h3>
               <p class="text-xs font-bold text-slate-400 mb-4 uppercase">STMicroelectronics</p>
               <p class="text-[11px] text-slate-500 font-medium leading-relaxed uppercase">• Led $20M automation project coordinating 100+ subcontractors.</p>
           </div>
           <div class="glass-card p-6 rounded-[2rem] border-l-4 border-slate-200">
               <div class="text-slate-400 font-black text-[9px] mb-2 uppercase tracking-widest">Aug 2024 — Feb 2025</div>
               <h3 class="text-xl font-black uppercase tracking-tight text-slate-900">Site Manager</h3>
               <p class="text-xs font-bold text-slate-400 mb-4 uppercase">Texas Instruments</p>
               <p class="text-[11px] text-slate-500 font-medium leading-relaxed uppercase">• $50M On-site execution management with 31% faster resolution.</p>
           </div>
           <div class="glass-card p-6 rounded-[2rem] border-l-4 border-slate-200">
               <div class="text-slate-400 font-black text-[9px] mb-2 uppercase tracking-widest">Jul 2022 — Jul 2024</div>
               <h3 class="text-xl font-black uppercase tracking-tight text-slate-900">Engineer</h3>
               <p class="text-xs font-bold text-slate-400 mb-4 uppercase">UMC, Soitec, Siltronic</p>
               <p class="text-[11px] text-slate-500 font-medium leading-relaxed uppercase">• Collaborated on 5 complex $12M+ projects leading risk mitigation.</p>
           </div>
       </div>
   </section>

   <!-- Stress Test Simulator -->
   <section class="px-6 py-10 flex flex-col items-center">
       <h2 class="text-3xl font-black text-slate-800 uppercase tracking-tighter mb-10 text-center">Simulator</h2>
       <button id="simBtn" onclick="toggleSection('sim')" class="nexus-btn bg-slate-800 shadow-xl shadow-blue-200 pulse-wave">
           <i id="simIcon" class="fa-solid fa-microchip text-3xl text-white shake-icon"></i>
       </button>

       <div id="simContent" class="exp-container">
           <div class="bg-slate-50 rounded-[2.5rem] p-8 border border-slate-100 shadow-inner mt-4 w-full">
               <h3 class="text-[9px] font-black text-blue-600 tracking-widest uppercase mb-2">PMP Simulation Mode</h3>
               <div id="simDisplay" class="p-6 bg-white rounded-2xl mb-6 text-center border border-slate-200 shadow-sm">
                   <div id="healthText" class="text-3xl font-black text-emerald-500">100%</div>
                   <div id="statusText" class="text-[9px] font-bold text-emerald-400 uppercase tracking-widest mt-1 italic">Optimal Performance</div>
               </div>
               <button id="runSimBtn" onclick="runSim()" class="w-full py-4 bg-slate-900 text-white rounded-xl font-black text-[10px] uppercase tracking-widest active:scale-95">
                   Initiate Stress Test
               </button>
               <div id="simSolution" class="hidden mt-6 p-4 border-l-2 border-blue-600 bg-blue-50">
                   <p class="text-[10px] font-bold text-blue-700 uppercase mb-1">Protocol: RCA & Schedule Compression</p>
                   <p class="text-[10px] text-slate-500 italic">"Mitigating 21% schedule delay through resource leveling..."</p>
               </div>
           </div>
       </div>
   </section>

   <!-- Academics Section -->
   <section class="px-6 py-10 flex flex-col items-center">
       <h2 class="text-3xl font-black text-blue-600 uppercase tracking-tighter mb-10 text-center">Academic</h2>
       <button id="acadBtn" onclick="toggleSection('acad')" class="nexus-btn bg-blue-500 shadow-xl shadow-blue-200 pulse-wave">
           <i id="acadIcon" class="fa-solid fa-graduation-cap text-3xl text-white shake-icon"></i>
       </button>

       <div id="acadContent" class="exp-container space-y-4">
           <div class="glass-card p-6 rounded-3xl text-center mt-4">
               <i class="fa-solid fa-graduation-cap text-blue-600 mb-4"></i>
               <h4 class="text-md font-black uppercase text-slate-900 leading-tight">M.Sc Project Management</h4>
               <p class="text-[8px] font-bold text-slate-400 uppercase mt-2">NTU Singapore<br>GPA: 4.14</p>
           </div>
           <div class="glass-card p-6 rounded-3xl text-center">
               <i class="fa-solid fa-user-graduate text-slate-400 mb-4"></i>
               <h4 class="text-md font-black uppercase text-slate-900 leading-tight">B.Tech Aerospace</h4>
               <p class="text-[8px] font-bold text-slate-400 uppercase mt-2">PM Institute<br>GPA: 4.07</p>
           </div>
       </div>
   </section>

   <!-- CTA Footer -->
   <section class="px-6 py-20 text-center">
       <h2 class="text-4xl font-black uppercase tracking-tighter text-slate-900 mb-10 leading-none">Ready to<br><span class="text-blue-600">Optimise?</span></h2>
       <div class="flex justify-center">
           <a href="https://forms.gle/uRQ48wjMT6mmZWS99" target="_blank" class="px-12 py-4 bg-blue-600 text-white rounded-full font-black text-[10px] uppercase tracking-[0.2em] shadow-lg active:scale-95 transition-all">
               Let's Connect
           </a>
       </div>
       <p class="text-slate-400 text-[9px] font-bold uppercase tracking-widest mt-8">Solving complex operational challenges</p>
   </section>

   <script>
       // Toggle Expandable Content
       function toggleSection(type) {
           const btn = document.getElementById(type + 'Btn');
           const icon = document.getElementById(type + 'Icon');
           const content = document.getElementById(type + 'Content');
           
           const isClosing = btn.classList.contains('active');
           
           btn.classList.toggle('active');
           content.classList.toggle('show');
           
           const originalIcons = { exp: 'fa-briefcase', sim: 'fa-microchip', acad: 'fa-graduation-cap' };
           if (!isClosing) {
               icon.className = 'fa-solid fa-xmark text-3xl text-white';
               setTimeout(() => content.scrollIntoView({ behavior: 'smooth', block: 'center' }), 300);
           } else {
               icon.className = `fa-solid ${originalIcons[type]} text-3xl text-white shake-icon`;
           }
       }

       // PMP Stress Test Simulation Logic
       let simState = 0; 
       function runSim() {
           const health = document.getElementById('healthText');
           const status = document.getElementById('statusText');
           const btn = document.getElementById('runSimBtn');
           const sol = document.getElementById('simSolution');

           if (simState === 0) {
               health.innerText = "65%";
               health.className = "text-3xl font-black text-red-500";
               status.innerText = "Schedule Conflict Detected";
               status.className = "text-[9px] font-bold text-red-500 uppercase tracking-widest mt-1";
               btn.innerText = "Apply PMP Mitigation";
               simState = 1;
           } else if (simState === 1) {
               btn.innerText = "Optimizing...";
               btn.disabled = true;
               sol.classList.remove('hidden');
               let val = 65;
               const interval = setInterval(() => {
                   val += 3;
                   health.innerText = val + "%";
                   if (val >= 98) {
                       clearInterval(interval);
                       health.innerText = "98%";
                       health.className = "text-3xl font-black text-blue-600";
                       status.innerText = "Timeline Recovered";
                       status.className = "text-[9px] font-bold text-blue-600 uppercase tracking-widest mt-1";
                       btn.innerText = "Reset Simulation";
                       btn.disabled = false;
                       btn.onclick = () => window.location.reload();
                   }
               }, 40);
           }
       }
   </script>
</body>
</html>
