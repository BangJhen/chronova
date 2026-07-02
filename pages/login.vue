<template>
  <div class="min-h-screen bg-[#f8f9fc] flex items-center justify-center p-4 font-sans">
    <div class="max-w-md w-full bg-white rounded-3xl shadow-xl shadow-indigo-100/50 p-8 border border-slate-100 relative overflow-hidden">
      <!-- Glow effect -->
      <div class="absolute -top-24 -right-24 w-48 h-48 bg-indigo-500/10 blur-[50px] rounded-full pointer-events-none"></div>

      <div class="text-center mb-8 relative z-10">
        <NuxtLink to="/" class="inline-block mb-4">
          <img src="/logo.png" alt="Chronova Logo" class="h-10 w-auto mx-auto drop-shadow-sm" />
        </NuxtLink>
        <h1 class="text-2xl font-bold text-slate-900 mb-2 tracking-tight">Welcome back</h1>
        <p class="text-sm text-slate-500">Enter your details to sign in to your account</p>
      </div>
      
      <!-- Placeholder Form -->
      <div class="space-y-5 relative z-10">
        <div>
          <label class="block text-sm font-medium text-slate-700 mb-1.5">Email</label>
          <input type="email" class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 transition-all text-sm" placeholder="you@example.com" />
        </div>
        <div>
          <div class="flex items-center justify-between mb-1.5">
            <label class="block text-sm font-medium text-slate-700">Password</label>
            <a href="#" class="text-xs font-semibold text-indigo-600 hover:text-indigo-700">Forgot password?</a>
          </div>
          <input type="password" class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-indigo-500/20 focus:border-indigo-500 transition-all text-sm" placeholder="••••••••" />
        </div>
        
        <button class="w-full py-3 px-4 bg-indigo-600 hover:bg-indigo-700 text-white text-sm font-bold rounded-xl shadow-[0_4px_14px_rgba(79,70,229,0.3)] hover:shadow-[0_6px_20px_rgba(79,70,229,0.4)] hover:-translate-y-0.5 transition-all">
          Sign In
        </button>
      </div>
      
      <p class="text-center text-sm text-slate-500 mt-8 relative z-10">
        Don't have an account? 
        <NuxtLink to="/register" class="text-indigo-600 font-semibold hover:underline">Get started</NuxtLink>
      </p>
    </div>
  </div>
</template>
