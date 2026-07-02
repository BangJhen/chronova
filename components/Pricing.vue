<template>
  <section class="relative w-full py-24 bg-[#EEEFFB] overflow-hidden font-sans">
    <!-- Background subtle glows -->
    <div class="absolute top-0 left-1/2 -translate-x-1/2 w-full max-w-4xl h-[500px] bg-indigo-500/5 blur-[120px] rounded-full pointer-events-none"></div>

    <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Header -->
      <div class="flex flex-col items-center text-center mb-16">
        <div class="inline-flex items-center px-4 py-1.5 rounded-full border border-indigo-100 bg-white mb-6 shadow-sm">
          <span class="text-xs font-bold tracking-wider text-indigo-600 uppercase">Pricing</span>
        </div>
        <h2 class="text-4xl md:text-5xl font-bold text-slate-900 tracking-tight mb-4">
          Simple, transparent pricing
        </h2>
        <p class="text-lg text-slate-500 max-w-xl mx-auto leading-relaxed">
          Choose the plan that fits your workflow.<br/>Upgrade or downgrade anytime.
        </p>

        <!-- Toggle -->
        <div class="mt-10 flex items-center gap-4 bg-transparent">
          <span :class="['text-sm font-semibold transition-colors', !isYearly ? 'text-slate-800' : 'text-slate-400']">Monthly</span>
          
          <button 
            @click="isYearly = !isYearly"
            class="relative inline-flex h-7 w-14 items-center rounded-full bg-indigo-500 transition-colors focus:outline-none shadow-inner"
          >
            <span 
              :class="['inline-block h-5 w-5 transform rounded-full bg-white transition-transform shadow-sm', isYearly ? 'translate-x-8' : 'translate-x-1']"
            ></span>
          </button>
          
          <div class="flex items-center gap-2">
            <span :class="['text-sm font-semibold transition-colors', isYearly ? 'text-slate-800' : 'text-slate-400']">Yearly</span>
            <span class="px-2.5 py-1 rounded-full bg-indigo-50 text-[10px] font-bold text-indigo-600 border border-indigo-100 uppercase tracking-wider">Save 20%</span>
          </div>
        </div>
      </div>

      <!-- Pricing Cards -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 lg:gap-8 items-stretch">
        
        <!-- Starter Card -->
        <div class="bg-white/70 backdrop-blur-xl rounded-[2.5rem] p-8 border border-white shadow-[0_8px_30px_rgba(0,0,0,0.04)] flex flex-col hover:shadow-[0_20px_40px_rgba(0,0,0,0.08)] transition-all duration-300">
          <div class="w-12 h-12 rounded-2xl bg-blue-50 flex items-center justify-center mb-6 border border-blue-100/50">
            <svg class="w-6 h-6 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/>
            </svg>
          </div>
          <h3 class="text-2xl font-bold text-slate-800 mb-2">Starter</h3>
          <p class="text-sm text-slate-500 h-10">For individuals getting started</p>
          
          <div class="mt-4 mb-2 flex items-baseline gap-1">
            <span class="text-6xl font-extrabold text-slate-900 tracking-tight">$0</span>
          </div>
          <p class="text-xs text-slate-500 mb-8 font-medium">Forever free</p>
          
          <div class="w-full h-px bg-slate-100 mb-8"></div>
          
          <ul class="flex flex-col gap-4 mb-8 flex-grow">
            <li v-for="feature in ['Up to 3 projects', 'AI task suggestions', 'Basic integrations', 'Community support']" :key="feature" class="flex items-center gap-3">
              <svg class="w-4 h-4 text-blue-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 13l4 4L19 7"/>
              </svg>
              <span class="text-sm text-slate-700 font-medium">{{ feature }}</span>
            </li>
          </ul>
          
          <button class="w-full py-3.5 rounded-xl border border-blue-200 bg-white text-blue-600 font-bold hover:bg-blue-50 hover:border-blue-300 transition-all shadow-sm mt-auto">
            Get Started
          </button>
        </div>

        <!-- Pro Card -->
        <div class="bg-white/90 backdrop-blur-xl rounded-[2.5rem] p-8 border border-white shadow-[0_20px_40px_rgba(99,102,241,0.1)] relative flex flex-col transform md:-translate-y-4 hover:shadow-[0_30px_60px_rgba(99,102,241,0.15)] transition-all duration-300 ring-4 ring-indigo-50/50">
          <div class="absolute top-6 right-6 bg-indigo-100 text-indigo-700 text-[10px] font-bold px-3 py-1.5 rounded-full flex items-center gap-1.5">
            <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/></svg>
            Most Popular
          </div>
          
          <div class="w-12 h-12 rounded-2xl bg-purple-50 flex items-center justify-center mb-6 border border-purple-100/50">
            <svg class="w-6 h-6 text-purple-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"/>
            </svg>
          </div>
          <h3 class="text-2xl font-bold text-slate-800 mb-2">Pro</h3>
          <p class="text-sm text-slate-500 h-10">For professionals and small teams</p>
          
          <div class="mt-4 mb-2 flex items-baseline gap-1">
            <span class="text-6xl font-extrabold text-slate-900 tracking-tight">${{ isYearly ? '9' : '12' }}</span>
            <span class="text-sm font-semibold text-slate-400">/ user / month</span>
          </div>
          <p class="text-xs text-slate-500 mb-8 font-medium">Billed {{ isYearly ? 'annually' : 'monthly' }}</p>
          
          <div class="w-full h-px bg-slate-100 mb-8"></div>
          
          <ul class="flex flex-col gap-4 mb-8 flex-grow">
            <li v-for="feature in ['Unlimited projects', 'Advanced AI planning', 'Priority integrations', 'Team collaboration', 'Priority support']" :key="feature" class="flex items-center gap-3">
              <svg class="w-4 h-4 text-purple-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 13l4 4L19 7"/>
              </svg>
              <span class="text-sm text-slate-700 font-medium">{{ feature }}</span>
            </li>
          </ul>
          
          <button class="w-full py-3.5 rounded-xl bg-gradient-to-r from-indigo-500 to-purple-500 text-white font-bold hover:shadow-[0_8px_20px_rgba(99,102,241,0.3)] transition-all duration-300 hover:-translate-y-0.5 mt-auto">
            Start Free Trial
          </button>
          <p class="text-[10px] text-center text-slate-400 mt-4 font-medium">14-day free trial · No credit card required</p>
        </div>

        <!-- Business Card -->
        <div class="bg-white/70 backdrop-blur-xl rounded-[2.5rem] p-8 border border-white shadow-[0_8px_30px_rgba(0,0,0,0.04)] flex flex-col hover:shadow-[0_20px_40px_rgba(0,0,0,0.08)] transition-all duration-300">
          <div class="w-12 h-12 rounded-2xl bg-blue-50 flex items-center justify-center mb-6 border border-blue-100/50">
            <svg class="w-6 h-6 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 21h18M5 21V7l5 4 2-6 2 6 5-4v14" />
            </svg>
          </div>
          <h3 class="text-2xl font-bold text-slate-800 mb-2">Business</h3>
          <p class="text-sm text-slate-500 h-10">For growing teams and organizations</p>
          
          <div class="mt-4 mb-2 flex items-baseline gap-1">
            <span class="text-6xl font-extrabold text-slate-900 tracking-tight">${{ isYearly ? '19' : '24' }}</span>
            <span class="text-sm font-semibold text-slate-400">/ user / month</span>
          </div>
          <p class="text-xs text-slate-500 mb-8 font-medium">Billed {{ isYearly ? 'annually' : 'monthly' }}</p>
          
          <div class="w-full h-px bg-slate-100 mb-8"></div>
          
          <ul class="flex flex-col gap-4 mb-8 flex-grow">
            <li v-for="feature in ['Everything in Pro', 'Advanced analytics', 'Custom roles & permissions', 'SLA & dedicated support', 'SSO & enterprise integrations']" :key="feature" class="flex items-center gap-3">
              <svg class="w-4 h-4 text-blue-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 13l4 4L19 7"/>
              </svg>
              <span class="text-sm text-slate-700 font-medium">{{ feature }}</span>
            </li>
          </ul>
          
          <button class="w-full py-3.5 rounded-xl border border-blue-200 bg-white text-blue-600 font-bold hover:bg-blue-50 hover:border-blue-300 transition-all shadow-sm mt-auto">
            Contact Sales
          </button>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const isYearly = ref(false)
</script>
