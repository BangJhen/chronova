<template>
  <div class="min-h-screen bg-slate-50 font-sans text-slate-900 flex">
    <!-- Sidebar -->
    <DashboardSidebar />
    
    <!-- Main Content Wrapper (offset by sidebar width) -->
    <div class="flex-1 ml-[240px] flex flex-col min-h-screen">
      <!-- Topbar (sticky, spans remaining width) -->
      <DashboardTopbar class="ml-0" />
      
      <!-- Page Content -->
      <main class="flex-1 p-8">
        <slot />
      </main>
    </div>
  </div>
</template>
