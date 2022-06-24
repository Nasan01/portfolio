
<template>
  <div class="h-screen bg-slate-800 text-slate-100">
    <div class="flex justify-between sm:flex sm:justify-between sm:items-center p-14" style="height: 20vh;">
      <h1 class="text-md sm:text-2xl"><a href="/portfolio">Avonasandratra</a></h1>
      <div class="text-lg text-slate-200 hidden sm:block">
        <ul class="md:flex md:justify">
          <li class="md:mx-3"><a href="#projects">Projects</a></li>
          <li class="md:mx-3"><a href="#contact">Contact</a></li>
        </ul>
      </div>
      <div>
        <a class="px-4 py-3 rounded-md text-sm sm:text-md bg-teal-400" href="#contact">Hire me</a>
      </div>
    </div>
    <div class="flex flex-col md:flex-none md:grid md:grid-cols-3 md:p-14" style="height: 80vh;">
      <div class="m-10 md:col-span-1 md:m-0 flex flex-col items-center justify-center">
        <div>
          <h2 class="font-bold text-3xl uppercase">Hi, I am <br /> Avonasandratra</h2>
          <h3 class="text-slate-300 text-xl">A Full-Stack Developer</h3>
        </div>
      </div>
      <div class="m-10 md:m-0 md:col-span-2 flex flex-col items-center justify-center">
        <div class="text-center">
          <img 
            src="https://raw.githubusercontent.com/Nasan01/tmp_pic/d4e6970bb4fc6994c9403fac6beef2f7801d8c11/01.svg" 
            alt="side picture representation"
            class="w-5/6 h-5/6"
          />
        </div>
      </div>
    </div>
  </div>
</template>