<script setup>
import { ref } from 'vue';
import ThemeSwitcher from './ThemeSwitcher.vue';

const isMobileMenuOpen = ref(false);
</script>

<template>
  <header class="relative z-50 w-full h-24 bg-bg">
    <div class="container flex items-center justify-center h-full max-w-6xl px-8 mx-auto sm:justify-between xl:px-0">
      <!-- Logo -->
      <a href="/" class="relative flex items-center h-full font-black leading-none">
        <img src="/src/assets/images/logo.jpeg" alt="Logo" class="w-auto h-12" >
        <span class="ml-3 text-xl text-text">AudioPine <span class="text-primary">.</span></span>
      </a>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex items-center space-x-6 lg:space-x-8 text-text">
        <a href="#" class="font-bold duration-100  hover:text-primary">Home</a>
        <a href="#services" class="font-bold duration-100  hover:text-primary">Services</a>
        <a href="#pricing" class="font-bold duration-100  hover:text-primary">Pricing</a>
        <a href="#testimonials" class="font-bold duration-100  hover:text-primary">Testimonials</a>
        <a href="#contact" class="text-lg font-bold hover:text-primary">Contact</a>
        <div class="absolute left-0 flex-col items-center justify-center hidden w-full pb-8 mt-48 border-b border-border md:relative md:w-auto md:bg-transparent md:border-none md:mt-0 md:flex-row md:p-0 md:items-end md:flex md:justify-between">
          <ThemeSwitcher class="px-3 py-2 text-sm font-bold  z-30 cursor-pointer"/>
          <a href="#" class="px-5 py-3 text-sm font-bold text-primary z-30 bg-white rounded shadow-md hover:shadow-xl transition-all">
            Get Started
          </a>
          <svg class="absolute top-0 left-0 hidden w-screen max-w-3xl -mt-64 -ml-12 lg:block"
                    viewBox="0 0 818 815" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                    <defs>
                        <linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="c">
                            <stop stop-color="#E614F2" offset="0%" />
                            <stop stop-color="#FC3832" offset="100%" />
                        </linearGradient>
                        <linearGradient x1="0%" y1="0%" x2="100%" y2="100%" id="f">
                            <stop stop-color="#657DE9" offset="0%" />
                            <stop stop-color="#1C0FD7" offset="100%" />
                        </linearGradient>
                        <filter x="-4.7%" y="-3.3%" width="109.3%" height="109.3%" filterUnits="objectBoundingBox"
                            id="a">
                            <feOffset dy="8" in="SourceAlpha" result="shadowOffsetOuter1" />
                            <feGaussianBlur stdDeviation="8" in="shadowOffsetOuter1" result="shadowBlurOuter1" />
                            <feColorMatrix values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.15 0" in="shadowBlurOuter1" />
                        </filter>
                        <filter x="-4.7%" y="-3.3%" width="109.3%" height="109.3%" filterUnits="objectBoundingBox"
                            id="d">
                            <feOffset dy="8" in="SourceAlpha" result="shadowOffsetOuter1" />
                            <feGaussianBlur stdDeviation="8" in="shadowOffsetOuter1" result="shadowBlurOuter1" />
                            <feColorMatrix values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.2 0" in="shadowBlurOuter1" />
                        </filter>
                        <path
                            d="M160.52 108.243h497.445c17.83 0 24.296 1.856 30.814 5.342 6.519 3.486 11.635 8.602 15.12 15.12 3.487 6.52 5.344 12.985 5.344 30.815v497.445c0 17.83-1.857 24.296-5.343 30.814-3.486 6.519-8.602 11.635-15.12 15.12-6.52 3.487-12.985 5.344-30.815 5.344H160.52c-17.83 0-24.296-1.857-30.814-5.343-6.519-3.486-11.635-8.602-15.12-15.12-3.487-6.52-5.343-12.985-5.343-30.815V159.52c0-17.83 1.856-24.296 5.342-30.814 3.486-6.519 8.602-11.635 15.12-15.12 6.52-3.487 12.985-5.343 30.815-5.343z"
                            id="b" />
                        <path
                            d="M159.107 107.829H656.55c17.83 0 24.296 1.856 30.815 5.342 6.518 3.487 11.634 8.602 15.12 15.12 3.486 6.52 5.343 12.985 5.343 30.816V656.55c0 17.83-1.857 24.296-5.343 30.815-3.486 6.518-8.602 11.634-15.12 15.12-6.519 3.486-12.985 5.343-30.815 5.343H159.107c-17.83 0-24.297-1.857-30.815-5.343-6.519-3.486-11.634-8.602-15.12-15.12-3.487-6.519-5.343-12.985-5.343-30.815V159.107c0-17.83 1.856-24.297 5.342-30.815 3.487-6.519 8.602-11.634 15.12-15.12 6.52-3.487 12.985-5.343 30.816-5.343z"
                            id="e" />
                    </defs>
                    <g fill="none" fill-rule="evenodd" opacity=".9">
                        <g transform="rotate(65 416.452 409.167)">
                            <use fill="#000" filter="url(#a)" xlink:href="#b" />
                            <use fill="#6cb446" xlink:href="#b" />
                        </g>
                        <g transform="rotate(29 421.929 414.496)">
                            <use fill="#000" filter="url(#d)" xlink:href="#e" />
                            <use fill="#314d4e" xlink:href="#e" />
                        </g>
                    </g>
                </svg>
        </div>
      </nav>

      

      <!-- Mobile Navigation Button -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen"
        class="absolute top-0 right-0 z-50 block w-6 mt-8 mr-10 cursor-pointer select-none md:hidden sm:mt-10"
      >
        <span 
          :class="{'rotate-45 translate-y-1.5 bg-gray-500': isMobileMenuOpen}"
          class="block w-full h-1 mt-2 transition-all duration-200 bg-text rounded-full sm:mt-1"
        ></span>
        <span 
          :class="{
            '-rotate-45 -translate-y-1 bg-gray-500': isMobileMenuOpen,
            'mt-1': !isMobileMenuOpen
          }" 
          class="block w-full h-1 transition-all duration-200 bg-text rounded-full"
        ></span>
      </button>

      <!-- Mobile Navigation Menu -->
      <div 
        v-show="isMobileMenuOpen"
        class="fixed inset-0 z-40 mt-24 bg-bg border-t border-border md:hidden"
      >
        <div class="container px-8 mx-auto text-text">
          <div class="flex flex-col items-center py-6 space-y-4">
            <a href="#" class="text-lg font-bold hover:text-primary">Home</a>
            <a href="#features" class="text-lg font-bold hover:text-primary">Features</a>
            <a href="#pricing" class="text-lg font-bold hover:text-primary">Pricing</a>
            <a href="#testimonials" class="text-lg font-bold hover:text-primary">Testimonials</a>
            <a href="#contact" class="text-lg font-bold hover:text-primary">Contact</a>
            <div class="w-full pt-4 mt-4 border-t border-border">
              <ThemeSwitcher class="block mx-auto px-5 py-3 text-center text-text bg-bg rounded shadow-md cursor-pointer"/>
              <a href="#" class="block w-full px-5 py-3 mt-2 text-center text-white bg-primary rounded shadow-md">
                Get Started
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>