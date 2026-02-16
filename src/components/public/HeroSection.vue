<template>
  <section id="home" class="relative min-h-screen flex items-center overflow-hidden bg-gradient-to-br from-slate-900 via-teal-900 to-slate-800">
    <!-- Animated background circles -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-teal-500/10 rounded-full blur-3xl animate-pulse-slow"></div>
      <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-cyan-500/10 rounded-full blur-3xl animate-pulse-slower"></div>
      <div class="absolute top-1/2 left-1/2 w-64 h-64 bg-emerald-500/10 rounded-full blur-3xl animate-float-gentle"></div>
    </div>

    <!-- Decorative floating elements -->
    <div class="absolute top-20 left-16 animate-float-sparkle">
      <div class="w-3 h-3 bg-teal-400 rounded-full opacity-40 shadow-lg shadow-teal-400/50"></div>
    </div>
    <div class="absolute top-40 right-20 animate-float-heart">
      <div class="w-4 h-4 bg-cyan-400 rounded-full opacity-35 shadow-lg shadow-cyan-400/50"></div>
    </div>
    <div class="absolute bottom-32 left-1/4 animate-float-butterfly">
      <div class="w-2 h-2 bg-emerald-400 rounded-full opacity-30 shadow-lg shadow-emerald-400/50"></div>
    </div>

    <div class="container relative mx-auto px-6 py-20 z-10">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <!-- Left Content -->
        <div class="space-y-8 text-left animate-slide-in-left">
          <!-- Brand Badge -->
          <div class="inline-flex items-center gap-3 animate-fade-in">
            <div class="flex items-center gap-2 px-4 py-2 bg-teal-500/20 backdrop-blur-sm rounded-full border border-teal-400/30">
              <span class="text-teal-400 font-bold text-sm tracking-wider">JC</span>
              <span class="text-teal-300 text-xs">WELCOME TO MY WORLD</span>
              <span class="w-2 h-2 bg-teal-400 rounded-full animate-pulse"></span>
            </div>
          </div>
          
          <!-- Main Heading -->
          <div class="space-y-4">
            <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight animate-slide-down">
              <span class="text-white">Hi, I'm</span>
              <br />
              <span class="block bg-gradient-to-r from-teal-300 via-cyan-300 to-teal-400 bg-clip-text text-transparent animate-gradient-text mt-2">
                Jemutai Christine
              </span>
            </h1>
            
            <div class="flex items-baseline gap-3 animate-fade-in min-h-[60px]" style="animation-delay: 0.2s">
              <span class="text-gray-400 text-xl">a</span>
              <span class="text-teal-400 text-3xl md:text-4xl font-semibold border-b-2 border-teal-400 pb-1">
                {{ displayedRole }}<span class="animate-blink">|</span>
              </span>
            </div>
            
            <p class="text-lg md:text-xl text-gray-300 max-w-2xl leading-relaxed animate-fade-in" style="animation-delay: 0.3s">
              Transforming ideas into elegant digital solutions. I blend creativity with technical expertise to build experiences that captivate and inspire.
            </p>
          </div>
          
          <!-- CTA Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 pt-4 animate-fade-in" style="animation-delay: 0.5s">
            <a
              href="#projects"
              class="group relative px-8 py-4 bg-gradient-to-r from-teal-400 to-cyan-500 hover:from-teal-500 hover:to-cyan-600 rounded-full font-semibold text-slate-900 overflow-hidden transition-all duration-500 hover:scale-105 hover:shadow-2xl hover:shadow-teal-400/50 shadow-lg cursor-pointer"
            >
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent -skew-x-12 group-hover:animate-shimmer"></div>
              <span class="relative z-10 flex items-center justify-center gap-2">
                Explore My Work
                <svg class="w-5 h-5 group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                </svg>
              </span>
            </a>
            
            <a
              href="#contact"
              class="group px-8 py-4 bg-transparent border-2 border-teal-400/50 hover:border-teal-400 rounded-full font-semibold text-teal-300 hover:bg-teal-400/10 transition-all duration-500 hover:scale-105 shadow-lg hover:shadow-xl hover:shadow-teal-400/30 flex items-center justify-center gap-2 cursor-pointer"
            >
              Let's Connect
              <svg class="w-5 h-5 group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
              </svg>
            </a>
          </div>

          <!-- Social Icons -->
          <div class="flex items-center gap-4 pt-4 animate-fade-in" style="animation-delay: 0.7s">
            <div class="w-12 h-px bg-gray-600"></div>
            <a href="#" class="group w-10 h-10 rounded-full border border-gray-600 hover:border-teal-400 flex items-center justify-center transition-all duration-300 hover:bg-teal-400/10 hover:scale-110">
              <svg class="w-5 h-5 text-gray-400 group-hover:text-teal-400" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
            </a>
            <a href="#" class="group w-10 h-10 rounded-full border border-gray-600 hover:border-teal-400 flex items-center justify-center transition-all duration-300 hover:bg-teal-400/10 hover:scale-110">
              <svg class="w-5 h-5 text-gray-400 group-hover:text-teal-400" fill="currentColor" viewBox="0 0 24 24">
                <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
              </svg>
            </a>
            <a href="#" class="group w-10 h-10 rounded-full border border-gray-600 hover:border-teal-400 flex items-center justify-center transition-all duration-300 hover:bg-teal-400/10 hover:scale-110">
              <svg class="w-5 h-5 text-gray-400 group-hover:text-teal-400" fill="currentColor" viewBox="0 0 24 24">
                <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
              </svg>
            </a>
            <a href="#" class="group w-10 h-10 rounded-full border border-gray-600 hover:border-teal-400 flex items-center justify-center transition-all duration-300 hover:bg-teal-400/10 hover:scale-110">
              <svg class="w-5 h-5 text-gray-400 group-hover:text-teal-400" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 0C5.372 0 0 5.372 0 12s5.372 12 12 12 12-5.372 12-12S18.628 0 12 0zm5.696 14.943c-4.103 4.103-11.433 1.794-11.433 1.794s-2.309-7.33 1.794-11.433S19.49 3.51 19.49 3.51s2.309 7.33-1.794 11.433z"/>
              </svg>
            </a>
          </div>
        </div>
        
        <!-- Right Content - Profile Image with Geometric Circles -->
        <div class="flex justify-center md:justify-end animate-slide-in-right">
          <div class="relative w-80 h-80 md:w-96 md:h-96">
            
            <!-- Outer decorative circle with animated border -->
            <div class="absolute inset-0 animate-spin-very-slow">
              <div class="absolute inset-0 rounded-full border-2 border-teal-500/30">
                <!-- Small decorative dots on the circle -->
                <div class="absolute top-0 left-1/2 w-3 h-3 bg-teal-400 rounded-full transform -translate-x-1/2 -translate-y-1/2 shadow-lg shadow-teal-400/50"></div>
                <div class="absolute bottom-0 left-1/2 w-3 h-3 bg-cyan-400 rounded-full transform -translate-x-1/2 translate-y-1/2 shadow-lg shadow-cyan-400/50"></div>
              </div>
            </div>

            <!-- Middle circle -->
            <div class="absolute inset-8 animate-spin-reverse-very-slow">
              <div class="absolute inset-0 rounded-full border-2 border-teal-400/20">
                <div class="absolute top-1/2 right-0 w-3 h-3 bg-emerald-400 rounded-full transform translate-x-1/2 -translate-y-1/2 shadow-lg shadow-emerald-400/50"></div>
                <div class="absolute top-1/2 left-0 w-3 h-3 bg-teal-300 rounded-full transform -translate-x-1/2 -translate-y-1/2 shadow-lg shadow-teal-300/50"></div>
              </div>
            </div>

            <!-- Inner circle -->
            <div class="absolute inset-16 animate-pulse-border">
              <div class="absolute inset-0 rounded-full border-2 border-cyan-400/30"></div>
            </div>

            <!-- Central profile image -->
            <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 z-20">
              <div class="relative group">
                <!-- Glowing ring effect -->
                <div class="absolute -inset-3 bg-gradient-to-r from-teal-400 via-cyan-400 to-emerald-400 rounded-full blur-2xl opacity-50 group-hover:opacity-75 transition duration-500 animate-pulse-glow"></div>
                
                <!-- Image container with animated border -->
                <div class="relative">
                  <div class="absolute -inset-1 bg-gradient-to-r from-teal-400 to-cyan-400 rounded-full opacity-75 group-hover:opacity-100 transition duration-500"></div>
                  <div class="relative bg-slate-800 rounded-full p-1">
                    <img
                      :src="profileImageUrl"
                      alt="Christine - IT Student"
                      class="w-48 h-48 md:w-56 md:h-56 rounded-full object-cover object-top border-4 border-slate-800 shadow-2xl"
                    />
                  </div>
                </div>

                <!-- Code symbol decorations around image -->
                <div class="absolute -top-4 -right-4 w-12 h-12 bg-gradient-to-br from-teal-400 to-cyan-500 rounded-xl flex items-center justify-center text-white font-bold shadow-lg shadow-teal-400/50 animate-float-code transform hover:scale-110 transition-transform cursor-pointer">
                  &lt;/&gt;
                </div>
                
                <div class="absolute -bottom-4 -left-4 w-12 h-12 bg-gradient-to-br from-cyan-400 to-emerald-500 rounded-xl flex items-center justify-center text-white font-bold shadow-lg shadow-cyan-400/50 animate-float-code-delayed transform hover:scale-110 transition-transform cursor-pointer">
                  &#123; &#125;
                </div>

                <!-- Additional code icons -->
                <!-- Lightbulb for Problem Solving (top-left) -->
                <div class="absolute -top-4 -left-4 w-12 h-12 bg-gradient-to-br from-yellow-400 to-orange-500 rounded-xl flex items-center justify-center text-white text-2xl shadow-lg shadow-yellow-400/50 animate-float-code-3 transform hover:scale-110 transition-transform cursor-pointer">
                  💡
                </div>

                <!-- Palette for UI/UX (bottom-right) -->
                <div class="absolute -bottom-4 -right-4 w-12 h-12 bg-gradient-to-br from-pink-400 to-purple-500 rounded-xl flex items-center justify-center text-white text-2xl shadow-lg shadow-pink-400/50 animate-float-code-4 transform hover:scale-110 transition-transform cursor-pointer">
                  🎨
                </div>

                <!-- Rocket for Innovation (right-middle) -->
                <div class="absolute top-1/2 -right-6 transform -translate-y-1/2 w-12 h-12 bg-gradient-to-br from-indigo-400 to-blue-500 rounded-xl flex items-center justify-center text-white text-2xl shadow-lg shadow-indigo-400/50 animate-float-code-5 transform hover:scale-110 transition-transform cursor-pointer">
                  🚀
                </div>

                <!-- Code brackets for Development (left-middle) -->
                <div class="absolute top-1/2 -left-6 tran sform -translate-y-1/2 w-12 h-12 bg-gradient-to-br from-green-400 to-teal-500 rounded-xl flex items-center justify-center text-white font-bold text-lg shadow-lg shadow-green-400/50 animate-float-code-6 transform hover:scale-110 transition-transform cursor-pointer">
                  [ ]
                </div>
              </div>
            </div>

            <!-- Pulsing circles background -->
            <div class="absolute inset-0 border border-teal-400/20 rounded-full opacity-30 animate-ping-very-slow"></div>
            <div class="absolute inset-12 border border-cyan-400/20 rounded-full opacity-20 animate-ping-slower"></div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Scroll indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce-slow">
      <div class="flex flex-col items-center gap-2 text-teal-300">
        <span class="text-xs font-medium tracking-wider uppercase">Scroll Down</span>
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
        </svg>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from 'vue'
