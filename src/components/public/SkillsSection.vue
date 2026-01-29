<template>
  <section
    id="skills"
    class="py-20 bg-gradient-to-br from-slate-900 via-slate-800 to-slate-900 relative overflow-hidden"
  >
    <!-- Animated background particles -->
    <div class="absolute inset-0 overflow-hidden">
      <div
        v-for="i in 20"
        :key="`particle-${i}`"
        class="absolute w-1 h-1 bg-cyan-400 rounded-full particle"
        :style="{
          left: `${Math.random() * 100}%`,
          top: `${Math.random() * 100}%`,
          animationDelay: `${Math.random() * 5}s`,
          animationDuration: `${3 + Math.random() * 4}s`,
        }"
      ></div>
    </div>

    <!-- Glowing orbs -->
    <div
      class="absolute top-20 left-10 w-64 h-64 bg-cyan-500/10 rounded-full blur-3xl animate-pulse-slow"
    ></div>
    <div
      class="absolute bottom-20 right-10 w-80 h-80 bg-blue-500/10 rounded-full blur-3xl animate-pulse-slower"
    ></div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center mb-16 animate-fade-in-down">
        <h2
          class="text-4xl md:text-5xl font-bold text-white mb-4 tracking-tight"
        >
          Skills & Expertise
        </h2>
        <div
          class="w-24 h-1 bg-gradient-to-r from-cyan-400 via-blue-500 to-purple-600 mx-auto rounded-full animate-width-expand"
        ></div>
        <p class="text-slate-300 mt-6 max-w-2xl mx-auto text-lg">
          Specialized in modern web technologies with a focus on creating
          exceptional digital experiences
        </p>
      </div>

      <div
        class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-7xl mx-auto"
      >
        <!-- Skill Cards -->
        <div
          v-for="(category, index) in skillCategories"
          :key="`category-${index}`"
          class="skill-card bg-slate-800/50 backdrop-blur-lg rounded-2xl p-6 border border-slate-700/50 hover:border-cyan-500/50 transition-all duration-500 animate-slide-up"
          :style="{ animationDelay: `${index * 0.1}s` }"
        >
          <!-- Card Header -->
          <div class="flex items-center mb-6">
            <div
              class="w-16 h-16 rounded-xl bg-gradient-to-br flex items-center justify-center mr-4 animate-rotate-in"
              :class="category.gradient"
              :style="{ animationDelay: `${0.2 + index * 0.1}s` }"
            >
              <i :class="`${category.icon} text-white text-2xl`"></i>
            </div>
            <h3 class="text-xl font-semibold text-white">
              {{ category.title }}
            </h3>
          </div>

          <!-- Skills Progress Bars -->
          <div class="space-y-4">
            <div
              v-for="(skill, skillIndex) in category.skills"
              :key="`skill-${index}-${skillIndex}`"
              class="skill-item"
              :style="{
                animationDelay: `${0.3 + index * 0.1 + skillIndex * 0.05}s`,
              }"
            >
              <div class="flex justify-between mb-2">
                <span class="text-slate-300 text-sm font-medium">{{
                  skill.name
                }}</span>
                <span class="text-cyan-400 text-sm font-bold skill-percentage"
                  >{{ skill.level }}%</span
                >
              </div>
              <div
                class="w-full bg-slate-700/50 rounded-full h-2 overflow-hidden"
              >
                <div
                  class="h-2 rounded-full progress-bar relative"
                  :class="category.barGradient"
                  :style="{
                    '--progress-width': `${skill.level}%`,
                    animationDelay: `${0.5 + index * 0.1 + skillIndex * 0.05}s`,
                  }"
                >
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent shimmer"
                  ></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
const skillCategories = [
  {
    title: "Frontend Development",
    icon: "fas fa-code",
    gradient: "from-cyan-500 to-blue-600",
    barGradient: "bg-gradient-to-r from-cyan-400 to-blue-500",
    skills: [
      { name: "Html/css", level: 95 },
      { name: "React & TypeScript", level: 90 },
      { name: "TailwindCSS", level: 92 },
      { name: "Vue.js", level: 85 },
    ],
  },
  {
    title: "Backend Development",
    icon: "fas fa-server",
    gradient: "from-blue-500 to-indigo-600",
    barGradient: "bg-gradient-to-r from-blue-400 to-indigo-500",
    skills: [
      { name: "Node.js", level: 88 },
      { name: "express.js", level: 82 },
      { name: "python", level: 85 },
      { name: "PostgreSQl", level: 80 },
    ],
  },
  {
    title: "UI/UX Design",
    icon: "fas fa-palette",
    gradient: "from-purple-500 to-pink-600",
    barGradient: "bg-gradient-to-r from-purple-400 to-pink-500",
    skills: [
      { name: "Figma", level: 93 },
      { name: "Adobe XD", level: 87 },
      { name: "canva", level: 90 },
      { name: "User Research", level: 85 },
    ],
  },
  {
    title: "DevOps & Tools",
    icon: "fas fa-tools",
    gradient: "from-emerald-500 to-teal-600",
    barGradient: "bg-gradient-to-r from-emerald-400 to-teal-500",
    skills: [
      { name: "Git & GitHub", level: 90 },
      { name: "Docker", level: 78 },
      { name: "CI/CD", level: 75 },
      { name: "AWS", level: 72 },
    ],
  },
  {
    title: "Soft Skills",
    icon: "fas fa-users",
    gradient: "from-purple-500 to-pink-600",
    barGradient: "bg-gradient-to-r from-purple-400 to-pink-500",
    skills: [
      { name: "Leadership", level: 90 },
      { name: "Communication", level: 95 },
      { name: "Problem Solving", level: 92 },
      { name: "Team Collaboration", level: 88 },
    ],
  },
];
</script>

