<template>
  <section class="relative w-full pt-32 pb-16 font-sans bg-[#f8f9fc] overflow-hidden">
    <!-- Static background image that covers the fixed section height -->
    <div class="absolute inset-0 w-full h-full z-0 pointer-events-none">
      <img src="/faq-background.png" alt="FAQ Background" class="w-full h-full object-cover object-top opacity-100" />
    </div>
    
    <div class="relative z-10 w-full max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <!-- Header -->
      <div class="flex flex-col items-center text-center mb-12">
        <div class="inline-flex items-center px-4 py-1.5 rounded-full border border-indigo-100 bg-white/60 backdrop-blur-md mb-6 shadow-sm">
          <span class="text-xs font-bold tracking-wider text-indigo-600 uppercase">FAQ</span>
        </div>
        <h2 class="text-4xl md:text-5xl font-bold text-slate-900 tracking-tight mb-5">
          Frequently Asked Questions
        </h2>
        <p class="text-slate-600 max-w-xl mx-auto leading-relaxed">
          Have questions? We've got answers.<br />
          If you can't find what you're looking for, feel free to reach out.
        </p>
      </div>

      <!-- FAQ Accordion -->
      <div class="flex flex-col gap-4 h-[700px] md:h-[600px]">
        <div 
          v-for="(faq, index) in faqs" 
          :key="index"
          class="bg-white/60 backdrop-blur-xl rounded-[1.25rem] border border-white shadow-[0_4px_20px_rgba(0,0,0,0.02)] overflow-hidden transition-all duration-300"
          :class="{ 'ring-1 ring-indigo-100/50 shadow-[0_8px_30px_rgba(99,102,241,0.06)]': activeIndex === index }"
        >
          <button 
            @click="toggle(index)"
            class="w-full px-8 py-5 flex items-center justify-between text-left focus:outline-none"
          >
            <span class="font-bold text-slate-800 pr-8">{{ faq.question }}</span>
            <div 
              class="w-7 h-7 rounded-full flex items-center justify-center flex-shrink-0 transition-colors"
              :class="activeIndex === index ? 'bg-indigo-50 text-indigo-600' : 'bg-slate-50/50 text-indigo-400'"
            >
              <svg v-if="activeIndex === index" class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M20 12H4"/></svg>
              <svg v-else class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M12 4v16m8-8H4"/></svg>
            </div>
          </button>
          
          <div 
            class="grid transition-all duration-300 ease-in-out"
            :class="activeIndex === index ? 'grid-rows-[1fr] opacity-100' : 'grid-rows-[0fr] opacity-0'"
          >
            <div class="overflow-hidden">
              <p class="px-8 pb-6 text-sm text-slate-500 leading-relaxed max-w-3xl">
                {{ faq.answer }}
              </p>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(0)

const toggle = (index) => {
  activeIndex.value = activeIndex.value === index ? -1 : index
}

const faqs = [
  {
    question: 'What is Chronova?',
    answer: 'Chronova is an AI-powered Kanban and scheduler that helps teams plan, prioritize, and track work in one intelligent workspace.'
  },
  {
    question: 'How does the AI scheduling work?',
    answer: 'Our AI analyzes your tasks, deadlines, and working patterns to automatically suggest the most optimal schedule, ensuring you focus on high-impact work without getting burned out.'
  },
  {
    question: 'Can I integrate Chronova with other tools?',
    answer: 'Yes, Chronova offers seamless integrations with popular tools like Slack, GitHub, Jira, and Google Calendar to keep your workflow connected.'
  },
  {
    question: 'Is my data secure?',
    answer: 'We take security seriously. All data is encrypted at rest and in transit, and we comply with industry standards to ensure your information is always protected.'
  },
  {
    question: 'Can I change my plan later?',
    answer: 'Absolutely! You can upgrade, downgrade, or cancel your plan at any time right from your account settings. Prorated refunds are applied automatically.'
  },
  {
    question: 'Do you offer refunds?',
    answer: 'We offer a 14-day money-back guarantee for all paid plans. If you\'re not satisfied, simply reach out to our support team for a full refund.'
  }
]
</script>
