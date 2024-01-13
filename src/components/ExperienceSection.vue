<script>
export default {
  name: 'ExperienceSection',
  data() {
    return {
      experience: [
        {
          id: 0,
          position: 'Frontend/UI Developer',
          company: 'Epic Startup Tech Company',
          date: 'March 2021 - April 2022',
          done: [
            {
              id: 'J1',
              job: 'Write modern, performant, maintainable code for a diverse array of projects.'
            },
            {
              id: 'J2',
              job: 'Work with a variety of different languages, platforms, frameworks, and plugins such as JavaScript, Tailwind, SASS, Sveltekit.'
            },
            {
              id: 'J3',
              job: 'Communicate with multi-disciplinary teams of developers, designers and product manager.'
            }
          ]
        },
        {
          id: 1,
          position: 'Instructor',
          company: 'The Perfect 404',
          date: 'September 2022 - Present',
          done: [
            {
              id: 'J1',
              job: 'Make tutorial videos on both Facebook and YouTube on how to code.'
            },
            {
              id: 'J2',
              job: 'Create beginner-friendly web development course structure and assessment project that are easy to learn for our tech students.'
            },
            {
              id: 'J3',
              job: 'Enhancing our SprintX web app by improving the UI, adding more courses, and planning to integrate an AI chat for a better learning experience for our students.'
            }
          ]
        }
      ]
    }
  }
}
</script>

<template>
  <section class="bg-indigo-950 px-10 lg:px-60 py-10 scroll-mt-20" id="experience">
    <h2 class="text-white opacity-75 *:text-teal-300 text-xl lg:text-4xl font-bold mb-10">
      <span class="text-sm lg:text-2xl">02.&nbsp;</span>Where I've Worked
    </h2>
    <div class="flex flex-col md:flex-row gap-16">
      <div
        v-for="exp in experience"
        :key="exp.id"
        class="md:w-1/2 border border-indigo-900 py-5 px-5 md:py-8 md:px-10"
      >
        <h3 class="text-slate-300 *:text-teal-300 text-lg font-semibold">
          {{ exp.position }}&nbsp;@&nbsp;<span>{{ exp.company }}</span>
        </h3>
        <p class="text-slate-400 mt-2 mb-4">{{ exp.date }}</p>
        <ul class="space-y-3">
          <li v-for="job in exp.done" :key="exp.id + job.id" class="text-slate-400">
            {{ job.job }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
li {
  display: flex;
  align-items: start;
  gap: 8px;
}
li::before {
  content: '';
  width: 6px;
  height: 6px;
  flex-shrink: 0;
  background-color: rgb(94, 234, 212);
  border-radius: 50%;
  transform: translateY(11px);
}
</style>
