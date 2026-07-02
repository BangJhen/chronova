<template>
  <div class="min-h-screen bg-[#f8f9fc] flex items-center justify-center p-4 font-sans relative">
    
    <!-- Return to Home Button -->
    <NuxtLink to="/" class="absolute top-6 left-6 md:top-10 md:left-10 flex items-center gap-2 text-sm font-semibold text-slate-500 hover:text-indigo-600 transition-colors bg-white/50 hover:bg-white px-4 py-2 rounded-full border border-slate-200 shadow-sm backdrop-blur-sm z-50">
      <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M10 19l-7-7m0 0l7-7m-7 7h18"></path></svg>
      Return to Home
    </NuxtLink>

    <div class="max-w-md w-full bg-white rounded-3xl shadow-xl shadow-indigo-100/50 p-8 border border-slate-100 relative overflow-hidden">
      <!-- Glow effect -->
      <div class="absolute -top-24 -left-24 w-48 h-48 bg-purple-500/10 blur-[50px] rounded-full pointer-events-none"></div>

      <div class="text-center mb-8 relative z-10">
        <h1 class="text-2xl font-bold text-slate-900 mb-2 tracking-tight">Create an account</h1>
        <p class="text-sm text-slate-500">Start your 14-day free trial. No credit card required.</p>
      </div>
      
      <!-- Placeholder Form -->
      <div class="space-y-5 relative z-10">
        <div>
          <label class="block text-sm font-medium text-slate-700 mb-1.5">Full Name</label>
          <input type="text" class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 transition-all text-sm" placeholder="John Doe" />
        </div>
        <div>
          <label class="block text-sm font-medium text-slate-700 mb-1.5">Email</label>
          <input type="email" class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 transition-all text-sm" placeholder="you@example.com" />
        </div>
        <div>
          <label class="block text-sm font-medium text-slate-700 mb-1.5">Password</label>
          <input type="password" class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 transition-all text-sm" placeholder="Create a strong password" />
        </div>
        
        <button class="w-full py-3 px-4 bg-gradient-to-r from-[#2dd4bf] via-[#3b82f6] to-[#a855f7] hover:opacity-90 text-white text-sm font-bold rounded-xl shadow-[0_4px_14px_rgba(59,130,246,0.3)] hover:shadow-[0_6px_20px_rgba(59,130,246,0.4)] hover:-translate-y-0.5 transition-all">
          Get Started
        </button>
      </div>
      
      <p class="text-center text-sm text-slate-500 mt-8 relative z-10">
        Already have an account? 
        <NuxtLink to="/login" class="text-indigo-600 font-semibold hover:underline">Sign in</NuxtLink>
      </p>
    </div>
  </div>
</template>
