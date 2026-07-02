<template>
  <div>
    <!-- Welcome Header -->
    <div class="mb-8">
      <h1 class="text-2xl font-bold text-slate-900 mb-1 flex items-center gap-2">
        Welcome back, Ammar <span class="text-xl">👋</span>
      </h1>
      <p class="text-sm text-slate-500">You have 6 tasks scheduled today and 2 high priority items.</p>
    </div>

    <!-- Main Grid -->
    <div class="grid grid-cols-1 xl:grid-cols-4 gap-8">
      
      <!-- Left Content (Stats, Kanban, Bottom sections) -->
      <div class="xl:col-span-3 space-y-8 flex flex-col min-h-0">
        
        <!-- Stat Cards -->
        <DashboardStatCards />

        <!-- Kanban Board -->
        <DashboardKanbanBoard class="flex-1" />

        <!-- Bottom Section -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
          <DashboardProductivityChart />
          <DashboardRecentActivity />
        </div>
        
      </div>

      <!-- Right Panel -->
      <div class="xl:col-span-1">
        <DashboardRightPanel />
      </div>

    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'dashboard'
})

useHead({
  title: 'Dashboard - Chronova'
})
</script>
