<template>
  <div class="min-h-screen bg-white">
    <Header />
    <HeroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectSection />
    
    <ContactSection />
    <Footer />
  </div>
</template>

<script setup>
import Header from "./components/common/Header.vue";
import Footer from "./components/common/Footer.vue";
import HeroSection from "./components/public/HeroSection.vue";
import AboutSection from "./components/public/AboutSection.vue";
import SkillsSection from "./components/public/SkillsSection.vue";
//import ProjectSection from "./components/public/ProjectSection.vue";
import ContactSection from "./components/public/ContactSection.vue";
</script>