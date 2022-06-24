<script setup>
  import { ref } from 'vue';

  const projects = ref([
    { pic: "/src/assets/pic_projects/hi-chaty.png", name:"Chat-App", domain:"Web Application", link:"https://github.com/Nasan01/hi-chaty" },
    { pic: "/src/assets/pic_projects/pendu.png", name:"Riddle words", domain:"Frontend App", link:"https://nasan01.github.io/pendu-game" },
    { pic: "/src/assets/pic_projects/portfolio.png", name:"My-portfolio", domain:"Website", link:"/" },
  ]);

</script>

<template>
  <div class="min-h-screen bg-slate-900 text-slate-100">
    <h1 class="text-center text-5xl p-5">Projects</h1>
    <div class="md:flex md:flex-wrap md:mt-5 md:mx-5 md:justify-center">
      <div 
        v-for="p in projects" 
        :key="p.name"
        class="rounded-lg bg-slate-700 text-center mx-3 shadow-lg shadow-slate-800"
      >
      <a :href="p.link" target="blank">
        <img 
          :src="p.pic" 
          :alt="'pic of project'+p.name" 
          class="w-96 h-60 rounded-t-lg"
        />
        <div class="p-4">
          <h3 class="text-xl font-semibold m-1">{{ p.name }}</h3>
          <h4 class="text-lg text-slate-200 m-1">{{ p.domain }}</h4>
        </div>
      </a>
      </div>
    </div>
  </div>
</template>
