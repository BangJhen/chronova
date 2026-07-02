<template>
  <div class="min-h-screen bg-[#fafafc] text-slate-900 font-sans relative">
    <!-- Background glows (Wrapped in an isolated overflow-hidden container to prevent horizontal scroll without breaking sticky positioning) -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none z-0">
      <div class="absolute top-0 left-1/2 -translate-x-1/2 w-[800px] h-[600px] bg-fuchsia-100/50 rounded-full blur-[100px] opacity-70"></div>
      <div class="absolute top-40 -left-40 w-[500px] h-[500px] bg-blue-100/50 rounded-full blur-[100px] opacity-60"></div>
      <div class="absolute top-40 -right-40 w-[500px] h-[500px] bg-purple-100/50 rounded-full blur-[100px] opacity-60"></div>
    </div>
    
    <Navbar />
    
    <main class="relative z-10">
      <slot />
    </main>
  </div>
</template>
