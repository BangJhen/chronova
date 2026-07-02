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
        <li><NuxtLink :to="{ path: '/', hash: '#how-it-works' }" class="hover:text-blue-600 transition-colors">How It Works</NuxtLink></li>
        <li><NuxtLink :to="{ path: '/', hash: '#features' }" class="hover:text-blue-600 transition-colors">Features</NuxtLink></li>
        <li><NuxtLink :to="{ path: '/', hash: '#pricing' }" class="hover:text-blue-600 transition-colors">Pricing</NuxtLink></li>
        <li><NuxtLink :to="{ path: '/', hash: '#faq' }" class="hover:text-blue-600 transition-colors">FAQ</NuxtLink></li>
      </ul>

      <!-- Actions Section -->
      <div class="flex items-center gap-3">
        <NuxtLink to="/login" class="px-5 py-2.5 text-[0.85rem] font-bold text-slate-700 bg-white border border-slate-200 rounded-xl hover:bg-slate-50 hover:border-slate-300 hover:shadow-sm transition-all text-center">
          Sign In
        </NuxtLink>
        <NuxtLink to="/register" class="px-6 py-2.5 text-[0.85rem] font-bold text-white rounded-xl bg-gradient-to-r from-[#2dd4bf] via-[#3b82f6] to-[#a855f7] hover:opacity-90 hover:shadow-[0_4px_20px_rgba(59,130,246,0.4)] hover:-translate-y-0.5 transition-all duration-300 text-center">
          Get Started
        </NuxtLink>
      </div>

    </nav>
  </div>
</template>
