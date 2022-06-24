<script setup>
  import { ref } from 'vue';

  const projects = ref([
    { pic: "https://github.com/Nasan01/tmp_pic/blob/master/hi-chaty.png?raw=true", name:"Chat-App", domain:"Web Application", link:"https://github.com/Nasan01/hi-chat" },
    { pic: "https://github.com/Nasan01/tmp_pic/blob/master/pendu.png?raw=true", name:"Riddle words", domain:"Frontend App", link:"https://nasan01.github.io/pendu-game" },
    { pic: "https://github.com/Nasan01/tmp_pic/blob/master/portfolio.png?raw=true", name:"My-portfolio", domain:"Website", link:"/portfolio" },
  ]);

</script>

<template>
  <div class="min-h-screen bg-slate-900 text-slate-100" id="projects">
    <h1 class="text-center text-2xl md:text-5xl p-5">Projects</h1>
    <div class="flex flex-wrap m-5 justify-center">
      <div 
        v-for="p in projects" 
        :key="p.name"
        class="rounded-lg bg-slate-700 text-center m-3 shadow-lg shadow-slate-800"
      >
      <a :href="p.link" target="blank">
        <img 
          :src="p.pic" 
          :alt="'pic of project'+p.name" 
          class="w-80 h-52 sm:w-96 sm:h-60 rounded-t-lg"
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
