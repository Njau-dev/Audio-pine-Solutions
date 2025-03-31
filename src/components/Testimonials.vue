
<script>
import SteveImg from '../assets/images/steve.jpeg';
import jon  from '../assets/images/jon.jpeg';
import dow from '../assets/images/dow.jpeg';
import Jane from '../assets/images/jane.jpeg';
export default {
  name: "Testimonials",
  data() {
    return {
      testimonials: [
        {
          quote: "Working with this web development team was a game-changer for my business. They created a stunning, user-friendly website that helped me attract more customers and grow online.",
          name: "Sandra Walton",
          position: "CEO SomeCompany",
          image: Jane,
        },
        {
          quote: "I was skeptical about upgrading my stock speakers, but the difference is night and day. The bass is powerful, and the clarity is insane!"
,
          name: "Kenny Jones",
          position: "Driver",
          image: SteveImg, 
        },
        {
          quote: "As a cybersecurity professional, I’ve helped businesses recover from attacks and strengthen their defenses. Seeing clients regain confidence in their security drives my passion for this field.",
          name: "Mike Smith",
          position: "CEO SomeCompany",
          image: dow,
         },
        {
          quote: "Joining this audio club was an amazing experience! The sound quality, engaging discussions, and expert insights have truly enhanced my learning and entertainment.",
          name: "Molly Sanchez",
          position: "CEO SomeCompany",
          image: jon, 
         }
      ]
    };
  },
  computed: {
    // Split testimonials into two columns
    leftTestimonials() {
      return this.testimonials.slice(0, Math.ceil(this.testimonials.length / 2));
    },
    rightTestimonials() {
      return this.testimonials.slice(Math.ceil(this.testimonials.length / 2));
    }
  }
};
</script>


<template>
  <!-- Start Testimonials -->
  <div
    id="testimonials"
    class="flex items-center justify-center w-full px-8 py-10 border-t border-border md:py-16 lg:py-24 xl:py-40 xl:px-0 bg-bg"
  >
    <div class="max-w-6xl mx-auto">
      <div class="flex-col items-center">
        <div
          class="flex flex-col items-center justify-center w-full h-full max-w-2xl pr-8 mx-auto text-center"
        >
          <p class="my-5 text-xl font-medium tracking-tight text-primary uppercase">
            Our customers love our product
          </p>
          <h2
            class="text-4xl font-extrabold leading-10 tracking-tight text-text sm:text-5xl sm:leading-none md:text-6xl lg:text-5xl xl:text-6xl"
          >
            Testimonials
          </h2>
          <p class="my-6 text-xl text-secondary">
            Don't just take our word for it, read from our extensive list of case studies and customer testimonials.
          </p>
        </div>
        <div
          class="flex flex-col items-center justify-center max-w-2xl py-8 mx-auto xl:flex-row xl:max-w-full"
        >
          <!-- Left Column -->
          <div class="w-full xl:w-1/2 xl:pr-8">
            <blockquote
              v-for="(testimonial, index) in leftTestimonials"
              :key="index"
              class="flex flex-col-reverse items-center justify-between w-full p-6 text-center transition-all duration-200 bg-lightshade rounded-lg md:flex-row md:text-left hover:bg-bg hover:shadow hover:border border-border ease"
              :class="{ 'my-16': index !== 0 }"
            >
              <div class="flex flex-col pr-8">
                <div class="relative pl-12">
                  <svg
                    class="absolute left-0 w-10 h-10 text-primary fill-current"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 100 125"
                  >
                    <path
                      d="M30.7 42c0 6.1 12.6 7 12.6 22 0 11-7.9 19.2-18.9 19.2C12.7 83.1 5 72.6 5 61.5c0-19.2 18-44.6 29.2-44.6 2.8 0 7.9 2 7.9 5.4S30.7 31.6 30.7 42zM82.4 42c0 6.1 12.6 7 12.6 22 0 11-7.9 19.2-18.9 19.2-11.8 0-19.5-10.5-19.5-21.6 0-19.2 18-44.6 29.2-44.6 2.8 0 7.9 2 7.9 5.4S82.4 31.6 82.4 42z"
                    />
                  </svg>
                  <p class="mt-2 text-base text-secondary">{{ testimonial.quote }}</p>
                </div>
                <h3 class="pl-12 mt-3 text-xl font-medium leading-5 text-text truncate">
                  {{ testimonial.name }}
                  <span class="mt-1 text-sm leading-5 text-secondary truncate">
                    - {{ testimonial.position }}
                  </span>
                </h3>
              </div>
              <img :src="testimonial.image" class="flex-shrink objetct w-24 h-24 mb-5 rounded-full md:mb-0" :alt="testimonial.name" />


            </blockquote>
          </div>
          
          <!-- Right Column -->
          <div class="w-full xl:w-1/2 xl:pl-8">
            <blockquote
              v-for="(testimonial, index) in rightTestimonials"
              :key="index"
              class="flex flex-col-reverse items-center justify-between w-full p-6 text-center transition-all duration-200 bg-lightshade rounded-lg md:flex-row md:text-left hover:bg-bg hover:shadow hover:border border-border ease"
              :class="{ 'my-16': index !== 0 }"
            >
              <div class="flex flex-col pr-10">
                <div class="relative pl-12">
                  <svg
                    class="absolute left-0 w-10 h-10 text-primary fill-current"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 100 125"
                  >
                    <path
                      d="M30.7 42c0 6.1 12.6 7 12.6 22 0 11-7.9 19.2-18.9 19.2C12.7 83.1 5 72.6 5 61.5c0-19.2 18-44.6 29.2-44.6 2.8 0 7.9 2 7.9 5.4S30.7 31.6 30.7 42zM82.4 42c0 6.1 12.6 7 12.6 22 0 11-7.9 19.2-18.9 19.2-11.8 0-19.5-10.5-19.5-21.6 0-19.2 18-44.6 29.2-44.6 2.8 0 7.9 2 7.9 5.4S82.4 31.6 82.4 42z"
                    />
                  </svg>
                  <p class="mt-2 text-base text-secondary">{{ testimonial.quote }}</p>
                </div>
                <h3 class="pl-12 mt-3 text-xl font-medium leading-5 text-text truncate">
                  {{ testimonial.name }}
                  <span class="mt-1 text-sm leading-5 text-secondary truncate">
                    - {{ testimonial.position }}
                  </span>
                </h3>
              </div>
              <img
                class="flex-shrink-0 object-cover w-24 h-24 mb-5 bg-gray-300 rounded-full md:mb-0"
                :src="testimonial.image"
                :alt="testimonial.name"
              />
            </blockquote>
          </div>

        </div>
      </div>
    </div>
  </div>
  <!-- End Testimonials -->
</template>