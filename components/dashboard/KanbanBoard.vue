<template>
  <div class="bg-transparent flex gap-6 overflow-x-auto pb-4 no-scrollbar">
    
    <!-- Column: Backlog -->
    <div class="flex-shrink-0 w-80 flex flex-col gap-4">
      <div class="flex items-center justify-between mb-1">
        <div class="flex items-center gap-2">
          <h3 class="font-bold text-slate-800 text-sm">Backlog</h3>
          <span class="px-2 py-0.5 rounded-full bg-slate-200 text-[10px] font-bold text-slate-600">7</span>
        </div>
        <button class="text-slate-400 hover:text-slate-600"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path></svg></button>
      </div>

      <!-- Card 1 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-purple-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">Competitor analysis</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-12</span>
          <div class="w-6 h-6 rounded-full bg-slate-100 flex items-center justify-center text-[10px] font-bold text-slate-600 border border-white ring-1 ring-slate-200">JD</div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-blue-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">User research synthesis</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-18</span>
          <div class="w-6 h-6 rounded-full bg-indigo-100 flex items-center justify-center text-[10px] font-bold text-indigo-700 border border-white ring-1 ring-indigo-200">AK</div>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-emerald-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">Technical audit</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-25</span>
          <div class="w-6 h-6 rounded-full bg-slate-100 flex items-center justify-center text-[10px] font-bold text-slate-600 border border-white ring-1 ring-slate-200">DS</div>
        </div>
      </div>

      <!-- Card 4 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-purple-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">Feature brainstorming</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-21</span>
          <div class="w-6 h-6 rounded-full bg-pink-100 flex items-center justify-center text-[10px] font-bold text-pink-700 border border-white ring-1 ring-pink-200">PR</div>
        </div>
      </div>
      
      <button class="flex items-center gap-2 text-sm font-medium text-slate-400 hover:text-indigo-600 transition-colors mt-2">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
        Add task
      </button>
    </div>

    <!-- Column: In Progress -->
    <div class="flex-shrink-0 w-80 flex flex-col gap-4">
      <div class="flex items-center justify-between mb-1">
        <div class="flex items-center gap-2">
          <h3 class="font-bold text-slate-800 text-sm">In Progress</h3>
          <span class="px-2 py-0.5 rounded-full bg-blue-100 text-[10px] font-bold text-blue-700">4</span>
        </div>
        <button class="text-slate-400 hover:text-slate-600"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path></svg></button>
      </div>

      <!-- Card 1 -->
      <div class="bg-white rounded-xl p-4 border border-blue-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer ring-1 ring-blue-100">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-blue-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">UI/UX Design System</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-02</span>
          <div class="flex items-center gap-3">
            <span class="flex items-center gap-1 text-[11px] text-slate-400 font-medium">
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
              2
            </span>
            <div class="w-6 h-6 rounded-full bg-indigo-100 flex items-center justify-center text-[10px] font-bold text-indigo-700 border border-white ring-1 ring-indigo-200">AK</div>
          </div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-blue-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">API Integrations</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-04</span>
          <div class="flex items-center gap-3">
            <span class="flex items-center gap-1 text-[11px] text-slate-400 font-medium">
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
              3
            </span>
            <div class="w-6 h-6 rounded-full bg-slate-100 flex items-center justify-center text-[10px] font-bold text-slate-600 border border-white ring-1 ring-slate-200">JD</div>
          </div>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-emerald-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">Dashboard development</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-08</span>
          <div class="flex items-center gap-3">
            <span class="flex items-center gap-1 text-[11px] text-slate-400 font-medium">
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
              5
            </span>
            <div class="w-6 h-6 rounded-full bg-slate-100 flex items-center justify-center text-[10px] font-bold text-slate-600 border border-white ring-1 ring-slate-200">DS</div>
          </div>
        </div>
      </div>

      <button class="flex items-center gap-2 text-sm font-medium text-slate-400 hover:text-indigo-600 transition-colors mt-2">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
        Add task
      </button>
    </div>

    <!-- Column: Scheduled -->
    <div class="flex-shrink-0 w-80 flex flex-col gap-4">
      <div class="flex items-center justify-between mb-1">
        <div class="flex items-center gap-2">
          <h3 class="font-bold text-slate-800 text-sm">Scheduled</h3>
          <span class="px-2 py-0.5 rounded-full bg-fuchsia-100 text-[10px] font-bold text-fuchsia-700">3</span>
        </div>
        <button class="text-slate-400 hover:text-slate-600"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path></svg></button>
      </div>

      <!-- Card 1 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-purple-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">Beta testing</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-15</span>
          <div class="w-6 h-6 rounded-full bg-indigo-100 flex items-center justify-center text-[10px] font-bold text-indigo-700 border border-white ring-1 ring-indigo-200">AK</div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white rounded-xl p-4 border border-slate-200 shadow-sm hover:shadow-md transition-shadow cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-emerald-500 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-800 text-sm leading-snug">Content creation</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-16</span>
          <div class="w-6 h-6 rounded-full bg-slate-100 flex items-center justify-center text-[10px] font-bold text-slate-600 border border-white ring-1 ring-slate-200">JD</div>
        </div>
      </div>
      
      <button class="flex items-center gap-2 text-sm font-medium text-slate-400 hover:text-indigo-600 transition-colors mt-2">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
        Add task
      </button>
    </div>

    <!-- Column: Done -->
    <div class="flex-shrink-0 w-80 flex flex-col gap-4">
      <div class="flex items-center justify-between mb-1">
        <div class="flex items-center gap-2">
          <h3 class="font-bold text-slate-800 text-sm">Done</h3>
          <span class="px-2 py-0.5 rounded-full bg-emerald-100 text-[10px] font-bold text-emerald-700">6</span>
        </div>
        <button class="text-slate-400 hover:text-slate-600"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"></path></svg></button>
      </div>

      <!-- Card 1 -->
      <div class="bg-white/60 rounded-xl p-4 border border-slate-200 shadow-sm opacity-75 cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-slate-300 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-600 text-sm leading-snug line-through decoration-slate-300">Project kickoff</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-01</span>
          <div class="flex items-center gap-2">
            <div class="w-6 h-6 rounded-full bg-slate-100 flex items-center justify-center text-[10px] font-bold text-slate-600 border border-white ring-1 ring-slate-200">JD</div>
            <div class="w-5 h-5 rounded-full bg-emerald-100 flex items-center justify-center text-emerald-600">
              <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
            </div>
          </div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white/60 rounded-xl p-4 border border-slate-200 shadow-sm opacity-75 cursor-pointer">
        <div class="flex items-start gap-2 mb-3">
          <span class="w-2 h-2 rounded-full bg-slate-300 mt-1.5 flex-shrink-0"></span>
          <h4 class="font-semibold text-slate-600 text-sm leading-snug line-through decoration-slate-300">Requirements gathering</h4>
        </div>
        <div class="flex items-center justify-between mt-4">
          <span class="text-[11px] font-bold text-slate-400">PMAR-03</span>
          <div class="flex items-center gap-2">
            <div class="w-6 h-6 rounded-full bg-indigo-100 flex items-center justify-center text-[10px] font-bold text-indigo-700 border border-white ring-1 ring-indigo-200">AK</div>
            <div class="w-5 h-5 rounded-full bg-emerald-100 flex items-center justify-center text-emerald-600">
              <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
            </div>
          </div>
        </div>
      </div>
      
      <button class="flex items-center gap-2 text-sm font-medium text-slate-400 hover:text-indigo-600 transition-colors mt-2">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
        Add task
      </button>
    </div>

  </div>
</template>
