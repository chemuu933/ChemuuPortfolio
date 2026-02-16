<template>
  <section
    id="about"
    class="py-20 bg-gradient-to-br from-teal-900 via-slate-800 to-emerald-900 relative overflow-hidden"
  >
    <!-- Floating decorative elements -->
    <div class="absolute top-10 left-10 animate-float-slow">
      <div class="w-8 h-8 bg-teal-400 rounded-full opacity-20"></div>
    </div>
    <div class="absolute top-32 right-20 animate-float-medium">
      <div class="w-6 h-6 bg-emerald-400 rounded-full opacity-25"></div>
    </div>
    <div class="absolute bottom-20 left-1/4 animate-float-fast">
      <div class="w-4 h-4 bg-cyan-400 rounded-full opacity-20"></div>
    </div>
    <div class="absolute bottom-40 right-1/3 animate-float-slow">
      <div class="w-5 h-5 bg-teal-300 rounded-full opacity-15"></div>
    </div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center mb-16 animate-fade-in-up">
        <h2
          class="text-3xl md:text-4xl font-bold text-white mb-4 animate-slide-in-title"
        >
          ✨ About Me ✨
        </h2>
        <div
          class="w-20 h-1 bg-gradient-to-r from-teal-400 to-emerald-400 mx-auto rounded-full animate-expand-line"
        ></div>
      </div>

      <div class="max-w-4xl mx-auto">
        <div class="animate-slide-in-up">
          <h3
            class="text-2xl md:text-3xl font-semibold text-teal-300 mb-6 animate-fade-in-up"
            style="animation-delay: 0.2s"
          >
            🌸 Who I Am
          </h3>
          <p
            class="text-gray-200 mb-6 leading-relaxed text-base md:text-lg animate-fade-in-up hover:text-white transition-colors duration-300"
            style="animation-delay: 0.3s"
          >
            I'm Christine, an ambitious IT professional passionate about
            creating meaningful digital experiences through code. My technology
            journey started with a curiosity about how websites work, which led
            me to pursue formal education in Information Technology at Kabarak
            University, where I built a strong foundation in both theory and
            practical application.. 💻
          </p>
          <p
            class="text-gray-200 mb-6 leading-relaxed text-base md:text-lg animate-fade-in-up hover:text-white transition-colors duration-300"
            style="animation-delay: 0.4s"
          >
            I specialize in frontend development, thriving on the challenge of
            translating ideas into intuitive, responsive interfaces. My
            technical toolkit includes HTML, CSS, JavaScript, React, and Vue.js,
            complemented by backend experience with Node.js and Express.js.. ✨
          </p>
          <p
            class="text-gray-200 mb-8 leading-relaxed text-base md:text-lg animate-fade-in-up hover:text-white transition-colors duration-300"
            style="animation-delay: 0.5s"
          >
            Beyond building applications, I am committed to continuous
            growth—expanding my expertise through online courses, contributing
            to open-source projects, and staying aligned with emerging trends in
            technology. I believe that thoughtful, well-crafted code has the
            power to solve real problems and deliver impactful user experiences.
            🚀
          </p>

          <div
            class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 mb-10 animate-fade-in-up"
            style="animation-delay: 0.6s"
          >
            <div
              class="flex items-center bg-white bg-opacity-10 backdrop-blur-sm px-4 py-3 rounded-xl shadow-lg hover:shadow-2xl hover:bg-opacity-15 transform hover:-translate-y-1 transition-all duration-300 animate-card-hover group border border-teal-500 border-opacity-20"
            >
              <i
                class="fas fa-graduation-cap text-teal-400 mr-3 text-lg group-hover:scale-110 transition-transform duration-300"
              ></i>
              <span class="text-gray-100 font-medium text-sm md:text-base"
                >IT Professional</span
              >
            </div>
            <div
              class="flex items-center bg-white bg-opacity-10 backdrop-blur-sm px-4 py-3 rounded-xl shadow-lg hover:shadow-2xl hover:bg-opacity-15 transform hover:-translate-y-1 transition-all duration-300 animate-card-hover group border border-emerald-500 border-opacity-20"
              style="animation-delay: 0.1s"
            >
              <i
                class="fas fa-code text-emerald-400 mr-3 text-lg group-hover:scale-110 transition-transform duration-300"
              ></i>
              <span class="text-gray-100 font-medium text-sm md:text-base"
                >Frontend Developer</span
              >
            </div>
            <div
              class="flex items-center bg-white bg-opacity-10 backdrop-blur-sm px-4 py-3 rounded-xl shadow-lg hover:shadow-2xl hover:bg-opacity-15 transform hover:-translate-y-1 transition-all duration-300 animate-card-hover group sm:col-span-2 lg:col-span-1 border border-cyan-500 border-opacity-20"
              style="animation-delay: 0.2s"
            >
              <i
                class="fas fa-pencil-alt text-cyan-400 mr-3 text-lg group-hover:scale-110 transition-transform duration-300"
              ></i>
              <span class="text-gray-100 font-medium text-sm md:text-base"
                >UI/UX Designer</span
              >
            </div>
          </div>

          <!-- Action Buttons -->
          <div
            class="flex flex-col sm:flex-row gap-4 justify-center items-center animate-fade-in-up"
            style="animation-delay: 0.7s"
          >
            <a
              href="https://wa.me/254708345963"
              target="_blank"
              rel="noopener noreferrer"
              class="group relative px-8 py-4 bg-gradient-to-r from-teal-500 to-emerald-500 text-white font-semibold rounded-full overflow-hidden transform hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-2xl animate-pulse-glow"
            >
              <span class="relative z-10 flex items-center gap-2">
                <i class="fas fa-envelope animate-swing"></i>
                Get in Touch
              </span>
              <div
                class="absolute inset-0 bg-gradient-to-r from-emerald-500 to-teal-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"
              ></div>
              <div
                class="absolute inset-0 bg-white opacity-0 group-hover:opacity-20 animate-shimmer"
              ></div>
            </a> 

            <a
              href="https://eu.docworkspace.com/d/sbPask59BjsmW9ZT_vche7o5u7slevod6f4?sa=601.1037"
              target="_blank"
              rel="noopener noreferrer"
              class="group relative px-8 py-4 bg-transparent text-teal-300 font-semibold rounded-full border-2 border-teal-400 overflow-hidden transform hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-2xl animate-border-glow"
            >
              <span class="relative z-10 flex items-center gap-2">
                <i class="fas fa-file-download animate-bounce-subtle"></i>
                View Resume
              </span>
              <div
                class="absolute inset-0 bg-gradient-to-r from-teal-500 to-emerald-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"
              ></div>
              <span
                class="absolute inset-0 border-2 border-teal-300 rounded-full animate-ping-slow opacity-20"
              ></span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
