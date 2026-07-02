<template>
  <div ref="containerRef" class="w-full relative" style="height: 400vh;">
    <!-- Sticky Wrapper that stays on screen while scrolling the 400vh height -->
    <div class="sticky top-0 w-full h-screen flex flex-col items-center justify-center py-12 px-4 md:px-8 font-sans z-10 overflow-hidden">
    
    <!-- Header Section -->
    <div class="flex flex-col items-center text-center mb-16">
      <!-- Badge -->
      <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-indigo-100 bg-white/50 backdrop-blur-md mb-6 shadow-sm">
        <svg class="w-4 h-4 text-blue-500" viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 2l2.4 7.6 7.6 2.4-7.6 2.4L12 22l-2.4-7.6-7.6-2.4 7.6-2.4L12 2z"/>
        </svg>
        <span class="text-xs font-semibold tracking-wider text-indigo-800 uppercase">How It Works</span>
      </div>
      
      <!-- Headline -->
      <h2 class="text-4xl md:text-5xl font-semibold text-slate-800 tracking-tight mb-4">
        Get started in <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 via-indigo-500 to-purple-500">4 simple steps</span>
      </h2>
      
      <!-- Subtitle -->
      <p class="text-lg text-slate-500 max-w-2xl mx-auto leading-relaxed">
        Chronova adapts to your workflow in minutes.<br class="hidden sm:block" />
        From planning to progress—AI handles the busywork.
      </p>
    </div>

    <!-- Main Content Grid -->
    <div class="w-full max-w-6xl mx-auto flex flex-col lg:flex-row gap-12 lg:gap-8">
      
      <!-- Left Column: Timeline Steps -->
      <div class="w-full lg:w-[400px] relative">
        <!-- Thin Vertical Line -->
        <div class="absolute left-6 top-10 bottom-16 w-px bg-indigo-200/60 z-0 hidden lg:block"></div>
        
        <div class="flex flex-col gap-6 relative z-10">
          
          <!-- Dynamic Steps -->
          <div v-for="step in steps" :key="step.id" 
               @click="activeStep = step.id"
               :class="['flex items-start gap-5 group cursor-pointer transition-all duration-300', activeStep === step.id ? 'relative' : 'opacity-80 hover:opacity-100']">
            
            <!-- Number Circle -->
            <div class="relative z-10 mt-3 hidden lg:flex items-center justify-center w-12 h-12 flex-shrink-0">
              <!-- Active Halo -->
              <div v-if="activeStep === step.id" class="absolute inset-[-3px] bg-white/90 backdrop-blur-md rounded-full shadow-[0_0_20px_rgba(99,102,241,0.3)] z-0 border border-indigo-50"></div>
              
              <!-- Inner Circle -->
              <div :class="[
                'flex items-center justify-center font-bold text-base relative z-10 shadow-sm rounded-full w-10 h-10',
                activeStep === step.id 
                  ? 'bg-gradient-to-br from-blue-500 via-indigo-500 to-purple-500 text-white shadow-inner' 
                  : 'bg-white/80 backdrop-blur-md text-slate-600 border border-slate-200'
              ]">
                {{ step.id }}
              </div>
            </div>
            
            <!-- Card -->
            <div :class="[
              'flex-grow rounded-[1.25rem] p-5 shadow-sm flex items-center gap-4 transition-colors',
              activeStep === step.id 
                ? 'bg-white/90 backdrop-blur-xl border border-indigo-200/80 shadow-[0_8px_30px_-5px_rgba(99,102,241,0.15)] relative z-10' 
                : 'bg-white/40 backdrop-blur-lg border border-white/60 group-hover:bg-white/60'
            ]">
              <!-- Icon Box -->
              <div :class="[
                'w-12 h-12 rounded-[1rem] flex items-center justify-center flex-shrink-0 border shadow-sm',
                activeStep === step.id ? 'bg-white border-indigo-50' : 'bg-white/80 backdrop-blur-sm border-white'
              ]">
                <svg v-if="step.id === 1" class="w-6 h-6 text-indigo-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M12 2L15 9l7 3-7 3-3 7-3-7-7-3 7-3z" fill="currentColor" class="text-indigo-200" stroke="none" />
                </svg>
                <svg v-else-if="step.id === 2" class="w-6 h-6 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h7"></path></svg>
                <svg v-else-if="step.id === 3" class="w-6 h-6 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                <svg v-else-if="step.id === 4" class="w-6 h-6 text-purple-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 12l3-3 3 3 4-4M8 21l4-4 4 4M3 4h18M4 4h16v12a1 1 0 01-1 1H5a1 1 0 01-1-1V4z"></path></svg>
              </div>
              
              <!-- Text -->
              <div class="flex-grow">
                <h4 :class="['font-bold text-[15px] mb-1', activeStep === step.id ? 'text-slate-800' : 'text-slate-700']">{{ step.title }}</h4>
                <p class="text-xs text-slate-500 leading-relaxed font-medium">{{ step.description }}</p>
              </div>
              
              <!-- Active Arrow (Always rendered to maintain layout width, hidden via opacity when inactive) -->
              <svg :class="['w-5 h-5 flex-shrink-0 transition-opacity duration-300', activeStep === step.id ? 'text-slate-400 opacity-100' : 'opacity-0']" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M9 5l7 7-7 7"></path></svg>
            </div>
          </div>
        </div>
      </div>

      <!-- Right Column: Step Detail UI Mockup -->
      <div class="w-full flex-1 min-w-0 relative mt-4 lg:mt-0">
        <!-- Main Glass Panel -->
        <div class="w-full h-auto lg:h-[550px] bg-white/30 backdrop-blur-xl rounded-[2.5rem] border border-white/60 shadow-[0_20px_60px_-15px_rgba(0,0,0,0.05)] p-8 lg:p-12 relative overflow-hidden">
          
          <!-- Decorative Background Gradients -->
          <div class="absolute top-0 right-0 w-64 h-64 bg-purple-200/40 rounded-full blur-3xl -translate-y-1/2 translate-x-1/3"></div>
          <div class="absolute bottom-0 left-0 w-72 h-72 bg-blue-200/40 rounded-full blur-3xl translate-y-1/3 -translate-x-1/4"></div>

          <div class="relative z-10 h-full flex flex-col">
            <!-- Header of Step -->
            <div class="mb-10 transition-all duration-300">
              <div class="inline-flex items-center gap-3 mb-4">
                <div class="px-3 py-1 rounded-lg bg-gradient-to-r from-indigo-500 to-purple-500 text-white text-[11px] font-black tracking-widest shadow-[0_4px_12px_rgba(99,102,241,0.3)]">
                  STEP 0{{ activeStep }}
                </div>
                <div class="w-12 h-[2px] bg-indigo-100 rounded-full"></div>
              </div>
              <h3 class="text-3xl lg:text-4xl font-extrabold text-slate-800 tracking-tight mb-4">{{ currentStepData.title }}</h3>
              <p class="text-slate-500 text-lg max-w-md">{{ currentStepData.description }}</p>
            </div>

            <!-- Content Area (Dynamic based on step) -->
            <transition name="fade" mode="out-in">
              <div :key="activeStep" class="flex flex-col md:flex-row gap-6 lg:gap-10 h-full">
                
                <!-- STEP 1 CONTENT -->
                <template v-if="activeStep === 1">
                  <!-- Left Mini Cards -->
                  <div class="flex flex-col justify-center gap-4 w-full md:w-1/3 transform origin-top-left scale-[0.85]">
                    <div class="bg-white/80 backdrop-blur-md rounded-2xl p-5 border border-white shadow-sm flex flex-col">
                      <div class="w-10 h-10 rounded-full bg-indigo-50 flex items-center justify-center mb-3 text-indigo-500">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
                      </div>
                      <h5 class="font-bold text-slate-800 text-sm mb-1">Secure & private</h5>
                      <p class="text-xs text-slate-500">Enterprise-grade security to keep your data safe.</p>
                    </div>
                    
                    <div class="bg-white/80 backdrop-blur-md rounded-2xl p-5 border border-white shadow-sm flex flex-col">
                      <div class="w-10 h-10 rounded-full bg-blue-50 flex items-center justify-center mb-3 text-blue-500">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                      </div>
                      <h5 class="font-bold text-slate-800 text-sm mb-1">Ready in seconds</h5>
                      <p class="text-xs text-slate-500">Get your workspace up and running instantly.</p>
                    </div>
                  </div>

                  <!-- Right Mockup Card -->
                  <div class="w-full md:w-2/3 flex items-center justify-end relative transform origin-top-right scale-[0.85]">
                    <div class="w-full max-w-[350px] bg-white/80 backdrop-blur-xl rounded-[1.5rem] p-6 border border-white shadow-[0_15px_50px_-10px_rgba(0,0,0,0.1)] relative z-10">
                      <div class="w-10 h-10 rounded-xl bg-indigo-50 flex items-center justify-center mb-4 text-indigo-500 shadow-sm border border-indigo-100/50">
                        <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                          <path d="M12 2L15 9l7 3-7 3-3 7-3-7-7-3 7-3z" fill="currentColor" class="text-indigo-200" stroke="none" />
                        </svg>
                      </div>
                      
                      <h4 class="text-lg font-bold text-slate-800 mb-4">Create Workspace</h4>
                      
                      <div class="space-y-4">
                        <!-- Form Group 1 -->
                        <div>
                          <label class="block text-xs font-semibold text-slate-500 mb-1.5">Workspace name</label>
                          <input type="text" value="Chronova Team" class="w-full px-3 py-2.5 bg-white border border-slate-200 rounded-lg text-sm text-slate-800 font-medium focus:outline-none focus:ring-2 focus:ring-indigo-500/20 shadow-sm" readonly />
                        </div>
                        
                        <!-- Form Group 2 -->
                        <div>
                          <label class="block text-xs font-semibold text-slate-500 mb-1.5">Invite members</label>
                          <div class="flex items-center bg-white border border-slate-200 rounded-lg shadow-sm overflow-hidden">
                            <input type="text" placeholder="Enter email address..." class="flex-grow px-3 py-2.5 text-sm text-slate-800 focus:outline-none placeholder-slate-400 bg-transparent" readonly />
                            <div class="px-3 py-2.5 border-l border-slate-200 bg-slate-50 text-xs font-medium text-slate-600 flex items-center gap-1">
                              Viewer
                              <svg class="w-3 h-3 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                            </div>
                          </div>
                        </div>

                        <!-- Avatars -->
                        <div class="flex items-center gap-1 pt-1">
                          <div class="flex -space-x-2">
                            <img class="w-8 h-8 rounded-full border-2 border-white object-cover" src="https://i.pravatar.cc/100?img=11" alt="Avatar" />
                            <img class="w-8 h-8 rounded-full border-2 border-white object-cover" src="https://i.pravatar.cc/100?img=33" alt="Avatar" />
                            <img class="w-8 h-8 rounded-full border-2 border-white object-cover" src="https://i.pravatar.cc/100?img=47" alt="Avatar" />
                            <img class="w-8 h-8 rounded-full border-2 border-white object-cover" src="https://i.pravatar.cc/100?img=12" alt="Avatar" />
                            <img class="w-8 h-8 rounded-full border-2 border-white object-cover" src="https://i.pravatar.cc/100?img=15" alt="Avatar" />
                          </div>
                          <span class="text-xs font-semibold text-slate-400 ml-2 bg-slate-100 px-2 py-1 rounded-full">+3</span>
                        </div>

                        <!-- Button -->
                        <button class="w-full py-3.5 mt-2 rounded-xl bg-gradient-to-r from-blue-400 via-indigo-500 to-purple-500 text-white font-bold text-sm shadow-[0_8px_20px_rgba(99,102,241,0.3)] opacity-100 cursor-default">
                          Create Workspace
                        </button>
                      </div>
                    </div>
                  </div>
                </template>

                <!-- STEP 2 CONTENT -->
                <template v-else-if="activeStep === 2">
                  <div class="flex flex-col justify-center gap-4 w-full md:w-1/3 transform origin-top-left scale-[0.85]">
                    <div class="bg-white/80 backdrop-blur-md rounded-2xl p-5 border border-white shadow-sm flex flex-col">
                      <div class="w-10 h-10 rounded-full bg-blue-50 flex items-center justify-center mb-3 text-blue-500">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
                      </div>
                      <h5 class="font-bold text-slate-800 text-sm mb-1">Bulk Import</h5>
                      <p class="text-xs text-slate-500">Import hundreds of tasks from CSV or Jira instantly.</p>
                    </div>
                    <div class="bg-white/80 backdrop-blur-md rounded-2xl p-5 border border-white shadow-sm flex flex-col">
                      <div class="w-10 h-10 rounded-full bg-indigo-50 flex items-center justify-center mb-3 text-indigo-500">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                      </div>
                      <h5 class="font-bold text-slate-800 text-sm mb-1">Smart Sorting</h5>
                      <p class="text-xs text-slate-500">Automatic categorization based on project context.</p>
                    </div>
                  </div>
                  
                  <div class="w-full md:w-2/3 flex items-center justify-end relative transform origin-top-right scale-[0.85]">
                    <div class="w-full max-w-[380px] bg-white/80 backdrop-blur-xl rounded-[2rem] p-6 border border-white shadow-[0_15px_50px_-10px_rgba(0,0,0,0.1)] relative z-10">
                      <div class="flex items-center justify-between mb-6">
                        <h4 class="text-lg font-bold text-slate-800">Task Backlog</h4>
                        <button class="text-xs bg-indigo-50 text-indigo-600 px-3 py-1.5 rounded-lg font-bold cursor-default">Add Task</button>
                      </div>
                      <div class="space-y-3">
                        <div class="p-3 bg-white border border-slate-100 rounded-xl shadow-sm flex items-center gap-3">
                          <div class="w-4 h-4 rounded border border-slate-300"></div>
                          <span class="text-sm font-medium text-slate-700">Design landing page UI</span>
                        </div>
                        <div class="p-3 bg-white border border-slate-100 rounded-xl shadow-sm flex items-center gap-3">
                          <div class="w-4 h-4 rounded border border-slate-300 bg-blue-500 border-blue-500 flex items-center justify-center">
                            <svg class="w-3 h-3 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="3" d="M5 13l4 4L19 7"></path></svg>
                          </div>
                          <span class="text-sm font-medium text-slate-400 line-through">Setup database schema</span>
                        </div>
                        <div class="p-3 bg-white border border-slate-100 rounded-xl shadow-sm flex items-center gap-3">
                          <div class="w-4 h-4 rounded border border-slate-300"></div>
                          <span class="text-sm font-medium text-slate-700">Write API documentation</span>
                        </div>
                        <div class="p-3 bg-white border border-slate-100 rounded-xl shadow-sm flex items-center gap-3 opacity-60">
                          <div class="w-4 h-4 rounded border border-slate-300 border-dashed"></div>
                          <span class="text-sm font-medium text-slate-400">Add new task...</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </template>

                <!-- STEP 3 CONTENT -->
                <template v-else-if="activeStep === 3">
                  <div class="flex flex-col justify-center gap-4 w-full md:w-1/3 transform origin-top-left scale-[0.85]">
                    <div class="bg-white/80 backdrop-blur-md rounded-2xl p-5 border border-white shadow-sm flex flex-col">
                      <div class="w-10 h-10 rounded-full bg-teal-50 flex items-center justify-center mb-3 text-teal-500">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                      </div>
                      <h5 class="font-bold text-slate-800 text-sm mb-1">Auto-Scheduling</h5>
                      <p class="text-xs text-slate-500">AI predicts deadlines and assigns capacity.</p>
                    </div>
                  </div>
                  
                  <div class="w-full md:w-2/3 flex items-center justify-end relative transform origin-top-right scale-[0.85]">
                    <div class="w-full max-w-[380px] bg-white/80 backdrop-blur-xl rounded-[2rem] p-6 border border-white shadow-[0_15px_50px_-10px_rgba(0,0,0,0.1)] relative z-10">
                      <h4 class="text-lg font-bold text-slate-800 mb-2">AI Generation</h4>
                      <p class="text-xs text-slate-500 mb-4">Building optimal sprint plan...</p>
                      <div class="w-full bg-slate-100 rounded-full h-2 mb-6 overflow-hidden">
                        <div class="bg-teal-400 h-2 rounded-full w-2/3"></div>
                      </div>
                      <div class="space-y-3">
                        <div class="flex items-center gap-3 p-2 bg-slate-50/50 rounded-lg">
                          <svg class="w-4 h-4 text-teal-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
                          <span class="text-xs text-slate-600 font-medium">Analyzing 43 tasks</span>
                        </div>
                        <div class="flex items-center gap-3 p-2 bg-slate-50/50 rounded-lg">
                          <svg class="w-4 h-4 text-teal-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
                          <span class="text-xs text-slate-600 font-medium">Estimating workload</span>
                        </div>
                        <div class="flex items-center gap-3 p-2 bg-white border border-slate-100 shadow-sm rounded-lg">
                          <div class="w-4 h-4 rounded-full border-2 border-slate-200 border-t-teal-500"></div>
                          <span class="text-xs text-slate-800 font-bold">Assigning team members...</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </template>

                <!-- STEP 4 CONTENT -->
                <template v-else-if="activeStep === 4">
                  <div class="flex flex-col justify-center gap-4 w-full md:w-1/3 transform origin-top-left scale-[0.85]">
                    <div class="bg-white/80 backdrop-blur-md rounded-2xl p-5 border border-white shadow-sm flex flex-col">
                      <div class="w-10 h-10 rounded-full bg-purple-50 flex items-center justify-center mb-3 text-purple-500">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 12l3-3 3 3 4-4M8 21l4-4 4 4M3 4h18M4 4h16v12a1 1 0 01-1 1H5a1 1 0 01-1-1V4z"></path></svg>
                      </div>
                      <h5 class="font-bold text-slate-800 text-sm mb-1">Velocity Insights</h5>
                      <p class="text-xs text-slate-500">Track team performance over time.</p>
                    </div>
                  </div>
                  
                  <div class="w-full md:w-2/3 flex items-center justify-end relative transform origin-top-right scale-[0.85]">
                    <div class="w-full max-w-[380px] bg-white/80 backdrop-blur-xl rounded-[2rem] p-6 border border-white shadow-[0_15px_50px_-10px_rgba(0,0,0,0.1)] relative z-10">
                      <h4 class="text-lg font-bold text-slate-800 mb-6">Sprint Progress</h4>
                      <div class="flex items-end gap-2 h-32 mb-4">
                        <div class="w-full bg-purple-100 rounded-t-md h-[40%]"></div>
                        <div class="w-full bg-purple-200 rounded-t-md h-[60%]"></div>
                        <div class="w-full bg-purple-300 rounded-t-md h-[30%]"></div>
                        <div class="w-full bg-purple-400 rounded-t-md h-[80%]"></div>
                        <div class="w-full bg-purple-500 rounded-t-md h-[100%]"></div>
                      </div>
                      <div class="flex justify-between text-xs text-slate-500 font-semibold mb-6">
                        <span>Mon</span>
                        <span>Tue</span>
                        <span>Wed</span>
                        <span>Thu</span>
                        <span>Fri</span>
                      </div>
                      <div class="p-3 bg-purple-50 rounded-xl flex items-center justify-between border border-purple-100">
                        <span class="text-xs font-bold text-purple-700">Team Velocity</span>
                        <span class="text-sm font-extrabold text-purple-600">+24%</span>
                      </div>
                    </div>
                  </div>
                </template>

              </div>
            </transition>
          </div>
        </div>
        
        <!-- Arrow pointing to See How It Works -->
      </div>
    </div>

    <!-- Built for teams section -->
    <div class="w-full max-w-5xl mx-auto relative group mt-12">
      <!-- Liquid glass effect: glowing background blob -->
      <div class="absolute -inset-0.5 bg-gradient-to-r from-indigo-300 to-purple-300 rounded-[2.5rem] blur-xl opacity-30 group-hover:opacity-60 transition duration-1000"></div>
      
      <div class="relative bg-white/30 backdrop-blur-2xl rounded-[2.5rem] border border-white/60 shadow-[0_8px_32px_rgba(255,255,255,0.2)] p-10 overflow-hidden ring-1 ring-white/40">
        <h3 class="text-center font-bold text-slate-800 text-xl mb-10">Built for teams of all sizes</h3>
        
        <div class="grid grid-cols-2 md:grid-cols-5 gap-6 text-center relative z-10">
          <!-- Item 1 -->
          <div class="flex flex-col items-center gap-3">
            <div class="w-12 h-12 rounded-2xl bg-indigo-50/80 backdrop-blur-md flex items-center justify-center text-indigo-500 border border-indigo-100/50 shadow-inner">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
            </div>
            <span class="text-xs font-semibold text-slate-600">Onboard in minutes</span>
          </div>
          
          <!-- Item 2 -->
          <div class="flex flex-col items-center gap-3">
            <div class="w-12 h-12 rounded-2xl bg-indigo-100/70 backdrop-blur-md flex items-center justify-center text-indigo-600 border border-indigo-200/50 shadow-inner">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"></path></svg>
            </div>
            <span class="text-xs font-semibold text-slate-600">No learning curve</span>
          </div>
          
          <!-- Item 3 -->
          <div class="flex flex-col items-center gap-3">
            <div class="w-12 h-12 rounded-2xl bg-indigo-50/80 backdrop-blur-md flex items-center justify-center text-indigo-500 border border-indigo-100/50 shadow-inner">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path></svg>
            </div>
            <span class="text-xs font-semibold text-slate-600">Enterprise ready</span>
          </div>
          
          <!-- Item 4 -->
          <div class="flex flex-col items-center gap-3">
            <div class="w-12 h-12 rounded-2xl bg-indigo-100/70 backdrop-blur-md flex items-center justify-center text-indigo-600 border border-indigo-200/50 shadow-inner">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z"></path></svg>
            </div>
            <span class="text-xs font-semibold text-slate-600">Access anywhere</span>
          </div>
          
          <!-- Item 5 -->
          <div class="flex flex-col items-center gap-3 col-span-2 md:col-span-1">
            <div class="w-12 h-12 rounded-2xl bg-indigo-50/80 backdrop-blur-md flex items-center justify-center text-indigo-500 border border-indigo-100/50 shadow-inner">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
            </div>
            <span class="text-xs font-semibold text-slate-600">Your data, your control</span>
          </div>
        </div>
      </div>
    </div>
  </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'

