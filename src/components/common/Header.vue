<template>
<header class="relative">
      <!-- Navigation -->
      <nav class="fixed top-0 left-0 right-0 z-50 bg-stone-800 shadow-md">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
          <div class="text-xl font-bold text-rose-600">Christine</div>
          <div class="hidden md:flex space-x-8">
            <a href="#home" class="text-green-700 hover:text-sky-800 transition duration-300 cursor-pointer">Home</a>
            <a href="#about" class="text-green-700 hover:text-sky-800 transition duration-300 cursor-pointer">About</a>
            <a href="#skills" class="text-green-700 hover:text-sky-800  transition duration-300 cursor-pointer">Skills</a>
            <a href="#projects" class="text-green-700 hover:text-sky-800  transition duration-300 cursor-pointer">Projects</a>
            <a href="#contact" class="text-green-700 hover:text-sky-800  transition duration-300 cursor-pointer">Contact</a>
          </div>
          <div class="md:hidden">
            <button @click="toggleMobileMenu" class="text-gray-700 cursor-pointer">
              <i class="fas fa-bars text-xl"></i>
            </button>
          </div>
        </div>

         <!-- Mobile Menu -->
        <div v-if="mobileMenuOpen" class="md:hidden bg-white shadow-lg absolute w-full">
          <div class="container mx-auto px-6 py-4 flex flex-col space-y-4">
            <a href="#home" @click="closeMobileMenu" class="text-gray-700 hover:text-indigo-600 transition duration-300 cursor-pointer">Home</a>
            <a href="#about" @click="closeMobileMenu" class="text-gray-700 hover:text-indigo-600 transition duration-300 cursor-pointer">About</a>
            <a href="#skills" @click="closeMobileMenu" class="text-gray-700 hover:text-indigo-600 transition duration-300 cursor-pointer">Skills</a>
            <a href="#projects" @click="closeMobileMenu" class="text-gray-700 hover:text-indigo-600 transition duration-300 cursor-pointer">Projects</a>
            <a href="#contact" @click="closeMobileMenu" class="text-gray-700 hover:text-indigo-600 transition duration-300 cursor-pointer">Contact</a>
          </div>
        </div>
      </nav>
        </header>
        </template>

<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from 'vue';
const mobileMenuOpen = ref(false);
const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
};
const closeMobileMenu = () => {
  mobileMenuOpen.value = false;
};

// Define the checkScrollPosition function
const checkScrollPosition = () => {
  // Example: You can add logic here if you want to handle scroll events
  // For now, it's just a placeholder to avoid errors
};

onMounted(() => {
  window.addEventListener('scroll', checkScrollPosition);
  checkScrollPosition();
});

onUnmounted(() => {
  window.removeEventListener('scroll', checkScrollPosition);
});
</script>
