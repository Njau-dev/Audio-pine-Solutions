<template>
  <footer class="relative z-50 w-full bg-gray-800 border-t border-gray-700">
    <div class="container max-w-6xl px-8 py-12 mx-auto xl:px-0">
      <div class="grid grid-cols-1 gap-8 md:grid-cols-4">
        <!-- Brand Column -->
        <div class="space-y-4">
          <a href="/" class="relative flex items-center h-full font-black leading-none">
            <img src="/src/assets/images/logo.jpeg" alt="Logo" class="w-auto h-12" >
            <span class="ml-3 text-xl text-text">AudioPine <span class="text-primary">.</span></span>
          </a>

          <p class="text-sm text-gray-400">
            Digital Growth Engine For your Business
          </p>
        </div>

        <!-- Links -->
        <div class="space-y-4">
          <h3 class="text-lg font-semibold text-white">Products</h3>
          <div class="flex flex-col space-y-2">
            <a href="#services" class="text-gray-400 hover:text-indigo-500">Services</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Solutions</a>
            <a href="#pricing" class="text-gray-400 hover:text-indigo-500">Pricing</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Demo</a>
          </div>
        </div>

        <!-- Company -->
        <div class="space-y-4">
          <h3 class="text-lg font-semibold text-white">Company</h3>
          <div class="flex flex-col space-y-2">
            <a href="#" class="text-gray-400 hover:text-indigo-500">About</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Blog</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Careers</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Contact</a>
          </div>
        </div>

        <!-- Legal -->
        <div class="space-y-4">
          <h3 class="text-lg font-semibold text-white">Legal</h3>
          <div class="flex flex-col space-y-2">
            <a href="#" class="text-gray-400 hover:text-indigo-500">Privacy</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Terms</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Security</a>
            <a href="#" class="text-gray-400 hover:text-indigo-500">Cookie Policy</a>
          </div>
        </div>
      </div>

      <!-- Bottom Section -->
      <div class="pt-8 mt-12 border-t border-gray-700">
        <div class="flex flex-col items-center justify-between md:flex-row">
          <p class="text-sm text-gray-400">
            © 2025 AudioPine. All rights reserved.
          </p>
          
          <!-- Social Links -->
          <div class="flex space-x-6 justify-center pt-8">
            <!-- Twitter -->
            <a href="#" class="text-primary hover:text-company">
                <span class="sr-only">Twitter</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"/>
                </svg>
            </a>

            <!-- Facebook -->
            <a href="https://www.facebook.com/share/1EbqhtMZn7/" class="text-primary hover:text-company">
                <span class="sr-only">Facebook</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd"/>
                </svg>
            </a>

            <!-- Instagram -->
            <a href="https://www.instagram.com/audiopinesolutions?igsh=Njd3cXg2ZHk1NGRs" class="text-primary hover:text-company">
                <span class="sr-only">Instagram</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/>
                </svg>
            </a>

            <!-- TikTok -->
            <a href="https://vm.tiktok.com/ZMBPP1w3s/" class="text-primary hover:text-company">
                <span class="sr-only">TikTok</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                </svg>
            </a>
            </div>
        </div>
      </div>
    </div>
  </footer>
</template>