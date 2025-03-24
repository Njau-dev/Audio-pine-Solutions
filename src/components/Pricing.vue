<script setup>
import { ref } from "vue";

const packages = ref({
  "Car Audio Packages": [
    {
      name: "Basic Car Audio Package",
      features: [
        "Installation of entry-level car audio system",
        "Basic sound tuning",
        "1-year warranty"
      ],
      price: "KSh 5,000–10,000"
    },
    {
      name: "Standard Car Audio Package",
      features: [
        "Installation of mid-range car audio system (e.g., 2 speakers + amplifier)",
        "Enhanced sound tuning",
        "2-year warranty"
      ],
      price: "KSh 15,000–25,000"
    },
    {
      name: "Premium Car Audio Package",
      features: [
        "Installation of high-end car audio system (e.g., multiple speakers, amplifier, subwoofer)",
        "Advanced sound tuning",
        "Noise isolation",
        "3-year warranty"
      ],
      price: "KSh 30,000–50,000"
    }
  ],
  "Web Development Packages": [
    {
      name: "Basic Web Package",
      features: [
        "Basic website setup (up to 5 pages)",
        "Responsive design",
        "Basic SEO optimization"
      ],
      price: "KSh 10,000–20,000"
    },
    {
      name: "Advanced Web Package",
      features: [
        "Custom website design (up to 10 pages)",
        "CMS integration",
        "SEO and performance optimization"
      ],
      price: "KSh 30,000–100,000"
    }
  ],
  "Cyber Security Packages": [
    {
      name: "Cyber Security Basic",
      features: [
        "Vulnerability scanning",
        "Basic firewall setup",
        "Security recommendations"
      ],
      price: "KSh 15,000–30,000"
    },
    {
      name: "Cyber Security Advanced",
      features: [
        "Penetration testing",
        "Advanced threat detection",
        "24/7 security monitoring"
      ],
      price: "KSh 50,000–100,000"
    }
  ]
});
</script>

<template>
  <div class="container mx-auto p-4">
    <h2 class="text-2xl font-bold mb-4 text-center">Service Packages</h2>
    <div v-for="(category, categoryName) in packages" :key="categoryName" class="mb-6">
      <h3 class="text-xl font-semibold mb-4 text-center">{{ categoryName }}</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div v-for="(packageItem, index) in category" :key="index" class="bg-white shadow-lg rounded-lg p-6 border border-gray-200">
          <h4 class="text-lg font-bold mb-2">{{ packageItem.name }}</h4>
          <ul class="list-disc list-inside mb-4">
            <li v-for="(feature, featureIndex) in packageItem.features" :key="featureIndex">
              {{ feature }}
            </li>
          </ul>
          <p class="text-center font-semibold text-gray-700">Price: {{ packageItem.price }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 1200px;
}
</style>