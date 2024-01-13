<script>
import NavBar from '@/components/NavBar.vue'
import HeroSection from '@/components/HeroSection.vue'
export default {
  name: 'HomeView',
  components: { NavBar, HeroSection },
  data() {
    return {
      activeSection: 'Title'
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
</template>

<style scoped></style>
