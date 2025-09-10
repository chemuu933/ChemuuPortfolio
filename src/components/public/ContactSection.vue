<template>
  <section id="contact" class="py-20 bg-gradient-to-br from-rose-100 via-pink-50 to-purple-100 relative overflow-hidden">
    <!-- Floating decorative elements -->
    <div class="absolute top-20 left-16 animate-float-hearts">
      <span class="text-4xl text-pink-300 opacity-30">💕</span>
    </div>
    <div class="absolute top-40 right-20 animate-float-sparkle">
      <span class="text-3xl text-rose-400 opacity-40">✨</span>
    </div>
    <div class="absolute bottom-32 left-1/4 animate-float-butterfly">
      <span class="text-2xl text-purple-400 opacity-35">🦋</span>
    </div>
    <div class="absolute bottom-16 right-1/3 animate-float-flower">
      <span class="text-3xl text-pink-400 opacity-30">🌸</span>
    </div>
    <div class="absolute top-60 left-1/2 animate-float-star">
      <span class="text-2xl text-rose-300 opacity-25">⭐</span>
    </div>

    <div class="container mx-auto px-6 relative z-10">
      <div class="text-center mb-16 animate-fade-in-up">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 animate-slide-down">
          💌 Get In Touch 💌
        </h2>
        <div class="w-20 h-1 bg-gradient-to-r from-pink-400 via-rose-500 to-purple-500 mx-auto rounded-full animate-expand-line"></div>
        <p class="text-gray-700 mt-6 max-w-2xl mx-auto text-lg animate-fade-in" style="animation-delay: 0.3s">
          Have a project in mind or want to discuss potential opportunities? I'd
          love to hear from you! 🌟
        </p>
      </div>

      <div class="flex flex-col lg:flex-row gap-10">
        <!-- Contact Form -->
        <div class="lg:w-1/2 animate-slide-in-left">
          <form
            @submit.prevent="submitForm"
            class="bg-white/80 backdrop-blur-sm p-8 rounded-2xl shadow-2xl border border-white/50 hover:shadow-3xl transition-all duration-500"
          >
            <div class="mb-6 animate-input-appear" style="animation-delay: 0.1s">
              <label for="name" class="block text-gray-800 font-medium mb-3 flex items-center">
                <span class="text-pink-500 mr-2">👤</span>
                Your Name
              </label>
              <input
                type="text"
                id="name"
                v-model="contactForm.name"
                class="w-full px-4 py-3 border-2 border-pink-200 rounded-xl focus:ring-2 focus:ring-pink-400 focus:border-pink-400 outline-none transition-all duration-300 bg-white/90 hover:bg-white focus:bg-white hover:border-pink-300"
                placeholder="June chemuu"
                required
              />
            </div>

            <div class="mb-6 animate-input-appear" style="animation-delay: 0.2s">
              <label for="email" class="block text-gray-800 font-medium mb-3 flex items-center">
                <span class="text-rose-500 mr-2">💌</span>
                Your Email
              </label>
              <input
                type="email"
                id="email"
                v-model="contactForm.email"
                class="w-full px-4 py-3 border-2 border-pink-200 rounded-xl focus:ring-2 focus:ring-pink-400 focus:border-pink-400 outline-none transition-all duration-300 bg-white/90 hover:bg-white focus:bg-white hover:border-pink-300"
                placeholder="chemuu579@gmail.com"
                required
              />
            </div>

            <div class="mb-6 animate-input-appear" style="animation-delay: 0.3s">
              <label for="subject" class="block text-gray-800 font-medium mb-3 flex items-center">
                <span class="text-purple-500 mr-2">📋</span>
                Subject
              </label>
              <input
                type="text"
                id="subject"
                v-model="contactForm.subject"
                class="w-full px-4 py-3 border-2 border-pink-200 rounded-xl focus:ring-2 focus:ring-pink-400 focus:border-pink-400 outline-none transition-all duration-300 bg-white/90 hover:bg-white focus:bg-white hover:border-pink-300"
                placeholder="Project Inquiry"
                required
              />
            </div>

            <div class="mb-6 animate-input-appear" style="animation-delay: 0.4s">
              <label for="message" class="block text-gray-800 font-medium mb-3 flex items-center">
                <span class="text-pink-500 mr-2">💭</span>
                Message
              </label>
              <textarea
                id="message"
                v-model="contactForm.message"
                rows="5"
                class="w-full px-4 py-3 border-2 border-pink-200 rounded-xl focus:ring-2 focus:ring-pink-400 focus:border-pink-400 outline-none transition-all duration-300 bg-white/90 hover:bg-white focus:bg-white hover:border-pink-300 resize-none"
                placeholder="Your message here..."
                required
              ></textarea>
            </div>

            <button
              type="submit"
              class="w-full bg-gradient-to-r from-pink-400 via-rose-500 to-purple-500 hover:from-pink-500 hover:via-rose-600 hover:to-purple-600 text-white py-4 px-6 rounded-xl font-medium transition-all duration-300 transform hover:scale-105 hover:shadow-xl animate-button-appear relative overflow-hidden group"
              :disabled="formSubmitting"
              style="animation-delay: 0.5s"
            >
              <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent -skew-x-12 group-hover:animate-shimmer"></div>
              <span v-if="formSubmitting" class="flex items-center justify-center">
                <i class="fas fa-spinner fa-spin mr-2"></i> Sending Magic... ✨
              </span>
              <span v-else class="flex items-center justify-center">
                <span class="mr-2">Send Message</span> 🚀
              </span>
            </button>

            <div
              v-if="formSuccess"
              class="mt-6 p-4 bg-gradient-to-r from-green-100 to-emerald-100 text-green-800 rounded-xl border border-green-200 animate-success-bounce"
            >
              <div class="flex items-center">
                <span class="text-2xl mr-3">🎉</span>
                <div>
                  <p class="font-medium">Thank you!</p>
                  <p class="text-sm">Your message has been sent successfully.</p>
                </div>
              </div>
            </div>
          </form>
        </div>

        <!-- Contact Information -->
        <div class="lg:w-1/2 animate-slide-in-right">
          <div class="bg-white/80 backdrop-blur-sm p-8 rounded-2xl shadow-2xl h-full border border-white/50 hover:shadow-3xl transition-all duration-500">
            <h3 class="text-2xl font-semibold text-gray-800 mb-8 animate-fade-in flex items-center" style="animation-delay: 0.2s">
              <span class="text-3xl mr-3">📞</span>
              Contact Information
            </h3>

            <div class="space-y-6">
              <div class="flex items-start animate-contact-item group cursor-pointer" style="animation-delay: 0.3s">
                <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-pink-100 to-rose-200 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fas fa-envelope text-pink-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="text-lg font-medium text-gray-800 mb-1">Email</h4>
                  <a
                    href="mailto:jemutaic18@gmail.com"
                    class="text-pink-600 hover:text-pink-700 hover:underline transition-colors duration-300 font-medium"
                  >jemutaic18@gmail.com</a>
                </div>
              </div>

              <div class="flex items-start animate-contact-item group cursor-pointer" style="animation-delay: 0.4s">
                <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-rose-100 to-pink-200 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fas fa-map-marker-alt text-rose-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="text-lg font-medium text-gray-800 mb-1">Location</h4>
                  <p class="text-gray-600">Nakuru, Kenya 🇰🇪</p>
                </div>
              </div>

              <div class="flex items-start animate-contact-item group cursor-pointer" style="animation-delay: 0.5s">
                <div class="w-14 h-14 rounded-2xl bg-gradient-to-br from-purple-100 to-pink-200 flex items-center justify-center mr-4 group-hover:scale-110 transition-transform duration-300 shadow-lg">
                  <i class="fas fa-clock text-purple-600 text-xl"></i>
                </div>
                <div>
                  <h4 class="text-lg font-medium text-gray-800 mb-1">Availability</h4>
                  <p class="text-gray-600">Monday - Friday, 9:00 AM - 5:00 PM EAT ⏰</p>
                </div>
              </div>
            </div>

            <div class="mt-10 animate-fade-in" style="animation-delay: 0.6s">
              <h4 class="text-lg font-medium text-gray-800 mb-6 flex items-center">
                <span class="text-2xl mr-2">🔗</span>
                Connect With Me
              </h4>
              <div class="flex flex-wrap gap-4">
                <a
                  href="https://github.com/"
                  target="_blank"
                  class="w-14 h-14 rounded-2xl bg-gradient-to-br from-gray-700 to-gray-900 hover:from-gray-800 hover:to-black flex items-center justify-center text-white transition-all duration-300 transform hover:scale-110 hover:shadow-xl group"
                >
                  <i class="fab fa-github text-xl group-hover:animate-bounce"></i>
                </a>
                <a
                  href="https://linkedin.com/"
                  target="_blank"
                  class="w-14 h-14 rounded-2xl bg-gradient-to-br from-blue-600 to-blue-800 hover:from-blue-700 hover:to-blue-900 flex items-center justify-center text-white transition-all duration-300 transform hover:scale-110 hover:shadow-xl group"
                >
                  <i class="fab fa-linkedin-in text-xl group-hover:animate-bounce"></i>
                </a>
                <a
                  href="https://twitter.com/"
                  target="_blank"
                  class="w-14 h-14 rounded-2xl bg-gradient-to-br from-blue-400 to-blue-600 hover:from-blue-500 hover:to-blue-700 flex items-center justify-center text-white transition-all duration-300 transform hover:scale-110 hover:shadow-xl group"
                >
                  <i class="fab fa-twitter text-xl group-hover:animate-bounce"></i>
                </a>
                <a
                  href="https://codepen.io/"
                  target="_blank"
                  class="w-14 h-14 rounded-2xl bg-gradient-to-br from-gray-900 to-black hover:from-black hover:to-gray-900 flex items-center justify-center text-white transition-all duration-300 transform hover:scale-110 hover:shadow-xl group"
                >
                  <i class="fab fa-codepen text-xl group-hover:animate-bounce"></i>
                </a>
              </div>
            </div>

            <div class="mt-10 animate-fade-in" style="animation-delay: 0.7s">
              <a
                href="#"
                class="inline-flex items-center bg-gradient-to-r from-purple-400 via-pink-500 to-rose-500 hover:from-purple-500 hover:via-pink-600 hover:to-rose-600 text-white py-4 px-6 rounded-xl font-medium transition-all duration-300 transform hover:scale-105 hover:shadow-xl relative overflow-hidden group"
              >
                <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent -skew-x-12 group-hover:animate-shimmer"></div>
                <i class="fas fa-download mr-2 group-hover:animate-bounce"></i> 
                <span>Download Resume</span>
                <span class="ml-2">📄</span>
              </a>
            </div>
          </div>
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
/* Floating animations */
@keyframes float-hearts {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(10deg); }
}

