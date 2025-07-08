<template>
  <section id="contact" class="py-20 bg-slate-400">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
          Get In Touch
        </h2>
        <div class="w-20 h-1 bg-indigo-600 mx-auto"></div>
        <p class="text-gray-600 mt-4 max-w-2xl mx-auto">
          Have a project in mind or want to discuss potential opportunities? I'd
          love to hear from you!
        </p>
      </div>

      <div class="flex flex-col md:flex-row gap-10">
        <div class="md:w-1/2">
          <form
            @submit.prevent="submitForm"
            class="bg-white p-8 rounded-xl shadow-lg"
          >
            <div class="mb-6">
              <label for="name" class="block text-gray-700 font-medium mb-2"
                >Your Name</label
              >
              <input
                type="text"
                id="name"
                v-model="contactForm.name"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none transition"
                placeholder="June chemuu"
                required
              />
            </div>

            <div class="mb-6">
              <label for="email" class="block text-gray-700 font-medium mb-2"
                >Your Email</label
              >
              <input
                type="email"
                id="email"
                v-model="contactForm.email"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none transition"
                placeholder="chemuu579@gmail.com"
                required
              />
            </div>

            <div class="mb-6">
              <label for="subject" class="block text-gray-700 font-medium mb-2"
                >Subject</label
              >
              <input
                type="text"
                id="subject"
                v-model="contactForm.subject"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none transition"
                placeholder="Project Inquiry"
                required
              />
            </div>

            <div class="mb-6">
              <label for="message" class="block text-gray-700 font-medium mb-2"
                >Message</label
              >
              <textarea
                id="message"
                v-model="contactForm.message"
                rows="5"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500 outline-none transition"
                placeholder="Your message here..."
                required
              ></textarea>
            </div>

            <button
              type="submit"
              class="w-full bg-cyan-600 hover:bg-slate-600 text-white py-3 px-6 rounded-lg font-medium transition duration-300 !rounded-button whitespace-nowrap cursor-pointer"
              :disabled="formSubmitting"
            >
              <span v-if="formSubmitting">
                <i class="fas fa-spinner fa-spin mr-2"></i> Sending...
              </span>
              <span v-else>Send Message</span>
            </button>

            <div
              v-if="formSuccess"
              class="mt-4 p-3 bg-green-100 text-green-700 rounded-lg"
            >
              Thank you! Your message has been sent successfully.
            </div>
          </form>
        </div>

        <div class="md:w-1/2">
          <div class="bg-white p-8 rounded-xl shadow-lg h-full">
            <h3 class="text-2xl font-semibold text-gray-800 mb-6">
              Contact Information
            </h3>

            <div class="space-y-6">
              <div class="flex items-start">
                <div
                  class="w-12 h-12 rounded-full bg-indigo-100 flex items-center justify-center mr-4"
                >
                  <i class="fas fa-envelope text-indigo-600"></i>
                </div>
                <div>
                  <h4 class="text-lg font-medium text-gray-800">Email</h4>
                  <a
                    href="mailto:christine@example.com"
                    class="text-indigo-600 hover:underline"
                    >jemutaic18@gmail.com</a
                  >
                </div>
              </div>

              <div class="flex items-start">
                <div
                  class="w-12 h-12 rounded-full bg-indigo-100 flex items-center justify-center mr-4"
                >
                  <i class="fas fa-map-marker-alt text-indigo-600"></i>
                </div>
                <div>
                  <h4 class="text-lg font-medium text-gray-800">Location</h4>
                  <p class="text-gray-600">Nakuru, Kenya</p>
                </div>
              </div>

              <div class="flex items-start">
                <div
                  class="w-12 h-12 rounded-full bg-indigo-100 flex items-center justify-center mr-4"
                >
                  <i class="fas fa-clock text-indigo-600"></i>
                </div>
                <div>
                  <h4 class="text-lg font-medium text-gray-800">
                    Availability
                  </h4>
                  <p class="text-gray-600">
                    Monday - Friday, 9:00 AM - 5:00 PM PST
                  </p>
                </div>
              </div>
            </div>

            <div class="mt-10">
              <h4 class="text-lg font-medium text-slate-800 mb-4">
                Connect With Me
              </h4>
              <div class="flex space-x-4">
                <a
                  href="https://github.com/"
                  target="_blank"
                  class="w-12 h-12 rounded-full bg-gray-800 hover:bg-gray-900 flex items-center justify-center text-white transition cursor-pointer"
                >
                  <i class="fab fa-github text-xl"></i>
                </a>
                <a
                  href="https://linkedin.com/"
                  target="_blank"
                  class="w-12 h-12 rounded-full bg-blue-600 hover:bg-blue-700 flex items-center justify-center text-white transition cursor-pointer"
                >
                  <i class="fab fa-linkedin-in text-xl"></i>
                </a>
                <a
                  href="https://twitter.com/"
                  target="_blank"
                  class="w-12 h-12 rounded-full bg-blue-400 hover:bg-blue-500 flex items-center justify-center text-white transition cursor-pointer"
                >
                  <i class="fab fa-twitter text-xl"></i>
                </a>
                <a
                  href="https://codepen.io/"
                  target="_blank"
                  class="w-12 h-12 rounded-full bg-gray-900 hover:bg-black flex items-center justify-center text-white transition cursor-pointer"
                >
                  <i class="fab fa-codepen text-xl"></i>
                </a>
              </div>
            </div>

            <div class="mt-10">
              <a
                href="#"
                class="inline-flex items-center bg-cyan-600 hover:bg-slate-600 text-white py-3 px-6 rounded-lg font-medium transition !rounded-button whitespace-nowrap cursor-pointer"
              >
                <i class="fas fa-download mr-2"></i> Download Resume
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
/* Custom scrollbar */

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
  background: #6366f1;
  border-radius: 5px;
}

::-webkit-scrollbar-thumb:hover {
  background: #4f46e5;
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

/* Transitions */
.transition {
  transition: all 0.3s ease;
}

/* Custom animations */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes slideUp {
  from { transform: translateY(20px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

.fade-in {
  animation: fadeIn 0.5s ease forwards;
}

.slide-up {
  animation: slideUp 0.5s ease forwards;
}
</style>