// @ts-ignore
import profileImageUrl from '../../assets/chemuu1.jpeg'

const roles = ['UI/UX Designer', 'Web Developer', 'Problem Solver']
const displayedRole = ref('')
let currentRoleIndex = 0
let currentCharIndex = 0
let isDeleting = false
let typingTimeout: ReturnType<typeof setTimeout> | null = null

const typeRole = () => {
  const currentRole = roles[currentRoleIndex]
  
  if (!isDeleting) {
    // Typing
    displayedRole.value = currentRole.substring(0, currentCharIndex + 1)
    currentCharIndex++
    
    if (currentCharIndex === currentRole.length) {
      // Finished typing, wait before deleting
      typingTimeout = setTimeout(() => {
        isDeleting = true
        typeRole()
      }, 2000) // Wait 2 seconds before deleting
      return
    }
    
    typingTimeout = setTimeout(typeRole, 100) // Typing speed
  } else {
    // Deleting
    displayedRole.value = currentRole.substring(0, currentCharIndex - 1)
    currentCharIndex--
    
    if (currentCharIndex === 0) {
      // Finished deleting, move to next role
      isDeleting = false
      currentRoleIndex = (currentRoleIndex + 1) % roles.length
      typingTimeout = setTimeout(typeRole, 500) // Wait before typing next role
      return
    }
    
    typingTimeout = setTimeout(typeRole, 50) // Deleting speed (faster)
  }
}

