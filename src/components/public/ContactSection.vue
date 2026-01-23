<template>
  <section id="contact" class="py-20 bg-gradient-to-br from-slate-900 via-slate-800 to-slate-900 relative overflow-hidden">
    <!-- Animated background elements -->
    <div class="absolute inset-0 opacity-30">
      <div class="absolute top-20 left-20 w-96 h-96 bg-cyan-500/20 rounded-full blur-3xl animate-pulse-slow"></div>
      <div class="absolute bottom-20 right-20 w-96 h-96 bg-teal-500/20 rounded-full blur-3xl animate-pulse-slower"></div>
      <div class="absolute top-1/2 left-1/2 w-96 h-96 bg-blue-500/10 rounded-full blur-3xl animate-float"></div>
    </div>

    <!-- Grid pattern overlay -->
    <div class="absolute inset-0 opacity-5" style="background-image: linear-gradient(#14b8a6 1px, transparent 1px), linear-gradient(90deg, #14b8a6 1px, transparent 1px); background-size: 50px 50px;"></div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center mb-16 animate-fade-in-up">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-4 animate-slide-down">
          Get In Touch
        </h2>
        <div class="w-20 h-1 bg-gradient-to-r from-cyan-400 to-teal-500 mx-auto rounded-full animate-expand-line"></div>
        <p class="text-gray-300 mt-6 max-w-2xl mx-auto text-lg animate-fade-in" style="animation-delay: 0.3s">
          Have a project in mind or want to discuss potential opportunities? I'd
          love to hear from you!
        </p>
      </div>

      <div class="flex flex-col lg:flex-row gap-10">
        <!-- Contact Information -->
        <div class="lg:w-2/5 animate-slide-in-left">
          <div class="bg-slate-800/50 backdrop-blur-xl p-8 rounded-3xl border border-slate-700/50 hover:border-cyan-500/30 transition-all duration-500 h-full shadow-2xl">
            
            <!-- Contact Info Cards -->
            <div class="space-y-6 mb-10">
              <div class="flex items-center animate-contact-item bg-slate-700/30 p-5 rounded-2xl border border-slate-600/30 hover:border-cyan-500/50 hover:bg-slate-700/50 transition-all duration-300 group cursor-pointer" style="animation-delay: 0.1s">
                <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-cyan-400 to-teal-500 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300 shadow-lg shadow-cyan-500/20">
                  <i class="fas fa-envelope text-slate-900 text-xl"></i>
                </div>
                <div>
                  <h4 class="text-sm font-medium text-gray-400 mb-1">Email</h4>
                  <a
                    href="mailto:jemutaic18@gmail.com"
                    class="text-white hover:text-cyan-400 transition-colors duration-300 font-medium"
                  >jemutaic18@gmail.com</a>
                </div>
              </div>

              <div class="flex items-center animate-contact-item bg-slate-700/30 p-5 rounded-2xl border border-slate-600/30 hover:border-cyan-500/50 hover:bg-slate-700/50 transition-all duration-300 group cursor-pointer" style="animation-delay: 0.2s">
                <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-cyan-400 to-teal-500 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300 shadow-lg shadow-cyan-500/20">
                  <i class="fas fa-phone text-slate-900 text-xl"></i>
                </div>
                <div>
                  <h4 class="text-sm font-medium text-gray-400 mb-1">Phone</h4>
                  <p class="text-white">+254708345963</p>
                </div>
              </div>

              <div class="flex items-center animate-contact-item bg-slate-700/30 p-5 rounded-2xl border border-slate-600/30 hover:border-cyan-500/50 hover:bg-slate-700/50 transition-all duration-300 group cursor-pointer" style="animation-delay: 0.3s">
                <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-cyan-400 to-teal-500 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300 shadow-lg shadow-cyan-500/20">
                  <i class="fas fa-map-marker-alt text-slate-900 text-xl"></i>
                </div>
                <div>
                  <h4 class="text-sm font-medium text-gray-400 mb-1">Location</h4>
                  <p class="text-white">Nakuru, Kenya 🇰🇪</p>
                </div>
              </div>
            </div>

            <!-- Social Links -->
            <div class="animate-fade-in" style="animation-delay: 0.4s">
              <h4 class="text-lg font-medium text-white mb-6">Follow Me</h4>
              <div class="flex flex-wrap gap-4">
                <a
                  href="https://github.com/chemuu933/"
                  target="_blank"
                  class="w-12 h-12 rounded-xl bg-slate-700/50 hover:bg-slate-600 border border-slate-600/50 hover:border-cyan-500/50 flex items-center justify-center text-gray-300 hover:text-cyan-400 transition-all duration-300 transform hover:scale-110 hover:shadow-lg hover:shadow-cyan-500/20 group"
                >
                  <i class="fab fa-github text-lg group-hover:animate-bounce"></i>
                </a>
                <a
                  href="https://linkedin.com/"
                  target="_blank"
                  class="w-12 h-12 rounded-xl bg-slate-700/50 hover:bg-slate-600 border border-slate-600/50 hover:border-cyan-500/50 flex items-center justify-center text-gray-300 hover:text-cyan-400 transition-all duration-300 transform hover:scale-110 hover:shadow-lg hover:shadow-cyan-500/20 group"
                >
                  <i class="fab fa-linkedin-in text-lg group-hover:animate-bounce"></i>
                </a>
                <a
                  href="https://twitter.com/"
                  target="_blank"
                  class="w-12 h-12 rounded-xl bg-slate-700/50 hover:bg-slate-600 border border-slate-600/50 hover:border-cyan-500/50 flex items-center justify-center text-gray-300 hover:text-cyan-400 transition-all duration-300 transform hover:scale-110 hover:shadow-lg hover:shadow-cyan-500/20 group"
                >
                  <i class="fab fa-twitter text-lg group-hover:animate-bounce"></i>
                </a>
                <a
                  href="https://dribbble.com/"
                  target="_blank"
                  class="w-12 h-12 rounded-xl bg-slate-700/50 hover:bg-slate-600 border border-slate-600/50 hover:border-cyan-500/50 flex items-center justify-center text-gray-300 hover:text-cyan-400 transition-all duration-300 transform hover:scale-110 hover:shadow-lg hover:shadow-cyan-500/20 group"
                >
                  <i class="fab fa-dribbble text-lg group-hover:animate-bounce"></i>
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="lg:w-3/5 animate-slide-in-right">
          <form
            @submit.prevent="submitForm"
            class="bg-slate-800/50 backdrop-blur-xl p-8 rounded-3xl border border-slate-700/50 hover:border-cyan-500/30 transition-all duration-500 shadow-2xl"
          >
            <div class="mb-6 animate-input-appear" style="animation-delay: 0.1s">
              <label for="name" class="block text-white font-medium mb-3">
                Your Name
              </label>
              <input
                type="text"
                id="name"
                v-model="contactForm.name"
                class="w-full px-5 py-4 bg-slate-700/50 border border-slate-600/50 rounded-xl focus:ring-2 focus:ring-cyan-500 focus:border-cyan-500 outline-none transition-all duration-300 text-white placeholder-gray-500 hover:bg-slate-700 hover:border-slate-500"
                placeholder="June chemuu"
                required
              />
            </div>

            <div class="mb-6 animate-input-appear" style="animation-delay: 0.2s">
              <label for="email" class="block text-white font-medium mb-3">
                Email Address
              </label>
              <input
                type="email"
                id="email"
                v-model="contactForm.email"
                class="w-full px-5 py-4 bg-slate-700/50 border border-slate-600/50 rounded-xl focus:ring-2 focus:ring-cyan-500 focus:border-cyan-500 outline-none transition-all duration-300 text-white placeholder-gray-500 hover:bg-slate-700 hover:border-slate-500"
                placeholder="chemuu579@gmail.com"
                required
              />
            </div>

            <div class="mb-6 animate-input-appear" style="animation-delay: 0.3s">
              <label for="subject" class="block text-white font-medium mb-3">
                Subject
              </label>
              <input
                type="text"
                id="subject"
                v-model="contactForm.subject"
                class="w-full px-5 py-4 bg-slate-700/50 border border-slate-600/50 rounded-xl focus:ring-2 focus:ring-cyan-500 focus:border-cyan-500 outline-none transition-all duration-300 text-white placeholder-gray-500 hover:bg-slate-700 hover:border-slate-500"
                placeholder="Project Inquiry"
                required
              />
            </div>

            <div class="mb-6 animate-input-appear" style="animation-delay: 0.4s">
              <label for="message" class="block text-white font-medium mb-3">
                Message
              </label>
              <textarea
                id="message"
                v-model="contactForm.message"
                rows="5"
                class="w-full px-5 py-4 bg-slate-700/50 border border-slate-600/50 rounded-xl focus:ring-2 focus:ring-cyan-500 focus:border-cyan-500 outline-none transition-all duration-300 text-white placeholder-gray-500 hover:bg-slate-700 hover:border-slate-500 resize-none"
                placeholder="Tell me about your project..."
                required
              ></textarea>
            </div>

            <button
              type="submit"
              class="w-full bg-gradient-to-r from-cyan-500 to-teal-500 hover:from-cyan-600 hover:to-teal-600 text-white py-4 px-6 rounded-xl font-medium transition-all duration-300 transform hover:scale-105 hover:shadow-xl hover:shadow-cyan-500/30 animate-button-appear relative overflow-hidden group"
              :disabled="formSubmitting"
              style="animation-delay: 0.5s"
            >
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent -skew-x-12 group-hover:animate-shimmer"></div>
              <span v-if="formSubmitting" class="flex items-center justify-center">
                <i class="fas fa-spinner fa-spin mr-2"></i> Sending...
              </span>
              <span v-else class="flex items-center justify-center">
                <span class="mr-2">Send Message</span>
                <i class="fas fa-paper-plane"></i>
              </span>
            </button>

            <div
              v-if="formSuccess"
              class="mt-6 p-4 bg-gradient-to-r from-emerald-500/20 to-teal-500/20 border border-emerald-500/30 text-emerald-300 rounded-xl animate-success-bounce"
            >
              <div class="flex items-center">
                <i class="fas fa-check-circle text-2xl mr-3"></i>
                <div>
                  <p class="font-medium">Thank you!</p>
                  <p class="text-sm">Your message has been sent successfully.</p>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const contactForm = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
});

