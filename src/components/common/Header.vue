<template>
<header class="relative">
      <!-- Navigation with Glass Morphism -->
      <nav class="fixed top-0 left-0 right-0 z-50 transition-all duration-500 nav-blur">
        <!-- Animated gradient border -->
        <div class="absolute inset-0 opacity-30">
          <div class="absolute inset-0 bg-gradient-to-r from-cyan-500 via-purple-500 to-pink-500 animate-gradient-shift"></div>
        </div>
        
        <!-- Glass background -->
        <div class="absolute inset-0 bg-gradient-to-br from-purple-900/40 via-slate-900/40 to-purple-900/40 backdrop-blur-xl border-b border-white/10"></div>
        
        <!-- Floating particles in nav -->
        <div class="absolute inset-0 overflow-hidden pointer-events-none">
          <div v-for="i in 8" :key="`nav-particle-${i}`" 
               class="absolute w-1 h-1 bg-cyan-400 rounded-full nav-particle"
               :style="{
                 left: `${Math.random() * 100}%`,
                 animationDelay: `${Math.random() * 3}s`,
                 animationDuration: `${4 + Math.random() * 2}s`
               }">
          </div>
        </div>

        <!-- Content -->
        <div class="container mx-auto px-6 py-4 flex justify-between items-center relative z-10">
          <!-- Logo with gradient animation -->
          <div class="text-2xl font-bold relative group cursor-pointer">
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 animate-gradient-text">
              Christine
            </span>
            <div class="absolute -bottom-1 left-0 w-0 h-0.5 bg-gradient-to-r from-cyan-400 to-purple-500 group-hover:w-full transition-all duration-500"></div>
          </div>

          <!-- Desktop Menu -->
          <div class="hidden md:flex space-x-1">
            <a 
              v-for="(item, index) in menuItems" 
              :key="`menu-${index}`"
              :href="item.href" 
              class="nav-link relative px-4 py-2 text-purple-200 hover:text-white transition-all duration-300 cursor-pointer group"
              :style="{ animationDelay: `${index * 0.1}s` }"
            >
              <!-- Link background glow -->
              <span class="absolute inset-0 bg-gradient-to-r from-cyan-500/0 via-purple-500/0 to-pink-500/0 group-hover:from-cyan-500/20 group-hover:via-purple-500/20 group-hover:to-pink-500/20 rounded-lg blur transition-all duration-500"></span>
              
              <!-- Link text -->
              <span class="relative z-10 flex items-center gap-2">
                <i :class="`${item.icon} text-sm`"></i>
                {{ item.label }}
              </span>
              
              <!-- Animated underline -->
              <span class="absolute bottom-0 left-1/2 -translate-x-1/2 w-0 h-0.5 bg-gradient-to-r from-cyan-400 via-purple-400 to-pink-400 group-hover:w-4/5 transition-all duration-500 rounded-full"></span>
              
              <!-- Glow dots -->
              <span class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-0 h-0 bg-purple-400 rounded-full opacity-0 group-hover:w-full group-hover:h-full group-hover:opacity-10 transition-all duration-500 blur-xl"></span>
            </a>
          </div>

          <!-- Mobile Menu Button -->
          <div class="md:hidden">
            <button 
              @click="toggleMobileMenu" 
              class="relative w-10 h-10 text-purple-200 hover:text-white cursor-pointer focus:outline-none group"
            >
              <!-- Button background -->
              <div class="absolute inset-0 bg-gradient-to-br from-cyan-500/20 to-purple-500/20 rounded-lg backdrop-blur-sm border border-white/10 group-hover:border-cyan-400/50 transition-all duration-300"></div>
              
              <!-- Hamburger icon with animation -->
              <div class="relative z-10 flex flex-col items-center justify-center w-full h-full gap-1.5">
                <span 
                  class="block w-5 h-0.5 bg-current transition-all duration-300 rounded-full"
                  :class="mobileMenuOpen ? 'rotate-45 translate-y-2' : ''"
                ></span>
                <span 
                  class="block w-5 h-0.5 bg-current transition-all duration-300 rounded-full"
                  :class="mobileMenuOpen ? 'opacity-0' : ''"
                ></span>
                <span 
                  class="block w-5 h-0.5 bg-current transition-all duration-300 rounded-full"
                  :class="mobileMenuOpen ? '-rotate-45 -translate-y-2' : ''"
                ></span>
              </div>
            </button>
          </div>
        </div>

        <!-- Mobile Menu with Glass Effect -->
        <transition name="slide-down">
          <div 
            v-if="mobileMenuOpen" 
            class="md:hidden absolute w-full top-full left-0 overflow-hidden"
          >
            <!-- Glass background -->
            <div class="relative bg-gradient-to-br from-purple-900/95 via-slate-900/95 to-purple-900/95 backdrop-blur-2xl border-b border-white/10 shadow-2xl">
              <!-- Gradient overlay -->
              <div class="absolute inset-0 bg-gradient-to-br from-cyan-500/5 via-purple-500/5 to-pink-500/5"></div>
              
              <!-- Menu items -->
              <div class="container mx-auto px-6 py-6 flex flex-col space-y-2 relative z-10">
                <a 
                  v-for="(item, index) in menuItems" 
                  :key="`mobile-menu-${index}`"
                  :href="item.href" 
                  @click="closeMobileMenu" 
                  class="mobile-nav-link relative px-4 py-3 text-purple-200 hover:text-white transition-all duration-300 cursor-pointer rounded-lg group overflow-hidden"
                  :style="{ animationDelay: `${index * 0.05}s` }"
                >
                  <!-- Background glow on hover -->
                  <div class="absolute inset-0 bg-gradient-to-r from-cyan-500/0 via-purple-500/0 to-pink-500/0 group-hover:from-cyan-500/20 group-hover:via-purple-500/20 group-hover:to-pink-500/20 transition-all duration-500"></div>
                  
                  <!-- Border on hover -->
                  <div class="absolute inset-0 border border-transparent group-hover:border-cyan-400/30 rounded-lg transition-all duration-500"></div>
                  
                  <!-- Content -->
                  <span class="relative z-10 flex items-center gap-3">
                    <i :class="`${item.icon} text-cyan-400`"></i>
                    {{ item.label }}
                  </span>
                  
                  <!-- Shine effect -->
                  <div class="absolute inset-0 opacity-0 group-hover:opacity-100 transition-opacity duration-500">
                    <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"></div>
                  </div>
                </a>
              </div>

              <!-- Decorative gradient line at bottom -->
              <div class="h-1 bg-gradient-to-r from-cyan-500 via-purple-500 to-pink-500 opacity-50"></div>
            </div>
          </div>
        </transition>
      </nav>
