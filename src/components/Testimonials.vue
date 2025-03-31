<script setup>
import { ref } from "vue";

const testimonials = ref([
  {
    name: "John Doe",
    text: "The car audio package transformed my driving experience!",
    service: "Car Audio Packages",
    avatar: "/img/Do.jpeg",
  },
  {
    name: "Jane Smith",
    text: "Highly professional web development services. My site looks amazing!",
    service: "Web Development Packages",
    avatar: "/img/jane.jpeg",
  },
  {
    name: "Alice Johnson",
    text: "The cyber security audit was a game-changer for my business security.",
    service: "Cyber Security Packages",
    avatar: "/img/emile.jpeg",
  },
  {
    name: "Bob Brown",
    text: "Exceptional customer support and attention to detail.",
    service: "Car Audio Packages",
    avatar: "/img/mins.jpeg",
  },
  {
    name: "Emily Davis",
    text: "The team delivered outstanding results ahead of schedule.",
    service: "Web Development Packages",
    avatar: "/img/emi.jpeg",
  },
  {
    name: "Michael Wilson",
    text: "Their expertise in cyber security is unparalleled.",
    service: "Cyber Security Packages",
    avatar: "/img/mich.jpeg",
  },
]);
</script>

<template>
  <div class="bg-gray-900 py-12 px-4">
    <h2 class="text-4xl font-extrabold text-white text-center mb-10">🌟 What Our Clients Say</h2>
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <div
        v-for="testimonial in testimonials"
        :key="testimonial.name"
        class="bg-white/10 backdrop-blur-md p-6 rounded-2xl shadow-xl flex flex-col items-center text-center transform transition duration-300 hover:scale-105 hover:shadow-2xl border border-white/20"
      >
        <img
          :src="testimonial.avatar"
          :alt="`Avatar of ${testimonial.name}`"
          class="w-24 h-24 rounded-full border-4 border-blue-400 shadow-md mb-4"
        />
        <h3 class="font-semibold text-lg text-white">{{ testimonial.name }}</h3>
        <p class="text-gray-300 italic text-sm mt-2">"{{ testimonial.text }}"</p>
        <span class="text-xs text-blue-300 mt-3 font-medium uppercase tracking-wide">{{ testimonial.service }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Soft glowing effect on hover */
div:hover img {
  filter: drop-shadow(0 0 10px rgba(59, 130, 246, 0.5));
}
</style>
