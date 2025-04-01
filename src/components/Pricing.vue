 
  <script setup>
  import { ref } from "vue";
  
  // Example dynamic data. You can rename, reorder, or add more packages.
  // The second item in each category is shown as "Pro Pricing" with the 
  // "Most Popular" label if `mostPopular: true`.
  const packages = ref({
    "Car Audio Packages": [
      {
        name: "Basic Car Audio Package",
        price: "5k–10k",
        description: "In our basic plan you can take advantage of all these features below.",
        features: [
          "Installation of entry-level car audio system",
          "Basic sound tuning",
          "1-year warranty"
        ]
      },
      {
        name: "Standard Car Audio Package",
        price: "15k–25k",
        description: "Our most popular package is the Pro Plan which gives you access to the following:",
        features: [
          "Installation of mid-range car audio system (e.g., 2 speakers + amplifier)",
          "Enhanced sound tuning",
          "2-year warranty"
        ],
        mostPopular: true
      },
      {
        name: "Premium Car Audio Package",
        price: "30k–50k",
        description: "With our premium plan you can take advantage of all the following features:",
        features: [
          "Installation of high-end car audio system.",
          "Advanced sound tuning",
          "Noise isolation"
        ]
      }
    ],
    "Web Development Packages": [
      {
        name: "Basic Web Package",
        price: "10k–20k",
        description: "In our basic plan you can take advantage of all these features below.",
        features: [
          "Basic website setup (up to 5 pages)",
          "Responsive design",
          "Basic SEO optimization"
        ]
      },
      {
        name: "Advanced Web Package",
        price: "30k–100k",
        description: "Our most popular package is the Pro Plan which gives you access to the following:",
        features: [
          "Custom website design (up to 10 pages)",
          "Dedicated support and maintenance",
          "SEO and performance optimization"
        ],
        mostPopular: true
      },
      {
        name: "Premium Web Package",
        price: "150k+",
        description: "The ultimate web solution for businesses that need advanced features and scalability.",
        features: [
            "Custom website design with unlimited pages",
            "E-commerce functionality",
            "Advanced SEO and performance optimization",
            "Custom dashboard and API integration",
        ]
    }
    ],
    "Cyber Security Packages": [
      {
        name: "Cyber Security Basic",
        price: "15k–30k",
        description: "In our basic plan you can take advantage of all these features below.",
        features: [
          "Vulnerability scanning",
          "Basic firewall setup",
          "Security recommendations"
        ]
      },
      {
        name: "Cyber Security Advanced",
        price: "50k–100k",
        description: "Our most popular package is the Pro Plan which gives you access to the following:",
        features: [
          "Penetration testing",
          "Advanced threat detection",
          "24/7 security monitoring"
        ],
        mostPopular: true
      },
      {
        name: "Cyber Security Elite",
        price: "150k+",
        description: "With our premium plan you can take advantage of all the following features:",
        features: [
          "Comprehensive penetration testing",
          "AI-driven threat detection",
          "Dedicated security expert"
        ]
      }
    ]
  });
  </script>
  