// Component logic can be added here if needed
</script>

<style scoped>
@keyframes float-slow {
  0%,
  100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
}

@keyframes float-medium {
  0%,
  100% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-15px) rotate(180deg);
  }
}

@keyframes float-fast {
  0%,
  100% {
    transform: translateY(0px) scale(1);
  }
  50% {
    transform: translateY(-10px) scale(1.1);
  }
}

@keyframes fade-in-up {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in-up {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in-title {
  0% {
    opacity: 0;
    transform: translateY(-20px) scale(0.9);
  }
  100% {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes expand-line {
  0% {
    width: 0;
    opacity: 0;
  }
  100% {
    width: 5rem;
    opacity: 1;
  }
}

@keyframes card-hover {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes pulse-glow {
  0%,
  100% {
    box-shadow: 0 0 20px rgba(20, 184, 166, 0.5);
  }
  50% {
    box-shadow: 0 0 30px rgba(16, 185, 129, 0.8);
  }
}

@keyframes border-glow {
  0%,
  100% {
    box-shadow: 0 0 15px rgba(20, 184, 166, 0.3);
  }
  50% {
    box-shadow: 0 0 25px rgba(20, 184, 166, 0.6);
  }
}

@keyframes shimmer {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}

@keyframes swing {
  0%,
  100% {
    transform: rotate(0deg);
  }
  25% {
    transform: rotate(-10deg);
  }
  75% {
    transform: rotate(10deg);
  }
}

@keyframes bounce-subtle {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-3px);
  }
}

@keyframes ping-slow {
  0% {
    transform: scale(1);
    opacity: 0.2;
  }
  50% {
    transform: scale(1.05);
    opacity: 0;
  }
  100% {
    transform: scale(1.1);
    opacity: 0;
  }
}

.animate-float-slow {
  animation: float-slow 6s ease-in-out infinite;
}

.animate-float-medium {
  animation: float-medium 4s ease-in-out infinite;
}

.animate-float-fast {
  animation: float-fast 3s ease-in-out infinite;
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-up {
  animation: slide-in-up 1s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-title {
  animation: slide-in-title 0.8s ease-out forwards;
  opacity: 0;
}

.animate-expand-line {
  animation: expand-line 1s ease-out forwards 0.5s;
  width: 0;
}

.animate-card-hover {
  animation: card-hover 0.6s ease-out forwards;
  opacity: 0;
}

.animate-pulse-glow {
  animation: pulse-glow 2s ease-in-out infinite;
}

.animate-border-glow {
  animation: border-glow 2s ease-in-out infinite;
}

.animate-shimmer {
  animation: shimmer 2s infinite;
}

.animate-swing {
  animation: swing 2s ease-in-out infinite;
}

.animate-bounce-subtle {
  animation: bounce-subtle 1.5s ease-in-out infinite;
}

.animate-ping-slow {
  animation: ping-slow 3s cubic-bezier(0, 0, 0.2, 1) infinite;
}

/* Responsive improvements */
@media (max-width: 768px) {
  .container {
    padding-left: 1rem;
    padding-right: 1rem;
  }
}

@media (max-width: 640px) {
  .grid-cols-1.sm\:grid-cols-2 {
    grid-template-columns: 1fr;
  }

  .sm\:col-span-2 {
    grid-column: span 1;
  }
}

/* Enhanced hover effects */
.group:hover .group-hover\:scale-110 {
  transform: scale(1.1);
}

/* Smooth scrolling for better UX */
html {
  scroll-behavior: smooth;
}
</style>