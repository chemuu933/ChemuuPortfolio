<template>
<header class="relative">
      <!-- Navigation -->
      <nav class="fixed top-0 left-0 right-0 z-50 bg-purple-900 shadow-md">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
          <div class="text-xl font-bold text-purple-300">Christine</div>
          <div class="hidden md:flex space-x-8">
            <a href="#home" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">Home</a>
            <a href="#about" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">About</a>
            <a href="#skills" class="text-purple-200 hover:text-purple-100  transition duration-300 cursor-pointer">Skills</a>
            <a href="#projects" class="text-purple-200 hover:text-purple-100  transition duration-300 cursor-pointer">Projects</a>
            <a href="#contact" class="text-purple-200 hover:text-purple-100  transition duration-300 cursor-pointer">Contact</a>
          </div>
          <div class="md:hidden">
            <button @click="toggleMobileMenu" class="text-purple-200 cursor-pointer">
              <i class="fas fa-bars text-xl"></i>
            </button>
          </div>
        </div>

         <!-- Mobile Menu -->
        <div v-if="mobileMenuOpen" class="md:hidden bg-purple-800 shadow-lg absolute w-full">
          <div class="container mx-auto px-6 py-4 flex flex-col space-y-4">
            <a href="#home" @click="closeMobileMenu" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">Home</a>
            <a href="#about" @click="closeMobileMenu" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">About</a>
            <a href="#skills" @click="closeMobileMenu" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">Skills</a>
            <a href="#projects" @click="closeMobileMenu" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">Projects</a>
            <a href="#contact" @click="closeMobileMenu" class="text-purple-200 hover:text-purple-100 transition duration-300 cursor-pointer">Contact</a>
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

<style scoped>
@keyframes gradient {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

@keyframes bounce-gentle {
  0%, 20%, 53%, 80%, 100% { transform: translate3d(0,0,0); }
  40%, 43% { transform: translate3d(0,-8px,0); }
  70% { transform: translate3d(0,-4px,0); }
  90% { transform: translate3d(0,-2px,0); }
}

@keyframes fade-in-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in {
  0% {
    opacity: 0;
    transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes pulse-gentle {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.8; }
}

.animate-gradient {
  background-size: 200% 200%;
  animation: gradient 6s ease infinite;
}

.animate-bounce-gentle {
  animation: bounce-gentle 3s infinite;
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
  opacity: 0;
}

.animate-slide-in {
  animation: slide-in 0.6s ease-out forwards;
  opacity: 0;
}

.animate-pulse-gentle {
  animation: pulse-gentle 2s ease-in-out infinite;
}

/* Vue transition for mobile menu */
.slide-down-enter-active {
  transition: all 0.3s ease-out;
}

.slide-down-leave-active {
  transition: all 0.3s ease-in;
}

.slide-down-enter-from {
  transform: translateY(-100%);
  opacity: 0;
}

.slide-down-leave-to {
  transform: translateY(-100%);
  opacity: 0;
}

/* Hover effects */
.group:hover .group-hover\:scale-100 {
  transform: scale(1);
}

.group:hover .group-hover\:opacity-20 {
  opacity: 0.2;
}
</style>