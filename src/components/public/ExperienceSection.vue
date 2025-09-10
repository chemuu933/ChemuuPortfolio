<template>
  <section class="py-20 bg-pink-100">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-rose-800 mb-4">
          My Journey
        </h2>
        <div class="w-20 h-1 bg-pink-500 mx-auto"></div>
        <p class="text-rose-600 mt-4 max-w-2xl mx-auto">
          A timeline of my educational and professional experiences in the tech
          world.
        </p>
      </div>

      <div class="relative">
        <!-- Timeline Line -->
        <div
          class="hidden md:block absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-pink-300"
        ></div>

        <div class="space-y-12">
          <div
            v-for="(item, index) in timeline"
            :key="index"
            class="flex flex-col md:flex-row items-center"
          >
            <div
              :class="`md:w-1/2 ${
                index % 2 === 0
                  ? 'md:pr-12 md:text-right'
                  : 'md:pl-12 md:order-last'
              }`"
            >
              <div class="bg-pink-50 p-6 rounded-xl shadow-md border border-pink-200">
                <div class="text-pink-600 text-sm font-semibold mb-1">
                  {{ item.date }}
                </div>
                <h3 class="text-xl font-bold text-purple-800 mb-2">
                  {{ item.title }}
                </h3>
                <p class="text-purple-600">{{ item.description }}</p>
              </div>
            </div>

            <div
              class="hidden md:flex items-center justify-center w-12 h-12 rounded-full bg-gradient-to-r from-pink-500 to-rose-500 text-white relative z-10 my-4 md:my-0 shadow-lg"
            >
              <i :class="`fas ${item.icon}`"></i>
            </div>

            <div class="md:w-1/2"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ExperienceSection",
  data() {
    return {
      timeline: [
        {
          date: "2025- Present",
          title: "Frontend Developer",
          description: "Building modern web applications using Vue.js and other technologies.",
          icon: "fa-laptop-code"
        },
        {
          date: "2025 - 2026  ",
          title: "Intern Developer",
          description: "Worked on various projects and gained valuable experience in software development.",
          icon: "fa-briefcase"
        },
        {
          date: "2023 - 2025",
          title: "Diploma in Information Technology",
          description: "Studied information technology at  kabarak University and learned the fundamentals of programming.",
          icon: "fa-graduation-cap"
        }
      ]
    };
  }
};
</script>