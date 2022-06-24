
<template>
  <div class="h-screen bg-slate-800 text-slate-100">
    <div class="md:flex md:justify-between md:items-center md:p-14" style="height: 20vh;">
      <h1 class="text-2xl"><a href="/">Avonasandratra</a></h1>
      <div class="text-lg text-slate-200">
        <ul class="md:flex md:justify">
          <li class="md:mx-3"><a href="#">Projects</a></li>
          <li class="md:mx-3"><a href="#">Contact</a></li>
        </ul>
      </div>
      <div>
        <button class="px-4 py-3 rounded-md bg-teal-400">Hire me</button>
      </div>
    </div>
    <div class="md:grid md:grid-cols-3 md:p-14" style="height: 80vh;">
      <div class="md:col-span-1 flex flex-col items-center justify-center">
        <div>
          <h2 class="font-bold text-3xl uppercase">Hi, I am <br /> Avonasandratra</h2>
          <h3 class="text-slate-300 text-xl">A Full-Stack Developer</h3>
        </div>
      </div>
      <div class="md:col-span-2 flex flex-col items-center justify-center">
        <div class="text-center">
          <img 
            src="@/assets/svg_portfolio/01.svg" 
            alt="side picture representation"
            class="w-5/6 h-5/6"
          />
        </div>
      </div>
    </div>
  </div>
</template>