const formSubmitting = ref(false);
const formSuccess = ref(false);

const submitForm = () => {
  formSubmitting.value = true;
  
  // Simulate form submission
  setTimeout(() => {
    formSubmitting.value = false;
    formSuccess.value = true;
    
    // Reset form
    contactForm.value = {
      name: '',
      email: '',
      subject: '',
      message: ''
    };
    
    // Hide success message after 5 seconds
    setTimeout(() => {
      formSuccess.value = false;
    }, 5000);
  }, 1500);
};
</script>

<style scoped>
/* Background animations */
@keyframes pulse-slow {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(1.1); }
}

@keyframes pulse-slower {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 0.6; transform: scale(1.15); }
}

@keyframes float {
  0%, 100% { transform: translate(-50%, -50%) translateY(0px); }
  50% { transform: translate(-50%, -50%) translateY(-20px); }
}

.animate-pulse-slow {
  animation: pulse-slow 8s ease-in-out infinite;
}

.animate-pulse-slower {
  animation: pulse-slower 10s ease-in-out infinite;
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

/* Main animations */
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
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
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

@keyframes input-appear {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes button-appear {
  0% {
    opacity: 0;
    transform: scale(0.95);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes contact-item {
  0% {
    opacity: 0;
    transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes success-bounce {
  0% {
    opacity: 0;
    transform: scale(0.9) translateY(20px);
  }
  60% {
    transform: scale(1.05) translateY(-5px);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}

@keyframes shimmer {
  0% { transform: translateX(-100%) skewX(-12deg); }
  100% { transform: translateX(200%) skewX(-12deg); }
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-5px); }
}

/* Apply animations */
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

.animate-input-appear {
  animation: input-appear 0.6s ease-out forwards;
  opacity: 0;
}

.animate-button-appear {
  animation: button-appear 0.6s ease-out forwards;
  opacity: 0;
}

.animate-contact-item {
  animation: contact-item 0.6s ease-out forwards;
  opacity: 0;
}

.animate-success-bounce {
  animation: success-bounce 0.8s ease-out forwards;
}

.animate-shimmer {
  animation: shimmer 1.5s ease-in-out;
}

.group:hover .group-hover\:animate-bounce {
  animation: bounce 0.6s ease-in-out;
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #1e293b;
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(45deg, #06b6d4, #14b8a6);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(45deg, #0891b2, #0d9488);
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Focus styles */
input:focus,
textarea:focus {
  box-shadow: 0 0 0 3px rgba(6, 182, 212, 0.1);
}

/* Disabled button state */
button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
  transform: none !important;
}
</style>