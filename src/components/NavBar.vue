<script>
import IconProfile from '@/components/icons/IconProfile.vue'
import IconMenu from '@/components/icons/IconMenu.vue'
export default {
  props: {
    activeMenu: String
  },
  emit: ['handleClickMenu'],
  components: { IconProfile, IconMenu },
  data() {
    return {
      navMenu: ['About', 'Experience', 'Work', 'Contact']
    }
  },
  methods: {}
}
</script>

<template>
  <nav
    class="w-screen sticky top-0 left-0 z-10 h-16 md:h-20 flex bg-indigo-950 justify-between items-center px-3 md:px-5 shadow-md"
  >
    <IconProfile
      class="text-4xl md:text-5xl text-teal-300 cursor-pointer"
      @click="$emit('handleClickMenu', 'hero')"
    />
    <div class="hidden md:flex h-full items-center gap-10 text-lg">
      <ul class="flex space-x-10 items-center h-full">
        <li
          v-for="(menu, idx) in navMenu"
          :key="idx"
          class="cursor-pointer group active:scale-95 transition"
          @click="$emit('handleClickMenu', menu)"
        >
          <span class="text-teal-300 group-hover:text-slate-200">0{{ idx + 1 }}.</span>
          <span
            class="group-hover:text-teal-300"
            :class="activeMenu === menu ? 'text-teal-300' : 'text-slate-200'"
            >&nbsp;{{ menu }}</span
          >
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
