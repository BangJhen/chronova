<template>
  <button 
    @click="scrollToTop"
    :class="[
      'fixed bottom-8 right-8 z-50 p-3 rounded-2xl bg-gradient-to-tr from-indigo-600 to-purple-600 text-white shadow-[0_4px_20px_rgba(79,70,229,0.4)] hover:shadow-[0_8px_30px_rgba(79,70,229,0.5)] hover:-translate-y-1 transition-all duration-300',
      isVisible ? 'opacity-100 translate-y-0 visible' : 'opacity-0 translate-y-10 invisible'
    ]"
    aria-label="Scroll to top"
  >
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
  </button>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isVisible = ref(false)

const toggleVisibility = () => {
  if (window.scrollY > 400) {
    isVisible.value = true
  } else {
    isVisible.value = false
  }
}

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}

onMounted(() => {
  window.addEventListener('scroll', toggleVisibility)
})

onUnmounted(() => {
  window.removeEventListener('scroll', toggleVisibility)
})
</script>