onMounted(() => {
  // Start typing animation after a short delay
  typingTimeout = setTimeout(typeRole, 1000)
})

onUnmounted(() => {
  if (typingTimeout) {
    clearTimeout(typingTimeout)
  }
})
</script>

<style scoped>
/* Floating animations for decorative elements */
@keyframes float-sparkle {
  0%, 100% { transform: translateY(0px) scale(1); }
  50% { transform: translateY(-20px) scale(1.3); }
}

@keyframes float-heart {
  0%, 100% { transform: translateY(0px) translateX(0px); }
  50% { transform: translateY(-15px) translateX(10px); }
}

@keyframes float-butterfly {
  0%, 100% { transform: translateY(0px) translateX(0px); }
  33% { transform: translateY(-10px) translateX(8px); }
  66% { transform: translateY(-5px) translateX(-8px); }
}

@keyframes float-gentle {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(20px, -20px); }
}

@keyframes float-code {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-10px) rotate(5deg); }
}

@keyframes float-code-delayed {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-10px) rotate(-5deg); }
}

@keyframes float-code-3 {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-12px) rotate(8deg); }
}

@keyframes float-code-4 {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-8px) rotate(-8deg); }
}

@keyframes float-code-5 {
  0%, 100% { transform: translateY(0px) rotate(0deg) translateX(0px); }
  50% { transform: translateY(-10px) rotate(10deg) translateX(-5px); }
}

