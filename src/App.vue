<script setup lang="ts">
import NavBar from "./components/NavBar.vue";
import HeroSection from "./components/HeroSection.vue";
import AboutSection from "./components/AboutSection.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import TechStack from "./components/TechStack.vue";
import ContactSection from "./components/ContactSection.vue";
import FooterSection from "./components/FooterSection.vue";
</script>

<template>
  <div class="min-h-screen bg-gray-950 text-gray-100 font-sans">
    <NavBar />
    <main>
      <HeroSection />
      <AboutSection />
      <ProjectsSection />
      <TechStack />
      <ContactSection />
    </main>
    <FooterSection />
  </div>
</template>