</header>
</template>

<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from 'vue';

const mobileMenuOpen = ref(false);

const menuItems = [
  { label: 'Home', href: '#home', icon: 'fas fa-home' },
  { label: 'About', href: '#about', icon: 'fas fa-user' },
  { label: 'Skills', href: '#skills', icon: 'fas fa-code' },
  { label: 'Projects', href: '#projects', icon: 'fas fa-folder' },
  { label: 'Contact', href: '#contact', icon: 'fas fa-envelope' },
];

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
/* Navigation blur effect */
.nav-blur {
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

/* Gradient animations */
@keyframes gradient-shift {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

.animate-gradient-shift {
  animation: gradient-shift 8s linear infinite;
}

@keyframes gradient-text {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

.animate-gradient-text {
  background-size: 200% auto;
  animation: gradient-text 4s ease infinite;
}

/* Nav particles */
@keyframes nav-particle-float {
  0% {
    transform: translateY(80px) translateX(0);
    opacity: 0;
  }
  10% {
    opacity: 1;
  }
  90% {
    opacity: 1;
  }
  100% {
    transform: translateY(-80px) translateX(30px);
    opacity: 0;
  }
}

.nav-particle {
  animation: nav-particle-float 6s ease-in-out infinite;
  box-shadow: 0 0 8px currentColor;
}

/* Nav link entrance animation */
@keyframes nav-link-appear {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.nav-link {
  animation: nav-link-appear 0.5s ease-out forwards;
  opacity: 0;
}

/* Mobile nav link entrance */
@keyframes mobile-link-slide {
  0% {
    opacity: 0;
    transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.mobile-nav-link {
  animation: mobile-link-slide 0.4s ease-out forwards;
  opacity: 0;
}

/* Mobile menu transitions */
.slide-down-enter-active {
  animation: slide-down 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.slide-down-leave-active {
  animation: slide-down 0.3s cubic-bezier(0.34, 1.56, 0.64, 1) reverse;
}

@keyframes slide-down {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Legacy animations kept for compatibility */
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

/* Hover effects */
.group:hover .group-hover\:scale-100 {
  transform: scale(1);
}

.group:hover .group-hover\:opacity-20 {
  opacity: 0.2;
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}
</style>