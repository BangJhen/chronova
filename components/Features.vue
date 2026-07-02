<template>
  <section class="relative w-full overflow-hidden flex items-center justify-center bg-slate-900">
    <!-- Image dictates the dimensions. w-full ensures it stretches, and h-auto keeps aspect ratio -->
    <img 
      src="/features-background.png" 
      alt="Features Background" 
      class="w-full h-auto min-h-[700px] md:min-h-0 object-cover md:object-contain block" 
    />
    
    <!-- Content overlaid exactly on top -->
    <div class="absolute inset-0 z-10 flex flex-col justify-center items-center p-6 md:p-12 lg:p-24 w-full h-full">
      <div class="text-center mb-10 lg:mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-indigo-300/30 bg-white/10 backdrop-blur-md mb-6 shadow-sm">
          <svg class="w-4 h-4 text-indigo-300" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
          </svg>
          <span class="text-xs font-semibold tracking-wider text-indigo-100 uppercase">Features</span>
        </div>
        <h2 class="text-3xl md:text-5xl font-semibold text-white tracking-tight mb-4">
          Everything you need to ship faster
        </h2>
        <p class="text-indigo-100/80 text-lg max-w-2xl mx-auto">
          Chronova comes packed with all the tools necessary to manage tasks, collaborate, and track progress effortlessly.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 lg:gap-8 w-full max-w-6xl mx-auto">
        <!-- Feature 1 -->
        <div class="bg-white/5 hover:bg-white/10 transition-colors backdrop-blur-md rounded-2xl p-6 md:p-8 border border-white/10 shadow-xl">
          <div class="w-12 h-12 rounded-xl bg-indigo-500/20 flex items-center justify-center mb-5 text-indigo-300">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-2">Lightning Fast</h3>
          <p class="text-indigo-100/70 text-sm leading-relaxed">Experience seamless navigation and instant updates across your entire workspace.</p>
        </div>
        
        <!-- Feature 2 -->
        <div class="bg-white/5 hover:bg-white/10 transition-colors backdrop-blur-md rounded-2xl p-6 md:p-8 border border-white/10 shadow-xl">
          <div class="w-12 h-12 rounded-xl bg-purple-500/20 flex items-center justify-center mb-5 text-purple-300">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path></svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-2">Bank-grade Security</h3>
          <p class="text-indigo-100/70 text-sm leading-relaxed">Your data is encrypted at rest and in transit, ensuring maximum privacy.</p>
        </div>
        
        <!-- Feature 3 -->
        <div class="bg-white/5 hover:bg-white/10 transition-colors backdrop-blur-md rounded-2xl p-6 md:p-8 border border-white/10 shadow-xl">
          <div class="w-12 h-12 rounded-xl bg-blue-500/20 flex items-center justify-center mb-5 text-blue-300">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path></svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-2">Advanced Analytics</h3>
          <p class="text-indigo-100/70 text-sm leading-relaxed">Gain deep insights into team performance and project bottlenecks.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
