<template>
  <section class="relative w-full overflow-hidden">
    <!-- Background image is the single source of truth for section dimensions -->
    <img
      src="/features-background.png"
      alt="Features Background"
      class="w-full h-auto block"
    />

    <!-- Content overlay - absolutely positioned, fills the entire section -->
    <div class="absolute inset-0 z-10 flex flex-col justify-center items-center px-4 sm:px-8 md:px-12 lg:px-16 py-8 lg:py-12">
      
      <!-- Header -->
      <div class="text-center mb-6 lg:mb-8">
        <div class="inline-flex items-center gap-2 mb-4">
          <svg class="w-4 h-4 text-indigo-500" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
          </svg>
          <span class="text-xs font-semibold tracking-widest text-slate-500 uppercase">Features</span>
        </div>
        <h2 class="text-2xl md:text-4xl lg:text-5xl font-semibold text-slate-800 tracking-tight mb-3 leading-tight">
          Powerful features for <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 via-indigo-500 to-purple-500">high-impact</span> teams
        </h2>
        <p class="text-slate-500 text-sm md:text-base max-w-lg mx-auto leading-relaxed">
          Chronova's AI-native features help teams plan smarter,<br class="hidden md:block" />
          move faster, and deliver what matters.
        </p>
      </div>

      <!-- 2x2 Grid of Feature Cards -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:gap-5 w-full max-w-5xl mx-auto">

        <!-- ===== CARD 1: AI Task Generation ===== -->
        <div class="bg-white/70 backdrop-blur-xl rounded-[2rem] border border-white/80 shadow-[0_8px_30px_rgba(0,0,0,0.06)] p-6 flex flex-col h-[300px] lg:h-[320px] overflow-hidden group">
          <!-- Top -->
          <div class="flex items-start justify-between mb-3">
            <div class="flex items-center gap-4">
              <div class="w-14 h-14 rounded-3xl bg-white/90 shadow-[0_4px_20px_rgba(0,0,0,0.03)] border border-white flex items-center justify-center flex-shrink-0">
                <svg class="w-7 h-7 text-indigo-500" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
                </svg>
              </div>
              <div>
                <h3 class="text-base font-bold text-slate-800">AI Task Generation</h3>
                <p class="text-[13px] text-slate-500 mt-1 leading-relaxed max-w-[280px]">Turn natural language into structured<br/>tasks with subtasks, owners, and due dates.</p>
              </div>
            </div>
            <svg class="w-4 h-4 text-indigo-300 flex-shrink-0 mt-1" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
            </svg>
          </div>

          <!-- Mockup -->
          <div class="flex-grow flex flex-col justify-center gap-4 transform transition-all duration-700 ease-[cubic-bezier(0.23,1,0.32,1)] translate-y-20 opacity-40 group-hover:translate-y-0 group-hover:opacity-100">
            <!-- Input bar -->
            <div class="flex items-center gap-3 bg-white border border-slate-200 rounded-2xl px-4 py-3 shadow-sm">
              <svg class="w-4 h-4 text-indigo-400 flex-shrink-0" viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
              </svg>
              <span class="text-sm text-slate-600 flex-grow">Draft a launch plan for <span class="text-indigo-500 font-semibold">v2</span></span>
              <div class="w-8 h-8 rounded-full bg-gradient-to-br from-indigo-500 to-purple-600 flex items-center justify-center flex-shrink-0">
                <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 10l7-7m0 0l7 7m-7-7v18"/>
                </svg>
              </div>
            </div>
            <!-- Status -->
            <div class="flex items-center gap-2 pl-1">
              <div class="w-5 h-5 rounded-full bg-indigo-500 flex items-center justify-center flex-shrink-0">
                <svg class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"/></svg>
              </div>
              <span class="text-xs text-slate-500 font-medium">12 tasks generated</span>
            </div>
          </div>
        </div>

        <!-- ===== CARD 2: Smart Scheduling ===== -->
        <div class="bg-white/70 backdrop-blur-xl rounded-[2rem] border border-white/80 shadow-[0_8px_30px_rgba(0,0,0,0.06)] p-6 flex flex-col h-[300px] lg:h-[320px] overflow-hidden group">
          <!-- Top -->
          <div class="flex items-start justify-between mb-3">
            <div class="flex items-center gap-4">
              <div class="w-14 h-14 rounded-3xl bg-white/90 shadow-[0_4px_20px_rgba(0,0,0,0.03)] border border-white flex items-center justify-center flex-shrink-0">
                <svg class="w-7 h-7 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/>
                </svg>
              </div>
              <div>
                <h3 class="text-base font-bold text-slate-800">Smart Scheduling</h3>
                <p class="text-[13px] text-slate-500 mt-1 leading-relaxed max-w-[280px]">AI finds the best time for your deep work,<br/>meetings, and important deadlines.</p>
              </div>
            </div>
            <svg class="w-4 h-4 text-indigo-300 flex-shrink-0 mt-1" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
            </svg>
          </div>

          <!-- Mockup: Calendar + Schedule -->
          <div class="flex-grow flex gap-3 overflow-hidden transform transition-all duration-700 ease-[cubic-bezier(0.23,1,0.32,1)] translate-y-20 opacity-40 group-hover:translate-y-0 group-hover:opacity-100">
            <!-- Mini Calendar -->
            <div class="bg-white/80 rounded-xl border border-slate-100 p-3 flex-shrink-0 w-[155px]">
              <div class="flex items-center justify-between mb-2">
                <svg class="w-3 h-3 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/></svg>
                <span class="text-[10px] font-semibold text-slate-600">May 2024</span>
                <svg class="w-3 h-3 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/></svg>
              </div>
              <div class="grid grid-cols-7 gap-y-1 text-center">
                <span class="text-[9px] text-slate-400 font-medium">S</span>
                <span class="text-[9px] text-slate-400 font-medium">M</span>
                <span class="text-[9px] text-slate-400 font-medium">T</span>
                <span class="text-[9px] text-slate-400 font-medium">W</span>
                <span class="text-[9px] text-slate-400 font-medium">T</span>
                <span class="text-[9px] text-slate-400 font-medium">F</span>
                <span class="text-[9px] text-slate-400 font-medium">S</span>
                <span class="text-[9px] text-slate-300">1</span>
                <span class="text-[9px] text-slate-300">2</span>
                <span class="text-[9px] text-slate-500">3</span>
                <span class="text-[9px] text-slate-500">4</span>
                <span class="text-[9px] text-slate-500">5</span>
                <span class="text-[9px] text-slate-500">6</span>
                <span class="text-[9px] text-slate-300">7</span>
                <span class="text-[9px] text-slate-300">8</span>
                <span class="text-[9px] text-slate-500">9</span>
                <span class="text-[9px] text-slate-500">10</span>
                <span class="text-[9px] text-slate-500">11</span>
                <span class="text-[9px] text-slate-500">12</span>
                <span class="text-[9px] text-slate-500">13</span>
                <span class="text-[9px] text-slate-300">14</span>
                <span class="text-[9px] text-slate-300">15</span>
                <span class="text-[9px] text-slate-500">16</span>
                <span class="text-[9px] text-slate-500">17</span>
                <span class="text-[9px] text-slate-500">18</span>
                <span class="text-[9px] text-slate-500">19</span>
                <span class="text-[9px] text-slate-500">20</span>
                <span class="text-[9px] text-slate-300">21</span>
                <span class="text-[9px] text-slate-300">22</span>
                <span class="text-[9px] text-slate-500">23</span>
                <span class="text-[9px] w-5 h-5 rounded-full bg-indigo-500 text-white flex items-center justify-center mx-auto">24</span>
                <span class="text-[9px] text-slate-500">25</span>
                <span class="text-[9px] text-slate-500">26</span>
                <span class="text-[9px] text-slate-300">27</span>
                <span class="text-[9px] text-slate-300">28</span>
                <span class="text-[9px] text-slate-500">29</span>
                <span class="text-[9px] text-slate-500">30</span>
                <span class="text-[9px] text-slate-500">31</span>
              </div>
            </div>
            <!-- Time Blocks -->
            <div class="flex-grow flex flex-col gap-2 overflow-hidden">
              <div class="flex gap-2 items-start">
                <span class="text-[9px] text-slate-400 font-medium w-6 flex-shrink-0 pt-1">9 AM</span>
                <div class="flex-grow bg-indigo-50 border border-indigo-100 rounded-lg p-2">
                  <p class="text-[10px] font-semibold text-indigo-700">Design Review</p>
                  <p class="text-[9px] text-indigo-400">9:00 – 10:00 AM</p>
                </div>
              </div>
              <div class="flex gap-2 items-start">
                <span class="text-[9px] text-slate-400 font-medium w-6 flex-shrink-0 pt-1">10 AM</span>
                <div class="flex-grow bg-blue-50 border border-blue-100 rounded-lg p-2">
                  <p class="text-[10px] font-semibold text-blue-700">Deep Work</p>
                  <p class="text-[9px] text-blue-400">10:30 AM – 12:00 PM</p>
                </div>
              </div>
              <div class="flex gap-2 items-start">
                <span class="text-[9px] text-slate-400 font-medium w-6 flex-shrink-0 pt-1">1 PM</span>
                <div class="flex-grow bg-purple-50 border border-purple-100 rounded-lg p-2">
                  <p class="text-[10px] font-semibold text-purple-700">Roadmap Planning</p>
                  <p class="text-[9px] text-purple-400">1:00 – 2:00 PM</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- ===== CARD 3: Focus Recommendations ===== -->
        <div class="bg-white/70 backdrop-blur-xl rounded-[2rem] border border-white/80 shadow-[0_8px_30px_rgba(0,0,0,0.06)] p-6 flex flex-col h-[300px] lg:h-[320px] overflow-hidden group">
          <!-- Top -->
          <div class="flex items-start justify-between mb-3">
            <div class="flex items-center gap-4">
              <div class="w-14 h-14 rounded-3xl bg-white/90 shadow-[0_4px_20px_rgba(0,0,0,0.03)] border border-white flex items-center justify-center flex-shrink-0">
                <svg class="w-7 h-7 text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <circle cx="12" cy="12" r="3" stroke-width="2"/>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 1v2m0 18v2M4.22 4.22l1.42 1.42m10.72 10.72l1.42 1.42M1 12h2m18 0h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"/>
                </svg>
              </div>
              <div>
                <h3 class="text-base font-bold text-slate-800">Focus Recommendations</h3>
                <p class="text-[13px] text-slate-500 mt-1 leading-relaxed max-w-[280px]">AI analyzes your context and surfaces<br/>what will drive the most impact today.</p>
              </div>
            </div>
            <svg class="w-4 h-4 text-indigo-300 flex-shrink-0 mt-1" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
            </svg>
          </div>

          <!-- Mockup: Score + List -->
          <div class="flex-grow flex gap-4 overflow-hidden transform transition-all duration-700 ease-[cubic-bezier(0.23,1,0.32,1)] translate-y-20 opacity-40 group-hover:translate-y-0 group-hover:opacity-100">
            <!-- Left: Score -->
            <div class="w-[120px] flex-shrink-0 flex flex-col justify-between">
              <div>
                <p class="text-xs text-slate-500 font-medium mb-1">Focus Score</p>
                <p class="text-4xl font-bold text-slate-800">87</p>
                <p class="text-xs text-indigo-500 font-medium">Great focus</p>
              </div>
              <!-- Mini chart SVG -->
              <div class="w-full h-14">
                <svg viewBox="0 0 100 40" class="w-full h-full" fill="none">
                  <polyline
                    points="0,35 20,28 40,30 55,18 70,12 90,5 100,8"
                    stroke="url(#focusGrad)"
                    stroke-width="2.5"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <polygon
                    points="0,35 20,28 40,30 55,18 70,12 90,5 100,8 100,40 0,40"
                    fill="url(#focusFill)"
                    opacity="0.3"
                  />
                  <defs>
                    <linearGradient id="focusGrad" x1="0" y1="0" x2="100" y2="0" gradientUnits="userSpaceOnUse">
                      <stop offset="0%" stop-color="#818cf8"/>
                      <stop offset="100%" stop-color="#a78bfa"/>
                    </linearGradient>
                    <linearGradient id="focusFill" x1="0" y1="0" x2="0" y2="1">
                      <stop offset="0%" stop-color="#818cf8"/>
                      <stop offset="100%" stop-color="#818cf8" stop-opacity="0"/>
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <p class="text-[9px] text-slate-400 flex items-center gap-1">
                <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"/></svg>
                Updated just now
              </p>
            </div>
            <!-- Right: Task List -->
            <div class="flex-grow flex flex-col gap-2 justify-center">
              <div class="bg-white/80 rounded-xl border border-slate-100 p-3 flex items-center gap-3">
                <svg class="w-4 h-4 text-slate-400 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"/></svg>
                <div class="flex-grow min-w-0">
                  <p class="text-[11px] font-semibold text-slate-700 truncate">Finish roadmap update</p>
                  <p class="text-[10px] text-slate-400">High impact</p>
                </div>
                <span class="text-[10px] font-bold text-slate-600 bg-slate-100 px-2 py-0.5 rounded-md flex-shrink-0">92</span>
              </div>
              <div class="bg-white/80 rounded-xl border border-slate-100 p-3 flex items-center gap-3">
                <svg class="w-4 h-4 text-slate-400 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0z"/></svg>
                <div class="flex-grow min-w-0">
                  <p class="text-[11px] font-semibold text-slate-700 truncate">User research synthesis</p>
                  <p class="text-[10px] text-slate-400">High impact</p>
                </div>
                <span class="text-[10px] font-bold text-slate-600 bg-slate-100 px-2 py-0.5 rounded-md flex-shrink-0">85</span>
              </div>
              <div class="bg-white/80 rounded-xl border border-slate-100 p-3 flex items-center gap-3">
                <svg class="w-4 h-4 text-slate-400 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                <div class="flex-grow min-w-0">
                  <p class="text-[11px] font-semibold text-slate-700 truncate">Email triage</p>
                  <p class="text-[10px] text-slate-400">Low impact</p>
                </div>
                <span class="text-[10px] font-bold text-slate-500 bg-slate-100 px-2 py-0.5 rounded-md flex-shrink-0">32</span>
              </div>
            </div>
          </div>
        </div>

        <!-- ===== CARD 4: Motion-first Kanban ===== -->
        <div class="bg-white/70 backdrop-blur-xl rounded-[2rem] border border-white/80 shadow-[0_8px_30px_rgba(0,0,0,0.06)] p-6 flex flex-col h-[300px] lg:h-[320px] overflow-hidden group">
          <!-- Top -->
          <div class="flex items-start justify-between mb-3">
            <div class="flex items-center gap-4">
              <div class="w-14 h-14 rounded-3xl bg-white/90 shadow-[0_4px_20px_rgba(0,0,0,0.03)] border border-white flex items-center justify-center flex-shrink-0">
                <svg class="w-7 h-7 text-teal-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"/>
                </svg>
              </div>
              <div>
                <h3 class="text-base font-bold text-slate-800">Motion-first Kanban</h3>
                <p class="text-[13px] text-slate-500 mt-1 leading-relaxed max-w-[280px]">A fluid, drag-and-drop Kanban that<br/>keeps work moving with clarity.</p>
              </div>
            </div>
            <svg class="w-4 h-4 text-indigo-300 flex-shrink-0 mt-1" viewBox="0 0 24 24" fill="currentColor">
              <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
            </svg>
          </div>

          <!-- Mockup: Kanban Board -->
          <div class="flex-grow flex gap-2 overflow-hidden transform transition-all duration-700 ease-[cubic-bezier(0.23,1,0.32,1)] translate-y-20 opacity-40 group-hover:translate-y-0 group-hover:opacity-100">
            <!-- Backlog -->
            <div class="flex-1 flex flex-col gap-1.5 min-w-0">
              <div class="flex items-center gap-1.5 mb-1">
                <span class="text-[10px] font-semibold text-slate-600">Backlog</span>
                <span class="text-[9px] bg-slate-100 text-slate-500 font-bold rounded px-1">8</span>
              </div>
              <div class="bg-white border border-slate-100 rounded-xl p-2.5 shadow-sm">
                <p class="text-[10px] font-medium text-slate-700 mb-1.5">Competitive analysis</p>
                <span class="text-[9px] bg-indigo-100 text-indigo-600 font-semibold px-2 py-0.5 rounded-full">Strategy</span>
              </div>
              <div class="bg-white border border-slate-100 rounded-xl p-2.5 shadow-sm opacity-60">
                <div class="flex items-center gap-1">
                  <svg class="w-3 h-3 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"/></svg>
                  <p class="text-[10px] text-slate-400">Add task</p>
                </div>
              </div>
            </div>
            <!-- In Progress -->
            <div class="flex-1 flex flex-col gap-1.5 min-w-0">
              <div class="flex items-center gap-1.5 mb-1">
                <span class="text-[10px] font-semibold text-slate-600">In Progress</span>
                <span class="text-[9px] bg-blue-100 text-blue-500 font-bold rounded px-1">5</span>
              </div>
              <div class="bg-white border border-slate-100 rounded-xl p-2.5 shadow-sm">
                <p class="text-[10px] font-medium text-slate-700 mb-1.5">Design system update</p>
                <div class="flex items-center justify-between">
                  <span class="text-[9px] bg-blue-100 text-blue-600 font-semibold px-2 py-0.5 rounded-full">Design</span>
                  <img class="w-5 h-5 rounded-full object-cover border border-white" src="https://i.pravatar.cc/40?img=33" alt="a"/>
                </div>
              </div>
              <!-- Dragging card -->
              <div class="bg-white border border-indigo-200 rounded-xl p-2.5 shadow-md rotate-2 relative">
                <p class="text-[10px] font-medium text-slate-700 mb-1.5">Integrations audit</p>
                <span class="text-[9px] bg-teal-100 text-teal-600 font-semibold px-2 py-0.5 rounded-full">Research</span>
                <!-- Cursor icon -->
                <div class="absolute -bottom-2 -right-2 bg-white rounded-full w-6 h-6 flex items-center justify-center shadow-md border border-slate-100">
                  <svg class="w-3.5 h-3.5 text-slate-500" fill="currentColor" viewBox="0 0 24 24"><path d="M4 0l16 12.279-6.951 1.17 4.325 8.817-3.596 1.734-4.35-8.879L4 18.617V0z"/></svg>
                </div>
              </div>
            </div>
            <!-- Done -->
            <div class="flex-1 flex flex-col gap-1.5 min-w-0">
              <div class="flex items-center gap-1.5 mb-1">
                <span class="text-[10px] font-semibold text-slate-600">Done</span>
                <span class="text-[9px] bg-green-100 text-green-600 font-bold rounded px-1">12</span>
              </div>
              <div class="bg-white border border-slate-100 rounded-xl p-2.5 shadow-sm">
                <div class="flex items-center gap-1 mb-1.5">
                  <div class="w-2 h-2 rounded-full bg-green-400"></div>
                  <p class="text-[10px] font-medium text-slate-700">Brand guidelines</p>
                </div>
                <span class="text-[9px] bg-blue-100 text-blue-600 font-semibold px-2 py-0.5 rounded-full">Design</span>
              </div>
              <div class="bg-white border border-slate-100 rounded-xl p-2.5 shadow-sm">
                <div class="flex items-center gap-1 mb-1.5">
                  <div class="w-2 h-2 rounded-full bg-green-400"></div>
                  <p class="text-[10px] font-medium text-slate-700">Release v1.2</p>
                </div>
                <div class="flex items-center justify-between">
                  <span class="text-[9px] bg-purple-100 text-purple-600 font-semibold px-2 py-0.5 rounded-full">Product</span>
                  <img class="w-5 h-5 rounded-full object-cover border border-white" src="https://i.pravatar.cc/40?img=12" alt="a"/>
                </div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
</script>
