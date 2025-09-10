<template>
  <section id="skills" class="py-20 bg-gradient-to-br from-purple-100 via-pink-50 to-rose-100 relative overflow-hidden">
    <!-- Floating decorative elements -->
    <div class="absolute top-16 left-10 animate-float-1">
      <div class="w-12 h-12 bg-gradient-to-br from-pink-300 to-rose-400 rounded-full opacity-20 blur-sm"></div>
    </div>
    <div class="absolute top-40 right-16 animate-float-2">
      <div class="w-8 h-8 bg-gradient-to-br from-purple-300 to-pink-400 rounded-full opacity-25"></div>
    </div>
    <div class="absolute bottom-32 left-1/4 animate-float-3">
      <div class="w-6 h-6 bg-gradient-to-br from-rose-300 to-pink-500 rounded-full opacity-30"></div>
    </div>
    <div class="absolute bottom-16 right-1/3 animate-float-4">
      <div class="w-10 h-10 bg-gradient-to-br from-pink-400 to-purple-400 rounded-full opacity-15 blur-sm"></div>
    </div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center mb-16 animate-fade-in-up">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 animate-slide-down">
          ✨ My Skills ✨
        </h2>
        <div class="w-20 h-1 bg-gradient-to-r from-pink-400 via-rose-500 to-purple-500 mx-auto rounded-full animate-expand-line"></div>
        <p class="text-gray-700 mt-6 max-w-2xl mx-auto text-lg animate-fade-in" style="animation-delay: 0.3s">
          I've developed expertise in various technologies throughout my
          education and personal projects. 🌸
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
        <!-- Technical Skills -->
        <div class="bg-white/70 backdrop-blur-sm rounded-2xl shadow-xl p-8 border border-white/50 animate-slide-in-left hover:shadow-2xl transition-all duration-500">
          <div class="flex items-center mb-8">
            <div class="w-12 h-12 bg-gradient-to-br from-pink-400 to-rose-500 rounded-xl flex items-center justify-center mr-4 animate-pulse-gentle">
              <i class="fas fa-code text-white text-xl"></i>
            </div>
            <h3 class="text-2xl font-semibold text-gray-800">
              💻 Technical Skills
            </h3>
          </div>

          <div class="space-y-6">
            <div
              v-for="(skill, index) in technicalSkills"
              :key="`tech-${index}`"
              class="animate-skill-appear"
              :style="{ animationDelay: `${0.1 * index}s` }"
            >
              <div class="flex justify-between mb-3">
                <span class="text-gray-800 font-medium text-lg">{{ skill.name }}</span>
                <span class="text-pink-600 font-bold text-lg animate-number-count"
                  >{{ skill.level }}%</span
                >
              </div>
              <div class="w-full bg-gray-200/60 rounded-full h-3 overflow-hidden shadow-inner">
                <div
                  class="bg-gradient-to-r from-pink-400 via-rose-500 to-purple-500 h-3 rounded-full animate-progress-fill relative overflow-hidden"
                  :style="{ 
                    width: `${skill.level}%`,
                    animationDelay: `${0.2 + (0.1 * index)}s`
                  }"
                >
                  <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent animate-shimmer"></div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Additional Skills -->
        <div class="bg-white/70 backdrop-blur-sm rounded-2xl shadow-xl p-8 border border-white/50 animate-slide-in-right hover:shadow-2xl transition-all duration-500">
          <div class="flex items-center mb-8">
            <div class="w-12 h-12 bg-gradient-to-br from-purple-400 to-pink-500 rounded-xl flex items-center justify-center mr-4 animate-pulse-gentle" style="animation-delay: 0.5s">
              <i class="fas fa-star text-white text-xl"></i>
            </div>
            <h3 class="text-2xl font-semibold text-gray-800">
              🌟 Additional Skills
            </h3>
          </div>

          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
            <div
              v-for="(skill, index) in softSkills"
              :key="`soft-${index}`"
              class="bg-white/80 backdrop-blur-sm rounded-xl p-4 shadow-lg flex items-center transition-all duration-300 hover:shadow-xl hover:-translate-y-1 hover:bg-white/90 animate-card-pop group cursor-pointer border border-white/30"
              :style="{ animationDelay: `${0.05 * index}s` }"
            >
              <div
                class="w-12 h-12 rounded-xl bg-gradient-to-br from-pink-100 to-rose-200 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300"
              >
                <i :class="`fas ${skill.icon} text-pink-600 text-lg`"></i>
              </div>
              <span class="text-gray-800 font-medium group-hover:text-gray-900 transition-colors duration-300">{{ skill.name }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
const technicalSkills = [
  { name: "HTML/CSS", level: 90 },
  { name: "JavaScript", level: 85 },
  { name: "React", level: 80 },
  { name: "Vue.js", level: 75 },
  { name: "Express.js", level: 70 },
  { name: "Responsive Design", level: 85 },
];

const softSkills = [
  { name: "Problem Solving", icon: "fa-lightbulb" },
  { name: "Team Collaboration", icon: "fa-users" },
  { name: "Git/Version Control", icon: "fa-code-branch" },
  { name: "UI/UX Design", icon: "fa-pencil-ruler" },
  { name: "Database Management", icon: "fa-database" },
  { name: "Communication", icon: "fa-comments" },
  { name: "Time Management", icon: "fa-clock" },
  { name: "Leadership", icon: "fa-crown" },
  { name: "Adaptability", icon: "fa-sync-alt" },
  { name: "Code Review", icon: "fa-check-circle" },
  { name: "RESTful APIs", icon: "fa-server" },
  { name: "Testing/Debugging", icon: "fa-bug" },
];
</script>

<style scoped>
@keyframes float-1 {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(180deg); }
}

