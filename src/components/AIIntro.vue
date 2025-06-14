<template>
  <div class="relative overflow-hidden">
    <!-- Animated Background with Three Circles -->
    <div class="absolute inset-0 -z-10 flex items-center justify-center">
      <div class="w-[600px] h-[600px] bg-gray-400 opacity-30 rounded-full animate-pulse"></div>
      <div class="w-[400px] h-[400px] bg-white opacity-20 rounded-full animate-ping absolute top-20 left-40"></div>
      <div class="w-[300px] h-[300px] bg-green-300 opacity-10 rounded-full animate-bounce absolute bottom-10 right-20"></div>
    </div>

    <!-- Cartoon Characters for Agentic AI in Four Corners with Transparency -->
    <div class="absolute bottom-5 left-5 z-0 opacity-50">
      <img src="/src/assets/images/106.jpg" alt="Cartoon teaching Agentic AI" class="w-32 h-auto rounded-full border-4 border-white shadow-lg" />
    </div>
    <div class="absolute bottom-5 right-5 z-0 opacity-50">
      <img src="/src/assets/images/106.jpg" alt="Cartoon teaching Agentic AI" class="w-32 h-auto rounded-full border-4 border-white shadow-lg" />
    </div>
    <div class="absolute top-5 left-5 z-0 opacity-50">
      <img src="/src/assets/images/106.jpg" alt="Cartoon teaching Agentic AI" class="w-32 h-auto rounded-full border-4 border-white shadow-lg" />
    </div>
    <div class="absolute top-5 right-5 z-0 opacity-50">
      <img src="/src/assets/images/106.jpg" alt="Cartoon teaching Agentic AI" class="w-32 h-auto rounded-full border-4 border-white shadow-lg" />
    </div>

    <!-- Content -->
    <div class="p-6 text-gray-900 mx-4 md:mx-12 lg:mx-20">
      <h1 class="text-3xl font-bold mb-8 text-center">AI Transformation Plan for Audio Pine Solutions</h1>
      <div class="grid gap-12 md:grid-cols-2 lg:grid-cols-3">
        <section
          v-for="(section, index) in sections"
          :key="index"
          class="bg-white shadow rounded-xl p-6"
          :class="{ 'col-span-full': section.full }"
        >
          <h2 class="text-2xl font-bold mb-4">{{ section.title }}</h2>
          <div v-if="section.contentType === 'list'">
            <div v-for="(item, idx) in section.items" :key="idx" class="mb-6">
              <h3 v-if="item.heading" class="text-xl font-semibold" :class="item.color">{{ item.heading }}</h3>
              <ul class="list-disc ml-6">
                <li v-for="(point, pIdx) in item.points" :key="pIdx" v-html="point"></li>
              </ul>
            </div>
          </div>
          <div v-else-if="section.contentType === 'paragraphs'">
            <div v-for="(item, idx) in section.items" :key="idx" class="mb-4">
              <h3 class="text-lg font-semibold">{{ item.heading }}</h3>
              <p>{{ item.description }}</p>
            </div>
          </div>
          <ul v-else-if="section.contentType === 'bullets'" class="list-disc ml-6">
            <li v-for="(point, idx) in section.points" :key="idx" v-html="point"></li>
          </ul>
        </section>
      </div>
    </div>
  </div>
</template>

<script setup>
const sections = [
  {
    title: 'AI-Enhanced Services',
    contentType: 'list',
    items: [
      {
        heading: 'Car Audio Installation',
        color: 'text-blue-600',
        points: [
          '<strong>AI-Powered Sound Tuning:</strong> Uses DSPs like Audison, JL Audio with TensorFlow to optimize sound in real-time.',
          '<strong>Smart Diagnostics:</strong> Predictive maintenance via OBD2 and AutoPi analytics.'
        ]
      },
      {
        heading: 'Cybersecurity',
        color: 'text-red-600',
        points: [
          '<strong>AI-Powered Threat Detection:</strong> Tools like Darktrace, Wazuh with ML models for real-time defense.',
          '<strong>AI-Assisted Vulnerability Scanning:</strong> Integrating OpenVAS with AI dashboards for risk analysis.'
        ]
      },
      {
        heading: 'Software & Web Development',
        color: 'text-gray-700',
        points: [
          '<strong>AI-Powered UX/UI:</strong> Use Uizard, Galileo AI, and Figma plugins to automate wireframing and design.',
          '<strong>AI Chatbots & Recommendation Engines:</strong> Powered by Dialogflow, LangChain, and OpenAI APIs.'
        ]
      }
    ]
  },
  {
    title: 'New AI-Based Services',
    contentType: 'paragraphs',
    items: [
      {
        heading: 'Agentic AI Training',
        description: 'Train teams in autonomous agents using tools like LangChain, Auto-GPT, and BabyAGI. Delivery via workshops, e-learning, and consulting.'
      },
      {
        heading: 'AI Strategy Consulting',
        description: 'We guide businesses in AI integration using tools like Miro, ChatGPT, and Tableau to create strategic roadmaps and validate use-cases.'
      },
      {
        heading: 'Custom AI Solutions',
        description: 'Build chatbots, voice assistants, and analytics tools with platforms like Coqui AI, Whisper, PyCaret, and Rasa. Delivered through custom deployments.'
      }
    ]
  },
  {
    title: 'Tools & Resources',
    contentType: 'bullets',
    points: [
      '<strong>Learning Platforms:</strong> Coursera, FastAI, DeepLearning.ai',
      '<strong>Cloud:</strong> Google AI, Azure, AWS SageMaker, Hugging Face',
      '<strong>Frameworks:</strong> LangChain, Auto-GPT, MetaGPT, PyCaret',
      '<strong>Community:</strong> OpenAI Forums, AI Kenya, HF Spaces'
    ]
  }
];
</script>

<style scoped>
section {
  transition: all 0.3s ease;
}
section:hover {
  transform: scale(1.01);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}
</style>

 