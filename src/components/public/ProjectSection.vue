<template>
  <section id="projects" class="py-20 bg-slate-400">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
          My Projects
        </h2>
        <div class="w-20 h-1 bg-indigo-600 mx-auto"></div>
        <p class="text-gray-600 mt-4 max-w-2xl mx-auto">
          Here are some of the projects I've worked on. Each one represents
          different skills and challenges I've tackled.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="bg-white rounded-xl overflow-hidden shadow-lg transition-all duration-300 hover:shadow-xl hover:translate-y-[-5px]"
        >
          <div class="h-48 overflow-hidden">
            <img
              :src="project.image"
              :alt="project.title"
              class="w-full h-full object-cover object-top transition-transform duration-500 hover:scale-110"
            />
          </div>
          <div class="p-6">
            <h3 class="text-xl font-bold text-gray-800 mb-2">
              {{ project.title }}
            </h3>
            <p class="text-gray-600 mb-4">{{ project.description }}</p>
            <div class="flex flex-wrap gap-2 mb-4">
              <span
                v-for="(tech, techIndex) in project.technologies"
                :key="techIndex"
                class="bg-indigo-100 text-indigo-800 text-xs px-3 py-1 rounded-full"
              >
                {{ tech }}
              </span>
            </div>
            <div class="flex space-x-3">
              <a
                :href="project.demoLink"
                target="_blank"
                class="bg-indigo-600 hover:bg-indigo-700 text-white px-4 py-2 rounded text-sm font-medium transition !rounded-button whitespace-nowrap cursor-pointer"
              >
                <i class="fas fa-external-link-alt mr-1"></i> Live Demo
              </a>
              <a
                :href="project.githubLink"
                target="_blank"
                class="bg-gray-800 hover:bg-gray-900 text-white px-4 py-2 rounded text-sm font-medium transition !rounded-button whitespace-nowrap cursor-pointer"
              >
                <i class="fab fa-github mr-1"></i> GitHub
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
const projects = [
  {
    title: 'E-Commerce Platform',
    description: 'A full-featured online store with product catalog, cart functionality, and payment processing.',
    technologies: ['React', 'Node.js', 'Express', 'MongoDB'],
    image: 'https://readdy.ai/api/search-image?query=modern%20e-commerce%20website%20interface%20on%20laptop%20screen%2C%20clean%20design%2C%20product%20grid%20layout%2C%20shopping%20cart%20icon%2C%20professional%20web%20design%2C%20high%20quality&width=600&height=400&seq=4&orientation=landscape',
    demoLink: '#',
    githubLink: '#'
  },
  {
    title: 'Task Management App',
    description: 'A productivity application for organizing tasks with drag-and-drop functionality and team collaboration features.',
    technologies: ['Vue.js', 'Vuex', 'Firebase'],
    image: 'https://readdy.ai/api/search-image?query=task%20management%20application%20interface%20with%20kanban%20board%2C%20task%20cards%2C%20clean%20modern%20UI%20design%2C%20productivity%20app%20on%20desktop%20screen%2C%20professional&width=600&height=400&seq=5&orientation=landscape',
    demoLink: '#',
    githubLink: '#'
  },
  {
    title: 'Weather Dashboard',
    description: 'Real-time weather application with forecast data, location search, and interactive maps.',
    technologies: ['JavaScript', 'API Integration', 'CSS'],
    image: 'https://readdy.ai/api/search-image?query=weather%20dashboard%20application%20showing%20forecast%2C%20temperature%20graphs%2C%20location%20search%2C%20clean%20modern%20UI%20design%2C%20professional%20web%20interface&width=600&height=400&seq=6&orientation=landscape',
    demoLink: '#',
    githubLink: '#'
  },
  {
    title: 'Recipe Finder',
    description: 'A web application that helps users discover recipes based on available ingredients and dietary preferences.',
    technologies: ['React', 'API Integration', 'Responsive Design'],
    image: 'https://readdy.ai/api/search-image?query=recipe%20finder%20application%20interface%20showing%20food%20images%2C%20search%20filters%2C%20ingredient%20lists%2C%20clean%20modern%20UI%20design%2C%20culinary%20web%20app&width=600&height=400&seq=7&orientation=landscape',
    demoLink: '#',
    githubLink: '#'
  },
  {
    title: 'Portfolio Website',
    description: 'A personal portfolio website showcasing projects and skills with a modern, responsive design.',
    technologies: ['HTML/CSS', 'JavaScript', 'Vue.js'],
    image: 'https://readdy.ai/api/search-image?query=portfolio%20website%20design%20with%20project%20showcase%20grid%2C%20about%20section%2C%20skills%20visualization%2C%20professional%20web%20design%2C%20clean%20modern%20interface&width=600&height=400&seq=8&orientation=landscape',
    demoLink: '#',
    githubLink: '#'
  },
  {
    title: 'Fitness Tracker',
    description: 'An application for tracking workouts, setting fitness goals, and visualizing progress over time.',
    technologies: ['Vue.js', 'Chart.js', 'Firebase'],
    image: 'https://readdy.ai/api/search-image?query=fitness%20tracking%20application%20with%20workout%20logs%2C%20progress%20charts%2C%20goal%20setting%20interface%2C%20clean%20modern%20UI%20design%2C%20health%20app%20on%20devices&width=600&height=400&seq=9&orientation=landscape',
    demoLink: '#',
    githubLink: '#'
  }
];

// Timeline data
const timeline = [
  {
    date: '2025 - Present',
    title: 'IT Student, Advanced Web Development',
    description: 'Focusing on advanced web technologies and full-stack development, maintaining a 3.9 GPA.',
    icon: 'fa-graduation-cap'
  },
  {
    date: '2024 - 2025',
    title: 'Web Development Intern',
    description: 'Contributed to front-end development for client projects using React and Vue.js frameworks.',
    icon: 'fa-briefcase'
  },
  {
    date: '2023 - 2024',
    title: 'IT Student, Fundamentals',
    description: 'Completed foundational courses in programming, databases, and web development basics.',
    icon: 'fa-graduation-cap'
  },
  {
    date: '2023',
    title: 'First Coding Project',
    description: 'Built my first responsive website using HTML, CSS, and JavaScript, sparking my passion for web development.',
    icon: 'fa-code'
  }
]
</script>