@keyframes float-sparkle {
  0%, 100% { transform: translateY(0px) scale(1); }
  50% { transform: translateY(-15px) scale(1.2); }
}

@keyframes float-butterfly {
  0%, 100% { transform: translateY(0px) translateX(0px); }
  33% { transform: translateY(-10px) translateX(5px); }
  66% { transform: translateY(-5px) translateX(-5px); }
}

@keyframes float-flower {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-18px) rotate(180deg); }
}

@keyframes float-star {
  0%, 100% { transform: translateY(0px) scale(1) rotate(0deg); }
  50% { transform: translateY(-12px) scale(1.1) rotate(90deg); }
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
    transform: scale(0.9);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes contact-item {
  0% {
    opacity: 0;
    transform: translateX(20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes success-bounce {
  0% {
    opacity: 0;
    transform: scale(0.8) translateY(20px);
  }
  50% {
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

/* Apply animations */
.animate-float-hearts { animation: float-hearts 4s ease-in-out infinite; }
.animate-float-sparkle { animation: float-sparkle 3s ease-in-out infinite; }
.animate-float-butterfly { animation: float-butterfly 5s ease-in-out infinite; }
.animate-float-flower { animation: float-flower 6s ease-in-out infinite; }
.animate-float-star { animation: float-star 4.5s ease-in-out infinite; }

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

/* Enhanced hover effects */
.group:hover .group-hover\:scale-110 {
  transform: scale(1.1);
}

.group:hover .group-hover\:animate-bounce {
  animation: bounce 0.6s ease-in-out;
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #f1f5f9;
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(45deg, #f472b6, #ec4899);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(45deg, #ec4899, #db2777);
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Remove number input arrows */
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

input[type="number"] {
  appearance: textfield;
  -moz-appearance: textfield;
}
</style>