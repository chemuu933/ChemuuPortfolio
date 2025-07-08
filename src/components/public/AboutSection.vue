<template>
  <section id="about" class="py-20 bg-cyan-200">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
          About Me
        </h2>
        <div class="w-20 h-1 bg-indigo-600 mx-auto"></div>
      </div>
      <div class="flex flex-col md:flex-row items-center">
        <div class="md:w-1/2 mb-10 md:mb-0">
          <img
            :src="aboutImageUrl"
            alt="Christine working on code"
            class="rounded-lg shadow-xl w-full h-auto max-w-md mx-auto object-cover object-top"
          />
        </div>
        <div class="md:w-1/2 md:pl-12">
          <h3 class="text-2xl font-semibold text-gray-800 mb-4">Who I Am</h3>
          <p class="text-stone-800 mb-6 leading-relaxed">
            I'm Christine, an ambitious IT professional passionate about creating
            meaningful digital experiences through code. My journey in
            technology began with a curiosity about how websites work, which led
            me to pursue formal education in Information Technology.
          </p>
          <p class="text-stone-800 mb-6 leading-relaxed">
            Currently focused on frontend development, I enjoy the challenge
            of building applications from the ground up. My experience spans
            front-end technologies like HTML, CSS, JavaScript, React, and
            Vue.js, as well as back-end work with Node.js and Express.js.
          </p>
          <p class="text-stone-800 mb-8 leading-relaxed">
            When I'm not coding, I'm expanding my knowledge through online
            courses, contributing to open-source projects, and staying updated
            with the latest tech trends. I believe in continuous learning and
            pushing the boundaries of what's possible with technology.
          </p>
          <div class="flex flex-wrap gap-4">
            <div class="flex items-center bg-white px-4 py-2 rounded-lg shadow">
              <i class="fas fa-graduation-cap text-indigo-600 mr-2"></i>
              <span class="text-purple-700">IT professional</span>
            </div>
            <div class="flex items-center bg-white px-4 py-2 rounded-lg shadow">
              <i class="fas fa-code text-indigo-600 mr-2"></i>
              <span class="text-purple-700">Frontend Developer</span>
            </div>
            <div class="flex items-center bg-white px-4 py-2 rounded-lg shadow">
              <i class="fas fa-laptop-code text-indigo-600 mr-2"></i>
              <span class="text-purple-700">Problem Solver</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang="ts" setup>
const aboutImageUrl = 'https://readdy.ai/api/search-image?query=young%20woman%20coding%20on%20laptop%20in%20modern%20workspace%2C%20focused%20on%20screen%20showing%20code%2C%20professional%20setting%2C%20soft%20natural%20lighting%2C%20high%20quality%2C%20tech%20environment&width=600&height=400&seq=3&orientation=landscape';
</script>