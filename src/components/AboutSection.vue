<script>
export default {
  name: 'AboutSection'
}
</script>

<template>
  <section
    class="bg-indigo-950 px-10 lg:px-60 py-10 scroll-mt-20 flex flex-col gap-5 md:flex-row"
    id="about"
  >
    <div class="md:w-2/3">
      <h2 class="text-white opacity-75 *:text-teal-300 text-xl lg:text-4xl font-bold mb-10">
        <span class="text-sm lg:text-2xl">01.&nbsp;</span>About Me
      </h2>
      <div class="space-y-5">
        <p
          class="text-slate-400 lg:text-lg w-[18em] lg:w-[35em] *:text-teal-300 leading-[1.5] tracking-wide"
        >
          Hello! My name is <span>Nay Hlaing Oo</span> and I enjoy sharing knowledge and exploring
          the beauty of technology. My interest in programming started back in 2019 when I decided
          to try self taught myself HTML, CSS and JS and eventually explore into the world of
          <span>Web Development.</span>
        </p>
        <p
          class="text-slate-400 lg:text-lg w-[18em] lg:w-[35em] *:text-teal-300 leading-[1.5] tracking-wide"
        >
          Fast-forward to today, and I’ve had the privilege of building several projects, including
          <span>an E-commerce platform</span>, <span>a logistic company dashboard</span>,
          <span>a site generation tool</span>. My main focus these days is educate people about web
          development at <span>The Perfect 404</span>.
        </p>
        <p class="text-slate-400">Here are a few technologies I’ve been working with recently:</p>
      </div>
      <div class="flex text-slate-400 mt-5 w-[16em] justify-between">
        <ul>
          <li>JavaScript</li>
          <li>Figma</li>
          <li>CSS</li>
          <li>SASS</li>
        </ul>

        <ul>
          <li>Vue JS</li>
          <li>Tailwind CSS</li>
          <li>Nuxt JS</li>
          <li>Svltekit</li>
        </ul>
      </div>
    </div>
    <div class="md:w-1/3">
      <img
        src="../../public/sir-nay-hlaing-oo.jpg"
        alt="sir-nay-haling-oo"
        class="object-cover aspect-square w-full"
      />
    </div>
  </section>
</template>

<style scoped>
li {
  display: flex;
  align-items: center;
  gap: 5px;
}
li::before {
  content: '';
  width: 4px;
  height: 4px;
  background-color: rgb(94, 234, 212);
  border-radius: 50%;
}
</style>
