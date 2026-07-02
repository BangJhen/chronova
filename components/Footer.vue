<template>
  <footer class="bg-white border-t border-slate-200 py-16 px-4 relative z-10 font-sans">
    <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-10 lg:gap-8">
      
      <!-- Brand & Logo -->
      <div class="lg:col-span-2">
        <NuxtLink to="/" class="inline-block mb-6">
          <img src="/logo.png" alt="Chronova Logo" class="h-10 w-auto" />
        </NuxtLink>
        <p class="text-slate-500 mb-6 leading-relaxed max-w-sm">
          Plan smarter, move faster. Chronova adalah AI-powered Kanban scheduler yang dirancang untuk menyederhanakan alur kerja dan mengubah ide menjadi tugas terstruktur.
        </p>
        <div class="flex items-center gap-4">
          <!-- Social Icons -->
          <a href="#" class="w-10 h-10 rounded-full bg-slate-50 flex items-center justify-center text-slate-400 hover:bg-indigo-50 hover:text-indigo-600 transition-colors shadow-sm">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/></svg>
          </a>
          <a href="#" class="w-10 h-10 rounded-full bg-slate-50 flex items-center justify-center text-slate-400 hover:bg-indigo-50 hover:text-indigo-600 transition-colors shadow-sm">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
          </a>
          <a href="#" class="w-10 h-10 rounded-full bg-slate-50 flex items-center justify-center text-slate-400 hover:bg-indigo-50 hover:text-indigo-600 transition-colors shadow-sm">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
          </a>
        </div>
      </div>

      <!-- Product Links -->
      <div>
        <h4 class="font-bold text-slate-900 mb-6 uppercase tracking-wider text-sm">Produk</h4>
        <ul class="space-y-3.5 text-sm text-slate-500">
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Fitur</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Harga</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Integrasi</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Changelog</a></li>
        </ul>
      </div>

      <!-- Company Links -->
      <div>
        <h4 class="font-bold text-slate-900 mb-6 uppercase tracking-wider text-sm">Perusahaan</h4>
        <ul class="space-y-3.5 text-sm text-slate-500">
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Tentang Kami</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Karir</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Blog</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Hubungi Kami</a></li>
        </ul>
      </div>

      <!-- Legal Links -->
      <div>
        <h4 class="font-bold text-slate-900 mb-6 uppercase tracking-wider text-sm">Legal</h4>
        <ul class="space-y-3.5 text-sm text-slate-500">
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Syarat & Ketentuan</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Kebijakan Privasi</a></li>
          <li><a href="#" class="hover:text-indigo-600 transition-colors">Kebijakan Cookie</a></li>
        </ul>
      </div>

    </div>

    <!-- Bottom Bar -->
    <div class="max-w-6xl mx-auto mt-16 pt-8 border-t border-slate-100 flex flex-col md:flex-row items-center justify-between gap-4">
      <p class="text-sm text-slate-400">
        &copy; {{ new Date().getFullYear() }} Chronova Inc. Hak cipta dilindungi.
      </p>
      <div class="flex items-center gap-6 text-sm text-slate-400">
        <span class="flex items-center gap-1.5">
          <span class="relative flex h-2 w-2">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-green-400 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-2 w-2 bg-green-500"></span>
          </span>
          Semua sistem normal
        </span>
      </div>
    </div>
  </footer>
</template>
