<template>
  <section id="skills" class="py-20 bg-slate-400">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
          My Skills
        </h2>
        <div class="w-20 h-1 bg-indigo-600 mx-auto"></div>
        <p class="text-neutral-900 mt-4 max-w-2xl mx-auto">
          I've developed expertise in various technologies throughout my
          education and personal projects.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
        <!-- Technical Skills -->
        <div class="bg-gray-50 rounded-xl shadow-lg p-8">
          <h3 class="text-2xl font-semibold text-gray-800 mb-6">
            Technical Skills
          </h3>

          <div
            v-for="(skill, index) in technicalSkills"
            :key="`tech-${index}`"
            class="mb-6"
          >
            <div class="flex justify-between mb-2">
              <span class="text-gray-700 font-medium">{{ skill.name }}</span>
              <span class="text-indigo-600 font-medium"
                >{{ skill.level }}%</span
              >
            </div>
            <div class="w-full bg-gray-200 rounded-full h-2.5">
              <div
                class="bg-indigo-600 h-2.5 rounded-full"
                :style="{ width: `${skill.level}%` }"
              ></div>
            </div>
          </div>
        </div>
    
        <div class="bg-gray-50 rounded-xl shadow-lg p-8">
          <h3 class="text-2xl font-semibold text-gray-800 mb-6">
            Additional Skills
          </h3>

          <div class="grid grid-cols-2 gap-4">
            <div
              v-for="(skill, index) in softSkills"
              :key="`soft-${index}`"
              class="bg-white rounded-lg p-4 shadow-md flex items-center transition-all duration-300 hover:shadow-lg hover:translate-y-[-2px]"
            >
              <div
                class="w-10 h-10 rounded-full bg-indigo-100 flex items-center justify-center mr-3"
              >
                <i :class="`fas ${skill.icon} text-indigo-600`"></i>
              </div>
              <span class="text-gray-700">{{ skill.name }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang="ts" setup>
const technicalSkills = [
  { name: 'HTML/CSS', level: 90 },
  { name: 'JavaScript', level: 85 },
  { name: 'React', level: 80 },
  { name: 'Vue.js', level: 75 },
  { name: 'Express.js', level: 70 },
  { name: 'Responsive Design', level: 85 }
];


const softSkills = [
  { name: 'Problem Solving', icon: 'fa-lightbulb' },
  { name: 'Team Collaboration', icon: 'fa-users' },
  { name: 'Git/Version Control', icon: 'fa-code-branch' },
  { name: 'UI/UX Design', icon: 'fa-pencil-ruler' },
  { name: 'Database Management', icon: 'fa-database' },
  { name: 'Agile Methodology', icon: 'fa-tasks' },
  { name: 'RESTful APIs', icon: 'fa-server' },
  { name: 'Testing/Debugging', icon: 'fa-bug' }
];
</script>
