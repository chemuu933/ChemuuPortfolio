<template>   
  <section id="about" class="py-20 bg-gradient-to-br from-pink-100 via-rose-50 to-pink-200 relative overflow-hidden">
    <!-- Floating decorative elements -->
    <div class="absolute top-10 left-10 animate-float-slow">
      <div class="w-8 h-8 bg-pink-300 rounded-full opacity-30"></div>
    </div>
    <div class="absolute top-32 right-20 animate-float-medium">
      <div class="w-6 h-6 bg-rose-400 rounded-full opacity-40"></div>
    </div>
    <div class="absolute bottom-20 left-1/4 animate-float-fast">
      <div class="w-4 h-4 bg-pink-400 rounded-full opacity-35"></div>
    </div>
    
    <div class="container mx-auto px-6 relative z-10">       
      <div class="text-center mb-16 animate-fade-in-up">         
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 animate-slide-in-title">           
          ✨ About Me ✨        
        </h2>         
        <div class="w-20 h-1 bg-gradient-to-r from-pink-400 to-rose-500 mx-auto rounded-full animate-expand-line"></div>       
      </div>       
      
      <div class="flex flex-col lg:flex-row items-center gap-8 lg:gap-12">         
        <div class="lg:w-1/2 mb-10 lg:mb-0 animate-slide-in-left">           
          <div class="relative group">
            <div class="absolute -inset-4 bg-gradient-to-r from-pink-400 to-rose-500 rounded-2xl blur-xl opacity-30 group-hover:opacity-50 transition-opacity duration-500 animate-pulse-bg"></div>
            <img             
              :src="aboutImageUrl"             
              alt="Christine working on code"             
              class="relative rounded-2xl shadow-2xl w-full h-auto max-w-md mx-auto object-cover object-top transform hover:scale-105 transition-transform duration-500 border-4 border-white"           
            />
            <div class="absolute top-4 right-4 bg-white bg-opacity-90 rounded-full p-2 animate-bounce-gentle">
              <span class="text-2xl">💖</span>
            </div>
          </div>          
        </div>         
        
        <div class="lg:w-1/2 animate-slide-in-right">           
          <h3 class="text-2xl md:text-3xl font-semibold text-gray-800 mb-6 animate-fade-in-up" style="animation-delay: 0.2s">
            🌸 Who I Am
          </h3>           
          <p class="text-gray-700 mb-6 leading-relaxed text-base md:text-lg animate-fade-in-up hover:text-gray-800 transition-colors duration-300" style="animation-delay: 0.3s">             
            I'm Christine, an ambitious IT professional passionate about creating             
            meaningful digital experiences through code. My journey in             
            technology began with a curiosity about how websites work, which led             
            me to pursue formal education in Information Technology. 💻          
          </p>           
          <p class="text-gray-700 mb-6 leading-relaxed text-base md:text-lg animate-fade-in-up hover:text-gray-800 transition-colors duration-300" style="animation-delay: 0.4s">             
            Currently focused on frontend development, I enjoy the challenge             
            of building applications from the ground up. My experience spans             
            front-end technologies like HTML, CSS, JavaScript, React, and             
            Vue.js, as well as back-end work with Node.js and Express.js. ✨           
          </p>           
          <p class="text-gray-700 mb-8 leading-relaxed text-base md:text-lg animate-fade-in-up hover:text-gray-800 transition-colors duration-300" style="animation-delay: 0.5s">             
            When I'm not coding, I'm expanding my knowledge through online             
            courses, contributing to open-source projects, and staying updated             
            with the latest tech trends. I believe in continuous learning and             
            pushing the boundaries of what's possible with technology. 🚀           
          </p>           
          
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 animate-fade-in-up" style="animation-delay: 0.6s">             
            <div class="flex items-center bg-white bg-opacity-80 backdrop-blur-sm px-4 py-3 rounded-xl shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-all duration-300 animate-card-hover group">               
              <i class="fas fa-graduation-cap text-pink-500 mr-3 text-lg group-hover:scale-110 transition-transform duration-300"></i>               
              <span class="text-gray-800 font-medium text-sm md:text-base">IT Professional</span>             
            </div>             
            <div class="flex items-center bg-white bg-opacity-80 backdrop-blur-sm px-4 py-3 rounded-xl shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-all duration-300 animate-card-hover group" style="animation-delay: 0.1s">               
              <i class="fas fa-code text-rose-500 mr-3 text-lg group-hover:scale-110 transition-transform duration-300"></i>               
              <span class="text-gray-800 font-medium text-sm md:text-base">Frontend Developer</span>             
            </div>             
            <div class="flex items-center bg-white bg-opacity-80 backdrop-blur-sm px-4 py-3 rounded-xl shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-all duration-300 animate-card-hover group sm:col-span-2 lg:col-span-1" style="animation-delay: 0.2s">               
              <i class="fas fa-pencil-alt text-pink-400 mr-3 text-lg group-hover:scale-110 transition-transform duration-300"></i>               
              <span class="text-gray-800 font-medium text-sm md:text-base">UI/UX Designer</span>             
            </div>           
          </div>         
        </div>       
      </div>     
    </div>   
  </section> 
</template> 

<script lang="ts" setup> 
const aboutImageUrl = 'https://readdy.ai/api/search-image?query=young%20woman%20coding%20on%20laptop%20in%20modern%20workspace%2C%20focused%20on%20screen%20showing%20code%2C%20professional%20setting%2C%20soft%20natural%20lighting%2C%20high%20quality%2C%20tech%20environment&width=600&height=400&seq=3&orientation=landscape'; 
</script>

<style scoped>
@keyframes float-slow {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

@keyframes float-medium {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-15px) rotate(180deg); }
}

@keyframes float-fast {
  0%, 100% { transform: translateY(0px) scale(1); }
  50% { transform: translateY(-10px) scale(1.1); }
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

@keyframes bounce-gentle {
  0%, 20%, 53%, 80%, 100% { transform: translate3d(0,0,0) rotate(0deg); }
  40%, 43% { transform: translate3d(0,-8px,0) rotate(5deg); }
  70% { transform: translate3d(0,-4px,0) rotate(-3deg); }
  90% { transform: translate3d(0,-2px,0) rotate(1deg); }
}

@keyframes pulse-bg {
  0%, 100% { opacity: 0.3; }
  50% { opacity: 0.5; }
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

.animate-slide-in-left {
  animation: slide-in-left 1s ease-out forwards;
  opacity: 0;
}

.animate-slide-in-right {
  animation: slide-in-right 1s ease-out forwards;
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

.animate-bounce-gentle {
  animation: bounce-gentle 3s infinite;
}

.animate-pulse-bg {
  animation: pulse-bg 3s ease-in-out infinite;
}

.animate-card-hover {
  animation: card-hover 0.6s ease-out forwards;
  opacity: 0;
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