<template>
     <footer class="bg-gradient-to-r from-pink-900 to-purple-900 text-white py-12">
      <div class="container mx-auto px-6">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="mb-6 md:mb-0">
            <div class="text-2xl font-bold mb-2 text-pink-200">Christine</div>
            <p class="text-purple-300"> Frontend Developer</p>
          </div>
          
          <div class="flex flex-wrap justify-center gap-6 mb-6 md:mb-0">
            <a href="#home" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">Home</a>
            <a href="#about" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">About</a>
            <a href="#skills" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">Skills</a>
            <a href="#projects" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">Projects</a>
            <a href="#contact" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">Contact</a>
          </div>
          
          <div class="flex space-x-4">
            <a href="https://github.com/" target="_blank" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">
              <i class="fab fa-github text-xl"></i>
            </a>
            <a href="https://linkedin.com/" target="_blank" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">
              <i class="fab fa-linkedin-in text-xl"></i>
            </a>
            <a href="https://twitter.com/" target="_blank" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">
              <i class="fab fa-twitter text-xl"></i>
            </a>
            <a href="https://codepen.io/" target="_blank" class="text-purple-300 hover:text-pink-200 transition cursor-pointer">
              <i class="fab fa-codepen text-xl"></i>
            </a>
          </div>
        </div>
        
        <hr class="border-purple-700 my-8">
        
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="text-purple-400 mb-4 md:mb-0">
            &copy; {{ currentYear }} Christine. All rights reserved.
          </div>
          
          <div class="flex items-center space-x-4">
            <span class="text-purple-400">Accepted Payment Methods:</span>
            <i class="fab fa-cc-visa text-xl text-purple-300"></i>
            <i class="fab fa-cc-mastercard text-xl text-purple-300"></i>
            <i class="fab fa-cc-paypal text-xl text-purple-300"></i>
          </div>
        </div>
      </div>
      
      <!-- Back to top button -->
      <button 
        @click="scrollToTop" 
        class="fixed bottom-6 right-6 w-12 h-12 rounded-full bg-gradient-to-r from-pink-500 to-purple-500 text-white flex items-center justify-center shadow-lg hover:from-pink-600 hover:to-purple-600 transition cursor-pointer"
        :class="{ 'opacity-0 pointer-events-none': !showBackToTop, 'opacity-100': showBackToTop }"
      >
        <i class="fas fa-arrow-up"></i>
      </button>
    </footer>
</template>
<script lang="ts" setup>

import { ref, onMounted, onUnmounted } from 'vue';  

const currentYear = new Date().getFullYear();

// Back to top button visibility
const showBackToTop = ref(false);
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
};

const checkScrollPosition = () => {
  showBackToTop.value = window.scrollY > 500;
};
</script>