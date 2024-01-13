<script>
import IconGithub from './icons/IconGithub.vue'
import IconFacebook from './icons/IconFacebook.vue'
import IconInstagram from './icons/IconInstagram.vue'

export default {
  name: 'FooterBar',
  components: { IconGithub, IconFacebook, IconInstagram }
}
</script>

<template>
  <footer class="w-full bg-indigo-950 flex flex-col items-center">
    <div class="flex gap-5 *:text-slate-300 *:text-2xl">
      <IconFacebook class="hover:text-teal-300" />
      <IconInstagram class="hover:text-teal-300" />
      <IconGithub class="hover:text-teal-300" />
    </div>
    <div>
      <p class="text-slate-400 mt-3 mb-10">Built By Nay Hlaing</p>
    </div>
  </footer>
</template>

<style scoped></style>
