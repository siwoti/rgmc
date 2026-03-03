<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ActivitiesSection from './components/ActivitiesSection.vue'
import GallerySection from './components/GallerySection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <header>
    <NavBar />
  </header>
  <main>
    <HeroSection />
    <AboutSection />
    <ActivitiesSection />
    <GallerySection />
    <ContactSection />
  </main>
  <FooterSection />
</template>
