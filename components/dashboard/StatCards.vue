<template>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
    
    <!-- Total Tasks -->
    <div class="bg-white rounded-2xl p-4 border border-slate-200 flex items-center gap-3 shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-purple-50 flex items-center justify-center flex-shrink-0 border border-purple-100">
        <svg class="w-5 h-5 text-purple-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
      </div>
      <div class="min-w-0 flex-1">
        <p class="text-xs font-semibold text-slate-500 mb-1 truncate">Total Tasks</p>
        <p class="text-xl font-bold text-slate-900 leading-none">42</p>
        <p class="text-[10px] font-medium text-emerald-600 mt-2 flex items-center gap-1 whitespace-nowrap">
          <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
          8% vs last week
        </p>
      </div>
    </div>

    <!-- Scheduled Today -->
    <div class="bg-white rounded-2xl p-4 border border-slate-200 flex items-center gap-3 shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-blue-50 flex items-center justify-center flex-shrink-0 border border-blue-100">
        <svg class="w-5 h-5 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
      </div>
      <div class="min-w-0 flex-1">
        <p class="text-xs font-semibold text-slate-500 mb-1 truncate">Scheduled Today</p>
        <p class="text-xl font-bold text-slate-900 leading-none">6</p>
        <p class="text-[10px] font-medium text-red-500 mt-2 flex items-center gap-1 whitespace-nowrap">
          2 high priority
        </p>
      </div>
    </div>

    <!-- Focus Score -->
    <div class="bg-white rounded-2xl p-4 border border-slate-200 flex items-center gap-3 shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-fuchsia-50 flex items-center justify-center flex-shrink-0 border border-fuchsia-100">
        <svg class="w-5 h-5 text-fuchsia-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path></svg>
      </div>
      <div class="min-w-0 flex-1">
        <p class="text-xs font-semibold text-slate-500 mb-1 truncate">Focus Score</p>
        <p class="text-xl font-bold text-slate-900 leading-none">87</p>
        <p class="text-[10px] font-medium text-emerald-600 mt-2 flex items-center gap-1 whitespace-nowrap">
          <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
          12 pts vs yesterday
        </p>
      </div>
    </div>

    <!-- Completion Rate -->
    <div class="bg-white rounded-2xl p-4 border border-slate-200 flex items-center gap-3 shadow-sm">
      <div class="w-10 h-10 relative flex items-center justify-center flex-shrink-0">
        <svg class="w-full h-full transform -rotate-90" viewBox="0 0 36 36">
          <path class="text-slate-100" stroke-width="3" stroke="currentColor" fill="none" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" />
          <path class="text-emerald-500" stroke-width="3" stroke-dasharray="72, 100" stroke-linecap="round" stroke="currentColor" fill="none" d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" />
        </svg>
        <span class="absolute text-[10px] font-bold text-emerald-600">72%</span>
      </div>
      <div class="min-w-0 flex-1">
        <p class="text-xs font-semibold text-slate-500 mb-1 truncate">Completion Rate</p>
        <p class="text-xl font-bold text-slate-900 leading-none">72%</p>
        <p class="text-[10px] font-medium text-emerald-600 mt-2 flex items-center gap-1 whitespace-nowrap">
          <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
          9% vs last week
        </p>
      </div>
    </div>

  </div>
</template>
