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
    <div class="overflow-x-auto">
      <div v-for="(category, categoryName) in packages" :key="categoryName" class="mb-6">
        <h3 class="text-xl font-semibold mb-2 text-center">{{ categoryName }}</h3>
        <table class="min-w-full border border-gray-300">
          <thead>
            <tr class="bg-gray-200">
              <th class="border border-gray-300 px-4 py-2">Package</th>
              <th class="border border-gray-300 px-4 py-2">Features</th>
              <th class="border border-gray-300 px-4 py-2">Price Range</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(packageItem, index) in category" :key="index" class="bg-white hover:bg-gray-100">
              <td class="border border-gray-300 px-4 py-2 font-bold">{{ packageItem.name }}</td>
              <td class="border border-gray-300 px-4 py-2">
                <ul class="list-disc ml-4">
                  <li v-for="(feature, featureIndex) in packageItem.features" :key="featureIndex">
                    {{ feature }}
                  </li>
                </ul>
              </td>
              <td class="border border-gray-300 px-4 py-2 text-center">{{ packageItem.price }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
