<script>
export default {
  name: 'HeroSection'
}
</script>

<template>
  <section class="bg-blue-950 px-10 lg:px-40 py-20" id="hero-section">
    <div class="space-y-1 lg:space-y-3 mb-4 lg:mb-6">
      <p class="text-teal-300 lg:text-lg lg:font-semibold lg:-mb-2">Hi, my name is</p>
      <h1 class="text-4xl font-bold lg:text-6xl text-white opacity-95">Nay Hlaing Oo.</h1>
      <p class="text-slate-400 text-2xl lg:text-3xl font-bold lg:pt-2">
        I build things for the web.
      </p>
    </div>
    <p
      class="text-slate-400 lg:text-lg w-[18em] lg:w-[35em] *:text-teal-300 leading-[1.5] tracking-wide"
    >
      A <span>tech enthusiast</span> and an <span>educator</span> believes that everyone can be a
      self-taught developer. I enjoy developing <span>Frontend</span> and
      <span>User Interface</span> design, where I can create visually appealing websites and make
      things beautiful.
    </p>
    <button
      class="hover:bg-blue-950 border border-transparent duration-300 hover:text-teal-300 hover:border hover:border-teal-300 transition my-5 lg:my-6 lg:text-lg px-4 py-2 text-blue-950 font-bold bg-teal-300 rounded-md"
    >
      Contact Me
    </button>
  </section>
</template>
