<template>
  <div>
    <!-- Hero Section -->
    <section class="relative w-full min-h-screen bg-[#fafafc] flex flex-col justify-center items-center text-center px-4 pt-32 pb-20">
      
      <!-- Background Video -->
      <div class="absolute inset-0 z-0 pointer-events-none">
        <div class="sticky -top-[20vh] w-full h-[120vh] flex justify-center items-center">
          <video
            class="w-full h-full object-cover opacity-90 mix-blend-multiply"
            src="/hero-background-video.mp4"
            autoplay
            loop
            muted
            playsinline
          ></video>
        </div>
      </div>
      
      <!-- Overlay to ensure text readability if needed -->
      <div class="absolute inset-0 bg-white/20 z-0 pointer-events-none"></div>

      <!-- Hero Content (Scrolls normally) -->
      <div class="relative z-10 w-full max-w-5xl mx-auto flex flex-col items-center mt-12">
        <!-- Top Badge -->
        <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-white/60 backdrop-blur-sm border border-purple-100 shadow-[0_4px_20px_rgba(168,85,247,0.08)] mb-8">
          <svg class="w-4 h-4 text-indigo-500" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2L14.4 9.6L22 12L14.4 14.4L12 22L9.6 14.4L2 12L9.6 9.6L12 2Z" />
          </svg>
          <span class="text-sm font-medium bg-clip-text text-transparent bg-gradient-to-r from-indigo-500 to-purple-600">
            AI-Powered Kanban Scheduler
          </span>
        </div>

        <!-- Headline -->
        <h1 class="text-[2.5rem] md:text-[3.75rem] lg:text-[4rem] font-semibold mb-6 text-[#1e293b] leading-[1.15] tracking-tight max-w-5xl mx-auto">
          Your <span class="bg-clip-text text-transparent bg-gradient-to-r from-[#38bdf8] via-[#6366f1] to-[#a855f7]">AI-powered</span> workspace <br class="hidden md:block" />
          for tasks, time, and momentum.
        </h1>

        <!-- Subtitle -->
        <p class="text-[1.1rem] md:text-[1.25rem] mb-10 max-w-2xl mx-auto text-slate-500 leading-relaxed font-medium">
          Turn ideas into structured tasks, organize them in a fluid Kanban board,
          and let Chronova's AI Copilot schedule what matters most.
        </p>

        <!-- Buttons -->
        <div class="flex flex-col sm:flex-row justify-center items-center gap-4 mb-4 w-full sm:w-auto">
          <button class="flex items-center justify-center gap-2 w-full sm:w-auto px-8 py-3.5 rounded-xl font-semibold text-white bg-gradient-to-r from-[#2dd4bf] via-[#3b82f6] to-[#a855f7] hover:opacity-90 transition-all duration-300 shadow-[0_8px_25px_rgba(59,130,246,0.35)] hover:-translate-y-0.5 hover:shadow-[0_12px_30px_rgba(59,130,246,0.45)]">
            Get Started Free
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M9 5l7 7-7 7"></path></svg>
          </button>
          
          <button class="flex items-center justify-center gap-3 w-full sm:w-auto px-8 py-3.5 rounded-xl font-semibold text-slate-800 bg-white border border-slate-100 hover:bg-slate-50 transition-all duration-300 shadow-[0_8px_25px_rgba(0,0,0,0.04)] hover:-translate-y-0.5 hover:shadow-[0_12px_30px_rgba(0,0,0,0.06)]">
            <div class="w-6 h-6 rounded-full border border-slate-200 flex items-center justify-center bg-white shadow-sm">
              <svg class="w-3 h-3 text-indigo-600 ml-0.5" fill="currentColor" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"></path></svg>
            </div>
            Watch Demo
          </button>
        </div>

        <!-- Demo Image -->
        <div class="max-w-5xl mx-auto relative z-20 flex justify-center mt-8">
          <img src="/demo-image.png" alt="Chronova Demo" class="w-full h-auto drop-shadow-[0_20px_40px_rgba(99,102,241,0.2)]" />
        </div>
      </div>
    </section>

    <!-- Glowing Section Divider -->
    <div class="w-full h-px relative z-20 flex justify-center items-center bg-slate-200/80">
      <div class="absolute w-1/2 max-w-3xl h-[2px] bg-gradient-to-r from-transparent via-indigo-500/40 to-transparent blur-[2px]"></div>
      <div class="absolute w-1/3 max-w-lg h-px bg-gradient-to-r from-transparent via-indigo-400/80 to-transparent shadow-[0_0_8px_rgba(99,102,241,0.8)]"></div>
    </div>

    <!-- How It Works Section -->
    <section id="how-it-works" class="relative z-10 w-full bg-[#f8f9fc]">
      <!-- Localized sticky background -->
      <div class="absolute inset-0 w-full h-full z-0 pointer-events-none">
        <div class="sticky top-0 w-full h-screen overflow-hidden">
          <div class="absolute inset-0 bg-[url('/how-it-works-background.png')] bg-cover bg-center"></div>
          <div class="absolute inset-0 bg-white/40"></div>
        </div>
      </div>
      
      <!-- The new complex How It Works Component -->
      <HowItWorks class="relative z-10" />
    </section>

    <!-- Glowing Section Divider -->
    <div class="w-full h-px relative z-20 flex justify-center items-center bg-slate-200/80">
      <div class="absolute w-1/2 max-w-3xl h-[2px] bg-gradient-to-r from-transparent via-indigo-500/40 to-transparent blur-[2px]"></div>
      <div class="absolute w-1/3 max-w-lg h-px bg-gradient-to-r from-transparent via-indigo-400/80 to-transparent shadow-[0_0_8px_rgba(99,102,241,0.8)]"></div>
    </div>

    <!-- Features Section -->
    <Features id="features" />

    <!-- Glowing Section Divider -->
    <div class="w-full h-px relative z-20 flex justify-center items-center bg-slate-200/80">
      <div class="absolute w-1/2 max-w-3xl h-[2px] bg-gradient-to-r from-transparent via-indigo-500/40 to-transparent blur-[2px]"></div>
      <div class="absolute w-1/3 max-w-lg h-px bg-gradient-to-r from-transparent via-indigo-400/80 to-transparent shadow-[0_0_8px_rgba(99,102,241,0.8)]"></div>
    </div>

    <!-- Pricing Section -->
    <Pricing id="pricing" />

    <!-- Glowing Section Divider -->
    <div class="w-full h-px relative z-20 flex justify-center items-center bg-slate-200/80">
      <div class="absolute w-1/2 max-w-3xl h-[2px] bg-gradient-to-r from-transparent via-indigo-500/40 to-transparent blur-[2px]"></div>
      <div class="absolute w-1/3 max-w-lg h-px bg-gradient-to-r from-transparent via-indigo-400/80 to-transparent shadow-[0_0_8px_rgba(99,102,241,0.8)]"></div>
    </div>

    <!-- FAQ Section -->
    <Faq id="faq" />

    <!-- Footer -->
    <Footer />
  </div>
</template>

<script setup>
useHead({
  title: 'Chronova - AI-Powered Kanban Scheduler',
  meta: [
    { name: 'description', content: 'Turn ideas into structured tasks and organize them in a fluid Kanban board.' }
  ]
})
</script>
