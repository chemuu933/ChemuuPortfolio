<template>
  <div id="home" class="relative pt-24 pb-16 md:pt-32 md:pb-24">
    <div class="absolute inset-0 overflow-hidden">
      <img
        :src="heroBackgroundUrl"
        alt="Tech Background"
        class="w-full h-full object-cover object-top"
      />
      <div
        class="absolute inset-0 bg-gradient-to-r from-slate-700/90 to-fuchsia-800/70"
      ></div>
    </div>
    <div
      class="container relative mx-auto px-6 flex flex-col md:flex-row items-center"
    >
      <div class="md:w-1/2 text-center md:text-left z-10 mb-10 md:mb-0">
        <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-4">
          Hi, I'm <span class="text-teal-300">Christine</span>
        </h1>
        <p class="text-xl md:text-2xl text-gray-200 mb-8">
          Crafting digital experiences with seamless frontend artistry and
          robust backend foundations.
        </p>
        <div
          class="flex flex-col sm:flex-row justify-center md:justify-start gap-4"
        >
          <a
            href="#projects"
            class="bg-slate-600 hover:bg-indigo-700 text-white px-6 py-3 rounded-lg font-medium transition duration-300 !rounded-button whitespace-nowrap cursor-pointer"
            >View My Work</a
          >
          <a
            href="#contact"
            class="bg-transparent border-2 border-white text-white hover:bg-white hover:text-indigo-600 px-6 py-3 rounded-lg font-medium transition duration-300 !rounded-button whitespace-nowrap cursor-pointer"
            >Contact Me</a
          >
        </div>
      </div>
      <div class="md:w-1/2 flex justify-center md:justify-end">
        <img
          :src="profileImageUrl"
          alt="Christine - IT Student"
          class="w-64 h-64 md:w-80 md:h-80 rounded-full border-4 border-white shadow-xl object-cover object-top"
        />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
// @ts-ignore
import profileImageUrl from '../../assets/chemuu1.jpeg'

const heroBackgroundUrl = 'https://readdy.ai/api/search-image?query=modern%20tech%20abstract%20background%20with%20blue%20and%20purple%20gradient%2C%20digital%20technology%20concept%2C%20high%20resolution%2C%20professional%2C%20clean%20design%2C%20suitable%20for%20web%20header&width=1440&height=800&seq=1&orientation=landscape';

</script>