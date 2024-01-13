<script>
import NavBar from '@/components/NavBar.vue'
import HeroSection from '@/components/HeroSection.vue'
import AboutSection from '@/components/AboutSection.vue'
export default {
  name: 'HomeView',
  components: { NavBar, HeroSection, AboutSection, AboutSection },
  data() {
    return {
      activeSection: ''
    }
  },
  methods: {
    goToSection(sectionName) {
      const sectionElement = document.getElementById(sectionName.toLowerCase())
      if (sectionElement) {
        this.activeSection = sectionName
        sectionElement.scrollIntoView({
          behavior: 'smooth',
          blocK: 'center'
        })
      }
    }
  }
}
</script>

<template>
  <NavBar @handleClickMenu="goToSection" :activeMenu="activeSection" />
  <HeroSection />
  <AboutSection />
</template>

<style scoped></style>
