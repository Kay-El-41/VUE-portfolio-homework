<script>
import NavBar from '@/components/NavBar.vue'
import HeroSection from '@/components/HeroSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import ExperienceSection from '@/components/ExperienceSection.vue'
import WorkSection from '@/components/WorkSection.vue'
import ContactSection from '@/components/ContactSection.vue'
import FooterBar from '@/components/FooterBar.vue'
export default {
  name: 'HomeView',
  components: {
    NavBar,
    HeroSection,
    AboutSection,
    ExperienceSection,
    WorkSection,
    ContactSection,
    FooterBar
  },
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
  <ExperienceSection />
  <WorkSection />
  <ContactSection />
  <FooterBar />
</template>

<style scoped></style>