<style scoped>
/* Particle Animation */
@keyframes float-particle {
  0%,
  100% {
    transform: translateY(0) translateX(0);
    opacity: 0;
  }
  10% {
    opacity: 1;
  }
  90% {
    opacity: 1;
  }
  100% {
    transform: translateY(-100vh) translateX(20px);
    opacity: 0;
  }
}

.particle {
  animation: float-particle 7s ease-in-out infinite;
}

/* Pulse Animations */
@keyframes pulse-slow {
  0%,
  100% {
    opacity: 0.3;
    transform: scale(1);
  }
  50% {
    opacity: 0.5;
    transform: scale(1.1);
  }
}

@keyframes pulse-slower {
  0%,
  100% {
    opacity: 0.2;
    transform: scale(1);
  }
  50% {
    opacity: 0.4;
    transform: scale(1.15);
  }
}

.animate-pulse-slow {
  animation: pulse-slow 8s ease-in-out infinite;
}

.animate-pulse-slower {
  animation: pulse-slower 10s ease-in-out infinite;
}

/* Fade In Down */
@keyframes fade-in-down {
  0% {
    opacity: 0;
    transform: translateY(-30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-down {
  animation: fade-in-down 0.8s ease-out forwards;
  opacity: 0;
}

/* Width Expand */
@keyframes width-expand {
  0% {
    width: 0;
  }
  100% {
    width: 6rem;
  }
}

.animate-width-expand {
  animation: width-expand 1s ease-out forwards;
  animation-delay: 0.5s;
  width: 0;
}

/* Slide Up */
@keyframes slide-up {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-slide-up {
  animation: slide-up 0.6s ease-out forwards;
  opacity: 0;
}

/* Rotate In */
@keyframes rotate-in {
  0% {
    opacity: 0;
    transform: rotate(-180deg) scale(0);
  }
  100% {
    opacity: 1;
    transform: rotate(0) scale(1);
  }
}

.animate-rotate-in {
  animation: rotate-in 0.6s ease-out forwards;
  opacity: 0;
}

/* Fade In */
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.animate-fade-in {
  animation: fade-in 0.8s ease-out forwards;
  opacity: 0;
}

/* Progress Bar Animation */
@keyframes progress-fill {
  0% {
    width: 0;
  }
  100% {
    width: var(--progress-width);
  }
}

.progress-bar {
  animation: progress-fill 1.5s cubic-bezier(0.4, 0, 0.2, 1) forwards;
  width: 0;
}

/* Shimmer Effect */
@keyframes shimmer {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(200%);
  }
}

.shimmer {
  animation: shimmer 2.5s ease-in-out infinite;
}

/* Skill Item Animation */
@keyframes skill-appear {
  0% {
    opacity: 0;
    transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.skill-item {
  animation: skill-appear 0.5s ease-out forwards;
  opacity: 0;
}

/* Percentage Counter Animation */
@keyframes count-up {
  0% {
    opacity: 0;
    transform: translateY(-10px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.skill-percentage {
  animation: count-up 0.5s ease-out forwards;
}

/* Soft Skills Badge Animation */
@keyframes badge-pop {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  50% {
    transform: scale(1.05);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

.soft-skill-badge {
  animation: badge-pop 0.4s ease-out forwards;
  opacity: 0;
}

/* Gentle Pulse */
@keyframes pulse-gentle {
  0%,
  100% {
    transform: scale(1);
    box-shadow: 0 0 0 0 rgba(168, 85, 247, 0.4);
  }
  50% {
    transform: scale(1.05);
    box-shadow: 0 0 0 10px rgba(168, 85, 247, 0);
  }
}

.animate-pulse-gentle {
  animation: pulse-gentle 2s ease-in-out infinite;
}

/* Card Hover Effect */
.skill-card {
  position: relative;
  overflow: hidden;
}

.skill-card::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(
    circle,
    rgba(34, 211, 238, 0.1) 0%,
    transparent 70%
  );
  opacity: 0;
  transition: opacity 0.5s ease;
}

.skill-card:hover::before {
  opacity: 1;
  animation: glow-rotate 3s linear infinite;
}

@keyframes glow-rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/* Scrollbar Styling */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: rgba(15, 23, 42, 0.5);
}

::-webkit-scrollbar-thumb {
  background: rgba(34, 211, 238, 0.3);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: rgba(34, 211, 238, 0.5);
}
</style>