@keyframes float-2 {
  0%, 100% { transform: translateY(0px) scale(1); }
  50% { transform: translateY(-15px) scale(1.1); }
}

@keyframes float-3 {
  0%, 100% { transform: translateY(0px) translateX(0px); }
  33% { transform: translateY(-10px) translateX(5px); }
  66% { transform: translateY(-5px) translateX(-5px); }
}

@keyframes float-4 {
  0%, 100% { transform: translateY(0px) rotate(0deg) scale(1); }
  50% { transform: translateY(-25px) rotate(90deg) scale(1.2); }
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

@keyframes slide-down {
  0% {
    opacity: 0;
    transform: translateY(-20px) scale(0.95);
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

@keyframes fade-in {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@keyframes slide-in-left {
  0% {
    opacity: 0;
    transform: translateX(-50px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-in-right {
  0% {
    opacity: 0;
    transform: translateX(50px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes skill-appear {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes progress-fill {
  0% {
    width: 0;
  }
  100% {
    /* Width is set via inline styles */
  }
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

@keyframes number-count {
  0% {
    transform: scale(0.8);
    opacity: 0;
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}

@keyframes card-pop {
  0% {
    opacity: 0;
    transform: scale(0.8) translateY(20px);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}

@keyframes pulse-gentle {
  0%, 100% { 
    transform: scale(1);
    box-shadow: 0 0 0 0 rgba(236, 72, 153, 0.4);
  }
  50% { 
    transform: scale(1.05);
    box-shadow: 0 0 0 10px rgba(236, 72, 153, 0);
  }
}

/* Apply animations */
.animate-float-1 { animation: float-1 6s ease-in-out infinite; }
.animate-float-2 { animation: float-2 4s ease-in-out infinite; }
.animate-float-3 { animation: float-3 5s ease-in-out infinite; }
.animate-float-4 { animation: float-4 7s ease-in-out infinite; }

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
  opacity: 0;
}

.animate-slide-down {
  animation: slide-down 0.8s ease-out forwards;
  opacity: 0;
}

.animate-expand-line {
  animation: expand-line 1s ease-out forwards;
  animation-delay: 0.5s;
  width: 0;
}

.animate-fade-in {
  animation: fade-in 0.8s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-left {
  animation: slide-in-left 1s ease-out forwards;
  animation-delay: 0.2s;
  opacity: 0;
}

.animate-slide-in-right {
  animation: slide-in-right 1s ease-out forwards;
  animation-delay: 0.4s;
  opacity: 0;
}

.animate-skill-appear {
  animation: skill-appear 0.6s ease-out forwards;
  opacity: 0;
}

.animate-progress-fill {
  animation: progress-fill 1.5s ease-out forwards;
  width: 0;
}

.animate-shimmer {
  animation: shimmer 2s ease-in-out infinite;
  animation-delay: 1s;
}

.animate-number-count {
  animation: number-count 0.6s ease-out forwards;
  animation-delay: 0.8s;
}

.animate-card-pop {
  animation: card-pop 0.5s ease-out forwards;
  opacity: 0;
}

.animate-pulse-gentle {
  animation: pulse-gentle 2s ease-in-out infinite;
}

/* Responsive improvements */
@media (max-width: 640px) {
  .grid-cols-1.sm\:grid-cols-2 {
    grid-template-columns: 1fr;
  }
}

/* Enhanced hover effects */
.group:hover .group-hover\:scale-110 {
  transform: scale(1.1);
}
</style>