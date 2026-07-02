<template>
  <div class="flex flex-col gap-6 h-full">
    
    <!-- Today's Schedule -->
    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm">
      <div class="flex items-center justify-between mb-6">
        <h3 class="font-bold text-slate-900 flex items-center gap-2">
          <svg class="w-5 h-5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
          Today's Schedule
        </h3>
        <div class="flex items-center gap-2 text-xs font-semibold text-slate-500">
          <button class="hover:text-slate-900"><svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path></svg></button>
          May 15, 2025
          <button class="hover:text-slate-900"><svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg></button>
        </div>
      </div>

      <div class="space-y-6 relative before:absolute before:inset-0 before:ml-[50px] before:-translate-x-px md:before:mx-auto md:before:translate-x-0 before:h-full before:w-0.5 before:bg-gradient-to-b before:from-transparent before:via-slate-200 before:to-transparent">
        
        <!-- Timeline Item 1 -->
        <div class="relative flex items-center justify-between">
          <div class="flex items-center gap-4 z-10 w-full">
            <div class="text-xs font-bold text-slate-500 w-16 text-right">09:00 AM</div>
            <div class="w-3 h-3 rounded-full border-2 border-emerald-500 bg-white ring-4 ring-white"></div>
            <div class="flex-1">
              <p class="text-sm font-semibold text-slate-900">Daily Standup</p>
            </div>
            <div class="text-[10px] font-bold text-blue-500 bg-blue-50 px-2 py-0.5 rounded">30m</div>
          </div>
        </div>

        <!-- Timeline Item 2 -->
        <div class="relative flex items-center justify-between">
          <div class="flex items-center gap-4 z-10 w-full">
            <div class="text-xs font-bold text-slate-500 w-16 text-right">10:00 AM</div>
            <div class="w-3 h-3 rounded-full border-2 border-fuchsia-500 bg-white ring-4 ring-white"></div>
            <div class="flex-1">
              <p class="text-sm font-semibold text-slate-900">UI Review</p>
            </div>
            <div class="text-[10px] font-bold text-fuchsia-500 bg-fuchsia-50 px-2 py-0.5 rounded">60m</div>
          </div>
        </div>

        <!-- Timeline Item 3 -->
        <div class="relative flex items-center justify-between">
          <div class="flex items-center gap-4 z-10 w-full">
            <div class="text-xs font-bold text-slate-500 w-16 text-right">01:00 PM</div>
            <div class="w-3 h-3 rounded-full border-2 border-indigo-500 bg-white ring-4 ring-white"></div>
            <div class="flex-1">
              <p class="text-sm font-semibold text-slate-900">Deep Work Block</p>
            </div>
            <div class="text-[10px] font-bold text-indigo-500 bg-indigo-50 px-2 py-0.5 rounded">2h</div>
          </div>
        </div>

        <!-- Timeline Item 4 -->
        <div class="relative flex items-center justify-between">
          <div class="flex items-center gap-4 z-10 w-full">
            <div class="text-xs font-bold text-slate-500 w-16 text-right">03:30 PM</div>
            <div class="w-3 h-3 rounded-full border-2 border-blue-500 bg-white ring-4 ring-white"></div>
            <div class="flex-1">
              <p class="text-sm font-semibold text-slate-900">Stakeholder Update</p>
            </div>
            <div class="text-[10px] font-bold text-blue-500 bg-blue-50 px-2 py-0.5 rounded">30m</div>
          </div>
        </div>

        <!-- Timeline Item 5 -->
        <div class="relative flex items-center justify-between">
          <div class="flex items-center gap-4 z-10 w-full">
            <div class="text-xs font-bold text-slate-500 w-16 text-right">04:30 PM</div>
            <div class="w-3 h-3 rounded-full border-2 border-red-500 bg-white ring-4 ring-white"></div>
            <div class="flex-1">
              <p class="text-sm font-semibold text-slate-900">Design Sync</p>
            </div>
            <div class="text-[10px] font-bold text-red-500 bg-red-50 px-2 py-0.5 rounded">45m</div>
          </div>
        </div>

      </div>
      
      <button class="flex items-center gap-1.5 text-xs font-semibold text-slate-500 hover:text-indigo-600 transition-colors mt-8">
        View full calendar
        <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
      </button>
    </div>

    <!-- AI Copilot -->
    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm">
      <div class="flex items-center gap-2 mb-4">
        <svg class="w-5 h-5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path></svg>
        <h3 class="font-bold text-slate-900">AI Copilot</h3>
        <span class="px-2 py-0.5 rounded bg-indigo-50 text-[9px] font-bold text-indigo-600 border border-indigo-100 uppercase tracking-wider">BETA</span>
      </div>

      <div class="space-y-2 mb-4">
        <button class="w-full flex items-center justify-between p-3 rounded-xl border border-slate-200 hover:border-indigo-300 hover:bg-indigo-50/50 transition-colors group">
          <div class="flex items-center gap-2 text-sm text-slate-600 group-hover:text-indigo-700">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            What should I focus on today?
          </div>
          <svg class="w-4 h-4 text-slate-300 group-hover:text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
        </button>

        <button class="w-full flex items-center justify-between p-3 rounded-xl border border-slate-200 hover:border-indigo-300 hover:bg-indigo-50/50 transition-colors group">
          <div class="flex items-center gap-2 text-sm text-slate-600 group-hover:text-indigo-700">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 10l-2 1m0 0l-2-1m2 1v2.5M20 7l-2 1m2-1l-2-1m2 1v2.5M14 4l-2-1-2 1M4 7l2-1M4 7l2 1M4 7v2.5M12 21l-2-1m2 1l2-1m-2 1v-2.5M6 18l-2-1v-2.5M18 18l2-1v-2.5"></path></svg>
            Break this project into tasks
          </div>
          <svg class="w-4 h-4 text-slate-300 group-hover:text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
        </button>

        <button class="w-full flex items-center justify-between p-3 rounded-xl border border-slate-200 hover:border-indigo-300 hover:bg-indigo-50/50 transition-colors group">
          <div class="flex items-center gap-2 text-sm text-slate-600 group-hover:text-indigo-700">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
            Schedule deep work block
          </div>
          <svg class="w-4 h-4 text-slate-300 group-hover:text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
        </button>

        <button class="w-full flex items-center justify-between p-3 rounded-xl border border-slate-200 hover:border-indigo-300 hover:bg-indigo-50/50 transition-colors group">
          <div class="flex items-center gap-2 text-sm text-slate-600 group-hover:text-indigo-700">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path></svg>
            Summarize project status
          </div>
          <svg class="w-4 h-4 text-slate-300 group-hover:text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
        </button>
      </div>

      <div class="relative">
        <input type="text" placeholder="Ask AI anything..." class="w-full py-3 pl-4 pr-12 bg-white border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 shadow-sm" />
        <button class="absolute right-2 top-1.5 p-1.5 bg-indigo-600 hover:bg-indigo-700 text-white rounded-lg transition-colors">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path></svg>
        </button>
      </div>
    </div>

    <!-- Focus Timer -->
    <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm flex flex-col flex-1">
      <h3 class="font-bold text-slate-900 mb-6">Focus Timer</h3>
      
      <div class="flex justify-center mb-6">
        <div class="relative w-32 h-32 flex items-center justify-center">
          <svg class="w-full h-full transform -rotate-90" viewBox="0 0 36 36">
            <path class="text-indigo-50" stroke-width="3" stroke="currentColor" fill="none" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" />
            <path class="text-indigo-500" stroke-width="3" stroke-dasharray="100, 100" stroke-linecap="round" stroke="currentColor" fill="none" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" />
          </svg>
          <div class="absolute text-center">
            <span class="block text-3xl font-bold text-slate-900 leading-none">45:00</span>
            <span class="text-[10px] font-semibold text-slate-400 uppercase tracking-widest mt-1">Deep Work</span>
          </div>
        </div>
      </div>

      <button class="w-full py-3 bg-indigo-600 hover:bg-indigo-700 text-white rounded-xl text-sm font-bold shadow-md shadow-indigo-200 transition-colors flex items-center justify-center gap-2">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        Start Focus Session
      </button>
    </div>

  </div>
</template>