const containerRef = ref(null)
const activeStep = ref(1)

const handleScroll = () => {
  if (!containerRef.value) return
  
  const rect = containerRef.value.getBoundingClientRect()
  // Calculate how far the container has scrolled relative to the viewport
  // rect.top is 0 when the top of container hits the top of viewport.
  // We want to track progress from rect.top = 0 to rect.bottom = window.innerHeight
  const maxScroll = rect.height - window.innerHeight
  const scrollProgress = -rect.top / maxScroll
  
  if (scrollProgress < 0) {
    activeStep.value = 1
  } else if (scrollProgress > 1) {
    activeStep.value = 4
  } else {
    // scrollProgress is between 0 and 1
    // Map to 4 steps: 0-0.25 -> step 1, 0.25-0.5 -> step 2, etc.
    const stepIndex = Math.floor(scrollProgress * 4)
    const boundedIndex = Math.max(0, Math.min(3, stepIndex))
    activeStep.value = steps[boundedIndex].id
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
  // Initial check in case user loads page already scrolled
  handleScroll()
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

const steps = [
  {
    id: 1,
    title: 'Create your workspace',
    description: 'Set up your workspace and invite your team in seconds.'
  },
  {
    id: 2,
    title: 'Add your tasks',
    description: 'Import tasks or create new ones. Chronova organizes everything for you.'
  },
  {
    id: 3,
    title: 'Let AI plan for you',
    description: 'Our AI analyzes priorities, estimates time, and builds the perfect plan.'
  },
  {
    id: 4,
    title: 'Track & accomplish more',
    description: 'Stay focused, get smart insights, and ship your best work.'
  }
]

const currentStepData = computed(() => steps.find(s => s.id === activeStep.value) || steps[0])
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.4s ease, transform 0.4s ease;
}

.fade-enter-from {
  opacity: 0;
  transform: translateY(10px);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
