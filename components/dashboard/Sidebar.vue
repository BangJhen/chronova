<template>
  <aside class="w-[280px] h-screen bg-[#fcfdff] border-r border-slate-200 flex flex-col fixed left-0 top-0 font-sans z-40">
    <!-- Logo -->
    <div class="h-20 flex items-center px-6">
      <NuxtLink to="/">
        <img src="/logo.png" alt="Chronova" class="h-6 w-auto" />
      </NuxtLink>
    </div>

    <div class="flex-1 overflow-y-auto px-4 py-4 space-y-8 no-scrollbar">
      <!-- Main Nav -->
      <div>
        <ul class="space-y-1">
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 bg-indigo-50 text-indigo-700 rounded-xl font-semibold text-sm">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
              Dashboard
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"></path></svg>
              Projects
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path></svg>
              Tasks
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
              Calendar
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6V4m0 2a2 2 0 100 4m0-4a2 2 0 110 4m-6 8a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4m6 6v10m6-2a2 2 0 100-4m0 4a2 2 0 110-4m0 4v2m0-6V4"></path></svg>
              Focus
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
              Analytics
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path></svg>
              AI Copilot
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2.5 text-slate-500 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
              Settings
            </a>
          </li>
        </ul>
      </div>

      <!-- Favorites -->
      <div>
        <h3 class="px-3 text-xs font-bold text-slate-400 uppercase tracking-wider mb-2">Favorites</h3>
        <ul class="space-y-1">
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2 text-slate-600 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <span class="w-2 h-2 rounded-full bg-purple-500"></span>
              Website Redesign
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2 text-slate-600 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <span class="w-2 h-2 rounded-full bg-blue-500"></span>
              Mobile App Launch
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2 text-slate-600 hover:text-slate-900 hover:bg-slate-50 rounded-xl font-medium text-sm transition-colors">
              <span class="w-2 h-2 rounded-full bg-emerald-500"></span>
              Marketing Campaign
            </a>
          </li>
          <li>
            <a href="#" class="flex items-center gap-3 px-3 py-2 text-slate-400 hover:text-indigo-600 hover:bg-indigo-50 rounded-xl font-medium text-sm transition-colors mt-2">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
              Add Favorite
            </a>
          </li>
        </ul>
      </div>
    </div>

    <!-- Bottom Team Selector -->
    <div class="p-4 border-t border-slate-200">
      <button class="w-full flex items-center justify-between p-2 rounded-xl hover:bg-slate-50 transition-colors">
        <div class="flex items-center gap-3">
          <div class="w-8 h-8 rounded-lg bg-slate-100 flex items-center justify-center border border-slate-200">
            <svg class="w-4 h-4 text-slate-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"></path></svg>
          </div>
          <div class="text-left">
            <p class="text-sm font-bold text-slate-900">Chronova Team</p>
            <p class="text-xs text-slate-500">Enterprise Plan</p>
          </div>
        </div>
        <svg class="w-4 h-4 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
      </button>
    </div>
  </aside>
</template>