@keyframes float-code-6 {
  0%, 100% { transform: translateY(0px) rotate(0deg) translateX(0px); }
  50% { transform: translateY(-10px) rotate(-10deg) translateX(5px); }
}

@keyframes blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0; }
}

/* Rotation animations */
@keyframes spin-very-slow {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

@keyframes spin-reverse-very-slow {
  from { transform: rotate(360deg); }
  to { transform: rotate(0deg); }
}

/* Slide animations */
@keyframes slide-in-left {
  0% {
    opacity: 0;
    transform: translateX(-60px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-in-right {
  0% {
    opacity: 0;
    transform: translateX(60px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-down {
  0% {
    opacity: 0;
    transform: translateY(-30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fade-in {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@keyframes gradient-text {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

@keyframes pulse-slow {
  0%, 100% { opacity: 0.3; }
  50% { opacity: 0.6; }
}

@keyframes pulse-slower {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.5; }
}

@keyframes pulse-glow {
  0%, 100% { opacity: 0.5; transform: scale(1); }
  50% { opacity: 0.75; transform: scale(1.05); }
}

@keyframes pulse-border {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 0.6; transform: scale(1.02); }
}

@keyframes shimmer {
  0% { transform: translateX(-100%) skewX(-12deg); }
  100% { transform: translateX(200%) skewX(-12deg); }
}

@keyframes ping-very-slow {
  0% { transform: scale(1); opacity: 0.3; }
  50% { transform: scale(1.1); opacity: 0.1; }
  100% { transform: scale(1); opacity: 0.3; }
}

@keyframes bounce-slow {
  0%, 100% { transform: translateY(0) translateX(-50%); }
  50% { transform: translateY(-10px) translateX(-50%); }
}

/* Apply animations */
.animate-float-sparkle { animation: float-sparkle 4s ease-in-out infinite; }
.animate-float-heart { animation: float-heart 5s ease-in-out infinite; }
.animate-float-butterfly { animation: float-butterfly 6s ease-in-out infinite; }
.animate-float-gentle { animation: float-gentle 8s ease-in-out infinite; }
.animate-float-code { animation: float-code 3s ease-in-out infinite; }
.animate-float-code-delayed { 
  animation: float-code-delayed 3s ease-in-out infinite;
  animation-delay: 1.5s;
}
.animate-float-code-3 { 
  animation: float-code-3 3.5s ease-in-out infinite;
  animation-delay: 0.5s;
}
.animate-float-code-4 { 
  animation: float-code-4 3.2s ease-in-out infinite;
  animation-delay: 2s;
}
.animate-float-code-5 { 
  animation: float-code-5 3.8s ease-in-out infinite;
  animation-delay: 0.8s;
}
.animate-float-code-6 { 
  animation: float-code-6 3.3s ease-in-out infinite;
  animation-delay: 1.2s;
}
.animate-blink {
  animation: blink 1s ease-in-out infinite;
}

.animate-spin-very-slow { animation: spin-very-slow 30s linear infinite; }
.animate-spin-reverse-very-slow { animation: spin-reverse-very-slow 25s linear infinite; }

.animate-slide-in-left {
  animation: slide-in-left 1s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-right {
  animation: slide-in-right 1s ease-out forwards;
  animation-delay: 0.3s;
  opacity: 0;
}

.animate-slide-down {
  animation: slide-down 0.8s ease-out forwards;
  opacity: 0;
}

.animate-fade-in {
  animation: fade-in 1s ease-out forwards;
  opacity: 0;
}

.animate-gradient-text {
  background-size: 200% 200%;
  animation: gradient-text 4s ease infinite;
}

.animate-pulse-slow { animation: pulse-slow 4s ease-in-out infinite; }
.animate-pulse-slower { animation: pulse-slower 5s ease-in-out infinite; }
.animate-pulse-glow { animation: pulse-glow 3s ease-in-out infinite; }
.animate-pulse-border { animation: pulse-border 4s ease-in-out infinite; }

.animate-shimmer { animation: shimmer 2s ease-in-out; }

.animate-ping-very-slow { animation: ping-very-slow 4s cubic-bezier(0, 0, 0.2, 1) infinite; }

.animate-bounce-slow { animation: bounce-slow 2.5s ease-in-out infinite; }
</style>