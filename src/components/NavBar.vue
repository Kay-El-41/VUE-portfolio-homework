<script>
import IconProfile from '@/components/icons/IconProfile.vue'
import IconMenu from '@/components/icons/IconMenu.vue'
export default {
  name: 'NavBar',
  components: { IconProfile, IconMenu },
  data() {
    return {
      navMenu: ['Title', 'Experience', 'Work', 'Contact']
    }
  }
}
</script>

<template>
  <nav
    class="w-screen sticky top-0 left-0 z-10 h-16 md:h-20 flex bg-blue-950 justify-between items-center px-3 md:px-5 shadow-md"
  >
    <IconProfile class="text-4xl md:text-5xl text-teal-300" />
    <div class="hidden md:flex h-full items-center gap-10 text-lg">
      <ul class="flex space-x-10 items-center h-full">
        <li
          v-for="(menu, idx) in navMenu"
          :key="idx"
          class="cursor-pointer group active:scale-95 transition"
        >
          <span class="text-teal-300 group-hover:text-slate-200">0{{ idx + 1 }}.</span>
          <span class="text-slate-200 group-hover:text-teal-300">&nbsp;{{ menu }}</span>
        </li>
      </ul>
      <button
        class="hover:text-slate-200 hover:border-slate-200 active:scale-95 transition text-teal-300 px-3 py-1 border border-teal-300 rounded-md"
      >
        Resume
      </button>
    </div>
    <IconMenu class="text-4xl text-teal-300 md:hidden" />
  </nav>
</template>

<style scoped></style>
