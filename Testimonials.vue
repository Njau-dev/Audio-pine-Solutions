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
    avatar: "/img/mich.jpexg",
  },
]);
</script>

<template>
  <div class="container mx-auto p-4">
    <h2 class="text-2xl font-bold mt-10 mb-4 text-center text-gray-800">Customer Testimonials</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="testimonial in testimonials"
        :key="testimonial.name"
        class="bg-white p-6 rounded-lg shadow-lg flex flex-col items-center"
      >
        <img
          :src="testimonial.avatar"
          :alt="`Avatar of ${testimonial.name}`"
          class="w-24 h-24 rounded-full mb-4"
        />
        <h3 class="font-bold text-lg text-gray-900">{{ testimonial.name }}</h3>
        <p class="text-gray-600 italic text-center">"{{ testimonial.text }}"</p>
        <span class="text-sm text-gray-500 mt-2">- {{ testimonial.service }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Additional custom styles can be added here if necessary */
</style>
