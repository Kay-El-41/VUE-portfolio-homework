<script>
import IconGit from './icons/IconGit.vue'
import IconLink from './icons/IconLink.vue'
export default {
  name: 'WorkSection',
  components: { IconGit, IconLink },
  data() {
    return {
      works: [
        {
          id: 0,
          title: 'Netflix Clone',
          description: 'TV Shows Online service using Tailwindcss',
          techUsed: ['Pure HTML', 'TailwindCSS'],
          image: '../../public/netflix.jpg',
          links: [
            {
              id: 'L1',
              icon: 'github',
              link: '#'
            }
          ]
        },
        {
          id: 1,
          title: 'Rock Paper Scissors',
          description: 'The game was build with JS. Play the demo',
          techUsed: ['Pure JavaScript', 'Pure CSS', 'Pure HTML'],
          image: '../../public/rockpaperscissor.png',
          links: [
            {
              id: 'L1',
              icon: 'github',
              link: '#'
            },
            {
              id: 'L2',
              icon: 'external',
              link: 'https://rock-paper-scissors-five-kohl.vercel.app/'
            }
          ]
        },
        {
          id: 2,
          title: 'Video Scroll Animation',
          description: 'Control the playback based on the page scroll',
          techUsed: ['Pure JavaScript', 'Pure CSS', 'Pure HTML'],
          image: '../../public/videoanimation.png',
          links: [
            {
              id: 'L1',
              icon: 'github',
              link: '#'
            },
            {
              id: 'L2',
              icon: 'external',
              link: 'https://video-scroll-js-animation.vercel.app/'
            }
          ]
        }
      ]
    }
  }
}
</script>

<template>
  <section class="bg-indigo-950 px-10 lg:px-60 py-10 scroll-mt-20" id="work">
    <h2 class="text-white opacity-75 *:text-teal-300 text-xl lg:text-4xl font-bold mb-10">
      <span class="text-sm lg:text-2xl">03.&nbsp;</span>Some Things I've Built
    </h2>
    <div class="flex flex-col md:flex-row gap-16">
      <div
        v-for="work in works"
        :key="work.id"
        class="border relative w-full aspect-square flex items-center border-indigo-900 py-5 px-5 md:py-8 md:px-10"
      >
        <img
          :src="work.image"
          alt="image"
          class="w-full h-full object-cover absolute top-0 left-0 opacity-40"
        />
        <div class="relative z-[1]">
          <p class="text-teal-300 text-sm">Featured Project</p>
          <p class="text-white opacity-75 font-bold text-lg my-2">{{ work.title }}</p>
          <p class="text-slate-400 my-4">{{ work.description }}</p>
          <ul class="flex gap-3 my-2">
            <li v-for="tech in work.techUsed" class="text-slate-400 text-sm" :key="tech">
              {{ tech }}
            </li>
          </ul>
          <ul class="flex gap-3">
            <li v-for="link in work.links" :key="work.id + link.id">
              <a :href="link.link" v-if="link.icon === 'github'">
                <IconGit class="text-slate-300 text-xl hover:text-teal-300" />
              </a>
              <a :href="link.link" v-if="link.icon === 'external'">
                <IconLink class="text-slate-300 text-xl hover:text-teal-300" />
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
