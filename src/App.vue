<script setup>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import Features from './components/Features.vue';
import Pricing from './components/Pricing.vue';
import Testimonials from './components/Testimonials.vue';
import Footer from './components/Footer.vue';
import Contact from './components/Contact.vue';
</script>

<template>
  <div class="overflow-x-hidden antialiased">
    <Header />
    <main>
      <Hero />
      <Features />
      <Pricing />
      <Testimonials />
      <Contact />
    </main>
    <Footer />
  </div>
</template>

<style scoped></style>
