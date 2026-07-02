<template>
  <div class="bg-white rounded-2xl p-6 border border-slate-200 shadow-sm flex flex-col">
    <div class="flex items-center justify-between mb-6">
      <h3 class="font-bold text-slate-900">Productivity Insights</h3>
      <button class="flex items-center gap-1 text-xs font-semibold text-slate-500 hover:text-slate-800">
        This Week
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
      </button>
    </div>

    <div class="flex flex-1 gap-6">
      <!-- Left side summary -->
      <div class="flex flex-col justify-between w-32 py-2">
        <div>
          <p class="text-xs font-semibold text-slate-500 mb-1">Focus Time</p>
          <p class="text-xl font-bold text-slate-900 mb-1">18h 42m</p>
          <p class="text-[10px] font-medium text-emerald-600 flex items-center gap-1">
            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
            15% vs last week
          </p>
        </div>
        
        <div>
          <p class="text-xs font-semibold text-slate-500 mb-1">Tasks Completed</p>
          <p class="text-xl font-bold text-slate-900 mb-1">28</p>
          <p class="text-[10px] font-medium text-emerald-600 flex items-center gap-1">
            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 10l7-7m0 0l7 7m-7-7v18"></path></svg>
            12% vs last week
          </p>
        </div>
      </div>

      <!-- Chart -->
      <div class="flex-1 h-[200px] w-full">
        <ClientOnly fallback-tag="div" fallback="Loading chart...">
          <apexchart 
            type="area" 
            height="100%" 
            :options="chartOptions" 
            :series="series"
          ></apexchart>
        </ClientOnly>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const series = ref([{
  name: 'Focus Hours',
  data: [2.5, 4.2, 3.8, 6.1, 4.9, 1.5, 0]
}])

const chartOptions = ref({
  chart: {
    type: 'area',
    toolbar: { show: false },
    zoom: { enabled: false },
    background: 'transparent',
    fontFamily: 'Outfit, sans-serif'
  },
  colors: ['#6366f1'], // Indigo 500
  fill: {
    type: 'gradient',
    gradient: {
      shadeIntensity: 1,
      opacityFrom: 0.4,
      opacityTo: 0.05,
      stops: [0, 100]
    }
  },
  dataLabels: { enabled: false },
  stroke: {
    curve: 'smooth',
    width: 3
  },
  xaxis: {
    categories: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
    axisBorder: { show: false },
    axisTicks: { show: false },
    labels: {
      style: { colors: '#94a3b8', fontSize: '11px', fontWeight: 500 }
    }
  },
  yaxis: {
    labels: {
      formatter: (value) => value + 'h',
      style: { colors: '#94a3b8', fontSize: '11px', fontWeight: 500 }
    }
  },
  grid: {
    borderColor: '#f1f5f9',
    strokeDashArray: 4,
    xaxis: { lines: { show: true } },
    yaxis: { lines: { show: true } }
  },
  tooltip: {
    theme: 'light',
    y: { formatter: (val) => val + ' hours' }
  }
})
</script>
