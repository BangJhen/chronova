<template>
  <div class="fixed top-6 left-0 right-0 z-50 flex justify-center px-4 w-full">
    <!-- Navbar Container -->
    <nav class="bg-white/75 backdrop-blur-md rounded-full shadow-[0_12px_40px_rgba(100,120,255,0.15)] border border-white/50 flex items-center justify-between px-6 py-2.5 w-full max-w-[1100px]">
      
      <!-- Logo Section -->
      <a href="/" class="flex items-center gap-2">
        <!-- Image Logo -->
        <div class="h-6 relative flex items-center justify-center">
          <img src="/logo.png" alt="Chronova" class="h-full w-auto object-contain drop-shadow-md" />
        </div>
      </a>

      <!-- Links Section -->
      <ul class="hidden md:flex items-center gap-8 text-[0.85rem] font-semibold text-[#334155]">
        <li><a href="#" class="hover:text-blue-600 transition-colors">Features</a></li>
        <li><a href="#" class="hover:text-blue-600 transition-colors">AI Copilot</a></li>
        <li><a href="#" class="hover:text-blue-600 transition-colors">Pricing</a></li>
        <li><a href="#" class="hover:text-blue-600 transition-colors">Templates</a></li>
        
        <!-- Dropdown Resource -->
        <li class="relative group py-4 -my-4 cursor-pointer">
          <a class="flex items-center gap-1 hover:text-blue-600 transition-colors">
            Resources
            <svg class="w-3.5 h-3.5 mt-0.5 text-slate-400 group-hover:text-blue-600 transition-transform duration-300 group-hover:rotate-180" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M19 9l-7 7-7-7"></path></svg>
          </a>
          <!-- Dropdown Menu -->
          <div class="absolute top-full right-1/2 translate-x-1/2 mt-2 w-48 bg-white/95 backdrop-blur-md rounded-2xl shadow-[0_10px_40px_rgba(0,0,0,0.1)] border border-slate-100 opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all duration-300 transform translate-y-3 group-hover:translate-y-0">
            <div class="p-2 space-y-1">
              <a href="#" class="block px-4 py-2.5 text-sm font-medium text-slate-600 hover:bg-blue-50 hover:text-blue-600 rounded-xl transition-colors">Documentation</a>
              <a href="#" class="block px-4 py-2.5 text-sm font-medium text-slate-600 hover:bg-blue-50 hover:text-blue-600 rounded-xl transition-colors">Blog & News</a>
              <a href="#" class="block px-4 py-2.5 text-sm font-medium text-slate-600 hover:bg-blue-50 hover:text-blue-600 rounded-xl transition-colors">Community</a>
            </div>
          </div>
        </li>
      </ul>

      <!-- Actions Section -->
      <div class="flex items-center gap-3">
        <button class="px-5 py-2.5 text-[0.85rem] font-bold text-slate-700 bg-white border border-slate-200 rounded-xl hover:bg-slate-50 hover:border-slate-300 hover:shadow-sm transition-all">
          Sign In
        </button>
        <button class="px-6 py-2.5 text-[0.85rem] font-bold text-white rounded-xl bg-gradient-to-r from-[#2dd4bf] via-[#3b82f6] to-[#a855f7] hover:opacity-90 hover:shadow-[0_4px_20px_rgba(59,130,246,0.4)] hover:-translate-y-0.5 transition-all duration-300">
          Get Started
        </button>
      </div>

    </nav>
  </div>
</template>
