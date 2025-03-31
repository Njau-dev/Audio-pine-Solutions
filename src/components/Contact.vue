<template>
    <!-- BEGIN CONTACT SECTION -->
    <section id = "contact"co class="bg-bg relative w-full px-8 py-16 border-t border-border md:py-24 lg:py-32 xl:py-40 xl:px-0">
      <div class="container max-w-6xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-xl font-medium tracking-tight text-primary uppercase mb-4">Get in Touch</h2>
          <h3 class="text-3xl font-black leading-tight text-text sm:text-5xl">
            Let's Build Something Amazing Together
          </h3>
        </div>
  
        <div class="grid grid-cols-1 gap-12 lg:grid-cols-2 lg:gap-24">
          <!-- Contact Form -->
          <div class="p-8 rounded-2xl bg-white shadow-xl">
            <form class="space-y-6">
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">Full Name</label>
                <input type="text" required 
                       class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent">
              </div>
  
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
                <input type="email" required 
                       class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent">
              </div>
  
              <div>
                <label class="block text-sm font-medium text-gray-700 mb-2">Message</label>
                <textarea rows="5" required 
                          class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent"></textarea>
              </div>
  
              <button type="submit" 
                      class="w-full bg-gradient-to-r from-purple-600 to-blue-600 text-white py-4 px-8 rounded-lg font-semibold hover:opacity-90 transition-opacity">
                Send Message
              </button>
            </form>
          </div>
  
          <!-- Contact Info & Map -->
          <div class="space-y-8">
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="flex-shrink-0">
                  <svg class="w-8 h-8 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                          d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                          d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-bold text-text mb-2">Visit Us</h4>
                  <p class="text-gray-600">Audio Pine Solutions, Modern Kiosk next to Old Uchumi Hyper<br>Ola Energies, Ngong Road, Nairobi</p>
                </div>
              </div>
  
              <div class="flex items-start space-x-4">
                <div class="flex-shrink-0">
                  <svg class="w-8 h-8 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                          d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-bold text-text mb-2">Call Us</h4>
                  <p class="text-gray-600">0748 025186<br>Mon-Sat: 9am - 5pm EST</p>
                </div>
              </div>
  
              <div class="flex items-start space-x-4">
                <div class="flex-shrink-0">
                  <svg class="w-8 h-8 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                          d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                  </svg>
                </div>
                <div>
                  <h4 class="text-lg font-bold text-text mb-2">Email Us</h4>
                  <p class="text-gray-600">audiopinesolutions@gmail.com</p>
                </div>
              </div>
            </div>
  
            <!-- Map -->
            <div class="rounded-xl overflow-hidden shadow-lg">
              <iframe 
                src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d3988.791592442001!2d36.78734762588713!3d-1.2998644486877873!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1sNgong%20Road%2C%20OLA%20Energies%20shop%20E5%2C%20Woodley%20Estate%2C%20Nairobi%20Area%2C%20Kenya%2001100!5e0!3m2!1sen!2ske!4v1743261915390!5m2!1sen!2ske"  
                class="w-full h-64 border-0"
                allowfullscreen
                loading="lazy">
              </iframe>
            </div>
  
            <!-- Social Links -->
            <div class="flex space-x-6 justify-center pt-8">
            <!-- Twitter -->
            <a href="#" class="text-primary hover:text-purple-700">
                <span class="sr-only">Twitter</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"/>
                </svg>
            </a>

            <!-- Facebook -->
            <a href="https://www.facebook.com/share/1EbqhtMZn7/" class="text-primary hover:text-purple-700">
                <span class="sr-only">Facebook</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd"/>
                </svg>
            </a>

            <!-- Instagram -->
            <a href="https://www.instagram.com/audiopinesolutions?igsh=Njd3cXg2ZHk1NGRs" class="text-primary hover:text-purple-700">
                <span class="sr-only">Instagram</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/>
                </svg>
            </a>

            <!-- TikTok -->
            <a href="https://vm.tiktok.com/ZMBPP1w3s/" class="text-primary hover:text-purple-700">
                <span class="sr-only">TikTok</span>
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                </svg>
            </a>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- END CONTACT SECTION -->
  </template> 