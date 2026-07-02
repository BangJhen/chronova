<template>
  <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm flex flex-col">
    <h3 class="font-bold text-slate-900 mb-6">Recent Activity</h3>
    
    <div class="flex-1 space-y-5">
      
      <!-- Activity 1 -->
      <div class="flex items-start gap-3">
        <div class="w-6 h-6 rounded-full bg-emerald-100 flex items-center justify-center flex-shrink-0 text-emerald-600 mt-0.5">
          <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
        </div>
        <div class="flex-1">
          <p class="text-sm text-slate-700 leading-snug"><span class="font-semibold text-slate-900">Aisyah Khan</span> completed <span class="font-semibold text-indigo-600">UI/UX Design System</span></p>
        </div>
        <span class="text-[11px] text-slate-400 font-medium whitespace-nowrap">2h ago</span>
      </div>

      <!-- Activity 2 -->
      <div class="flex items-start gap-3">
        <div class="w-6 h-6 rounded-full bg-blue-100 flex items-center justify-center flex-shrink-0 text-blue-600 mt-0.5">
          <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>
        </div>
        <div class="flex-1">
          <p class="text-sm text-slate-700 leading-snug"><span class="font-semibold text-slate-900">Daniel Sutanto</span> commented on <span class="font-semibold text-indigo-600">API Integrations</span></p>
        </div>
        <span class="text-[11px] text-slate-400 font-medium whitespace-nowrap">3h ago</span>
      </div>

      <!-- Activity 3 -->
      <div class="flex items-start gap-3">
        <div class="w-6 h-6 rounded-full bg-indigo-100 flex items-center justify-center flex-shrink-0 text-indigo-600 mt-0.5">
          <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4"></path></svg>
        </div>
        <div class="flex-1">
          <p class="text-sm text-slate-700 leading-snug">You moved <span class="font-semibold text-indigo-600">Performance optimization</span> to <span class="font-semibold text-slate-900">In Progress</span></p>
        </div>
        <span class="text-[11px] text-slate-400 font-medium whitespace-nowrap">5h ago</span>
      </div>

      <!-- Activity 4 -->
      <div class="flex items-start gap-3">
        <div class="w-6 h-6 rounded-full bg-emerald-100 flex items-center justify-center flex-shrink-0 text-emerald-600 mt-0.5">
          <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
        </div>
        <div class="flex-1">
          <p class="text-sm text-slate-700 leading-snug"><span class="font-semibold text-indigo-600">Project kickoff</span> marked as done</p>
        </div>
        <span class="text-[11px] text-slate-400 font-medium whitespace-nowrap">1d ago</span>
      </div>

    </div>
    
    <button class="flex items-center gap-1.5 text-xs font-semibold text-slate-500 hover:text-indigo-600 transition-colors mt-6">
      View all activity
      <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
    </button>
  </div>
</template>