<template>
    <!-- Pricing Section -->
    <div class="relative px-8 py-10 bg-bg border-t border-border md:py-16 lg:py-24 xl:py-40 xl:px-0">
      <div id="pricing" class="container flex flex-col items-center h-full max-w-6xl mx-auto">
        <!-- Main Section Title -->
        <h2 class="my-5 text-xl font-medium tracking-tight text-primary uppercase">
          Our Pricing
        </h2>
        <h3
          class="w-full max-w-2xl px-5 mt-2 text-2xl font-black leading-tight text-center text-text sm:mt-0 sm:px-0 sm:text-6xl md:px-0"
        >
          Simple, Transparent Pricing for Everyone
        </h3>
  
        <!-- Loop through each category of packages -->
        <div
          v-for="(plans, categoryName) in packages"
          :key="categoryName"
          class="w-full mt-10"
        >
          <!-- Category Heading -->
          <h4 class="mb-6 text-2xl font-bold text-center text-primary">
            {{ categoryName }}
          </h4>
  
          <!-- Exact container as in your original code -->
          <div class="max-w-full mx-auto md:max-w-6xl sm:px-8">
            <div class="relative flex flex-col items-center sm:flex-row">
              <!-- 1) Basic Pricing Column (index 0) -->
              <div
                v-if="plans[0]"
                class="relative z-0 w-11/12 max-w-sm my-8 border border-border hover:scale-105 transition-all rounded-lg sm:w-3/5 lg:w-1/3 sm:my-5 md:-mr-4"
              >
                <div class="overflow-hidden text-text bg-bg rounded-lg shadow-sm">
                  <div
                    class="block max-w-sm px-8 mx-auto mt-5 text-sm text-left text-text sm:text-md lg:px-6"
                  >
                    <h3
                      class="p-3 text-lg font-bold tracking-wide text-center uppercase"
                    >
                      {{ plans[0].name }}
                      </h3>
                    <h4
                      class="flex items-center justify-center pb-6 pt-1 text-2xl font-bold text-center text-text"
                    >
                      <span
                        class="mr-1 -ml-2 text-lg text-primary font-medium"
                        >Kshs</span
                      >
                      {{ plans[0].price }}
                    </h4>
                    <!-- Use the package's description exactly where you had it -->
                    <p class="text-sm text-secondary">
                      {{ plans[0].description }}
                    </p>
                  </div>
  
                  <div class="flex flex-wrap px-6 mt-8">
                    <ul>
                      <li
                        v-for="(feature, index) in plans[0].features"
                        :key="index"
                        class="flex items-center"
                      >
                        <div
                          class="p-2 text-primary rounded-full fill-current"
                        >
                          <svg
                            class="w-6 h-6 align-middle"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                          >
                            <path
                              d="M22 11.08V12a10 10 0 1 1-5.93-9.14"
                            />
                            <polyline points="22 4 12 14.01 9 11.01" />
                          </svg>
                        </div>
                        <span
                          class="ml-3 text-lg text-secondary font-medium"
                          >{{ feature }}</span
                        >
                      </li>
                    </ul>
                  </div>
                  <div class="flex items-center p-8 uppercase">
                    <a
                      href="#_"
                      class="block w-full px-6 py-4 mt-3 text-lg font-semibold text-center text-white bg-primary rounded shadow-sm hover:bg-company"
                    >
                      Select This Plan
                    </a>
                  </div>
                </div>
              </div>
  
              <!-- 2) Pro Pricing Column (index 1) -->
              <div
                v-if="plans[1]"
                class="relative z-10 w-full max-w-md my-8 bg-bg border border-border hover:scale-105 transition-all rounded-lg shadow-lg sm:w-2/3 lg:w-1/3 sm:my-5"
              >
                <!-- "Most Popular" label appears only if the plan data says so -->
                <div
                  v-if="plans[1].mostPopular"
                  class="py-4 text-sm font-semibold leading-none tracking-wide text-center text-white uppercase bg-primary rounded-t"
                >
                  Most Popular
                </div>
                <div
                  class="block max-w-sm px-8 mx-auto mt-5 text-sm text-left text-text sm:text-md lg:px-6"
                >
                  <h3
                    class="p-3 pb-1 text-lg font-bold tracking-wide text-center uppercase"
                  >
                    {{ plans[1].name }}
                  </h3>
                  <!-- Notice Pro has text-5xl for the price -->
                  <h4
                    class="flex items-center justify-center pb-6 pt-2 text-3xl font-bold text-center text-text"
                  >
                    <span
                      class="mr-2 -ml-2 text-lg text-primary font-medium"
                      >Kshs </span
                    >
                    {{ plans[1].price }}
                  </h4>
                  <p class="text-sm text-secondary">
                    {{ plans[1].description }}
                  </p>
                </div>
                <div class="flex justify-start pl-12 mt-8 sm:justify-start">
                  <ul>
                    <li
                      v-for="(feature, index) in plans[1].features"
                      :key="index"
                      class="flex items-center"
                    >
                      <div
                        class="p-2 text-primary rounded-full fill-current"
                      >
                        <svg
                          class="w-6 h-6 align-middle"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        >
                          <path
                            d="M22 11.08V12a10 10 0 1 1-5.93-9.14"
                          />
                          <polyline
                            points="22 4 12 14.01 9 11.01"
                          />
                        </svg>
                      </div>
                      <span
                        class="ml-3 text-lg text-secondary font-medium"
                        >{{ feature }}</span
                      >
                    </li>
                  </ul>
                </div>
                <div class="flex items-center p-8 uppercase">
                  <a
                    href="#_"
                    class="block w-full px-6 py-4 mt-3 text-lg font-semibold text-center text-white bg-primary rounded shadow-sm hover:bg-company"
                  >
                    Select This Plan
                  </a>
                </div>
              </div>
  
              <!-- 3) Premium Pricing Column (index 2) -->
              <div
                v-if="plans[2]"
                class="relative z-0 w-11/12 max-w-sm my-8 border border-border hover:scale-105 transition-all rounded-lg shadow-lg sm:w-3/5 lg:w-1/3 sm:my-5 md:-ml-4"
              >
                <div class="overflow-hidden text-text bg-bg rounded-lg shadow-lg">
                  <div
                    class="block max-w-sm px-8 mx-auto mt-5 text-sm text-left text-text sm:text-md lg:px-8"
                  >
                    <h3
                      class="p-3 pb-1 text-lg font-bold tracking-wide text-center uppercase"
                    >
                      {{ plans[2].name }}
                      </h3>
                    <h4
                      class="flex items-center justify-center pb-6 pt-1 text-2xl font-bold text-center text-text"
                    >
                      <span
                        class="mr-1 -ml-2 text-lg text-primary font-medium"
                        >Kshs</span
                      >
                      {{ plans[2].price }}
                    </h4>
                    <p class="pl-2 text-sm text-secondary">
                      {{ plans[2].description }}
                    </p>
                  </div>
                  <div class="flex flex-wrap px-8 mt-8">
                    <ul>
                      <li
                        v-for="(feature, index) in plans[2].features"
                        :key="index"
                        class="flex items-center"
                      >
                        <div
                          class="p-2 text-primary rounded-full fill-current"
                        >
                          <svg
                            class="w-6 h-6 align-middle"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                          >
                            <path
                              d="M22 11.08V12a10 10 0 1 1-5.93-9.14"
                            />
                            <polyline
                              points="22 4 12 14.01 9 11.01"
                            />
                          </svg>
                        </div>
                        <span
                          class="ml-3 text-lg text-secondary font-medium"
                          >{{ feature }}</span
                        >
                      </li>
                    </ul>
                  </div>
                  <div class="flex items-center p-8 uppercase">
                    <a
                      href="#_"
                      class="block w-full px-6 py-4 mt-3 text-lg font-semibold text-center text-white bg-primary rounded shadow-sm hover:bg-company"
                    >
                      Select This Plan
                    </a>
                  </div>
                </div>
              </div>
              <!-- End Premium Pricing -->
            </div>
          </div>
          <!-- End row of 3 cards -->
        </div>
        <!-- End loop of categories -->
      </div>
    </div>
    <!-- End Pricing Section -->
  </template>
 