
<script setup>

import CardWork from './CardWork.vue';
defineProps({
    workWeb:Array,

})

const workWEB = [
  {
    "id":1,
    "title": "Одностраничный сайт",
    "description": "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
    "stack_list_title": "Стек технологий:",
    "stack_list": "HTML5, CSS3, JavaScript, VUE",
    "links": "gergerg",
    "imageUrl": " /public/Снимок экрана (155).png",
  },
  {
    "id":2,
    "title": "Одностраничный сайт",
    "description": "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
    "stack_list_title": "Стек технологий:",
    "stack_list": "HTML5, CSS3, JavaScript, VUE",
    "links": "gergerg",
    "imageUrl": " /public/Снимок экрана (155).png",
  },
  {
    "id":3,
    "title": "Одностраничный сайт",
    "description": "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
    "stack_list_title": "Стек технологий:",
    "stack_list": "HTML5, CSS3, JavaScript, VUE",
    "links": "gergerg",
    "imageUrl": " /public/Снимок экрана (155).png",
    "marker": true
  },
  {
    "id":4,
    "title": "Одностраничный сайт",
    "description": "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
    "stack_list_title": "Стек технологий:",
    "stack_list": "HTML5, CSS3, JavaScript, VUE",
    "links": "gergerg",
    "imageUrl": " /public/Снимок экрана (155).png",
    "marker": true
  },

 
]
</script>






<template>
  
<div class="section_work">
  <div class="container max-w-7xl mx-auto pl-4 pr-4">
    <div class="py-4 text-white">
      <h2 style="text-align: center; margin-bottom: 32px; font-size: clamp(2rem,4vw,3rem); font-weight: 900;">{{$t('itemJob')}}</h2>
<div class="flex justify-center gap-4">
  
      <button class="tabs_btn cursor-pointer flex justify-center items-center gap-1 rounded"  style="font-size: 16px; border: 1px solid #7f5af0; padding: 12px 16px; transition: background-color .2s linear, fill .2s linear;" data-type="layout">
        <span data-localization-key="layout">Вёрстка</span>
         <svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" fill="#6c63ff" viewBox="0 0 502.664 502.664" style="enable-background:new 0 0 502.664 502.664"  xml:space="preserve"  ><g><g>
          <path style="transition: background-color .2s linear, fill .2s linear;" fill="#6c63ff;" d="M153.821,358.226L0,274.337v-46.463l153.821-83.414v54.574L46.636,250.523l107.185,53.431
			C153.821,303.954,153.821,358.226,153.821,358.226z">
    </path>
    <path style="transition: background-color .2s linear, fill .2s linear;" fill="#6c63ff;" d="M180.094,387.584L282.103,115.08h32.227L212.084,387.584H180.094z"></path>
    <path style="transition: background-color .2s linear, fill .2s linear;" fill="#6c63ff;" d="M348.843,358.226v-54.272l107.164-52.999l-107.164-52.59v-53.927l153.821,83.522v46.183
			L348.843,358.226z">
    </path></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g>
  </svg>
</button>


      <button class="tabs_btn tabs_btn--active cursor-pointer flex justify-center items-center gap-1 rounded"  style="font-size: 16px; border: 1px solid #7f5af0; padding: 12px 16px; transition: background-color .2s linear, color .2s linear;" data-type="projects">
        <span>VUE / JS</span> 
      
<svg fill="#6c63ff" width="24px" height="24px" viewBox="0 0 24 24" role="img" xmlns="http://www.w3.org/2000/svg" style="transition: background-color .2s linear, fill .2s linear;"><title>Vue.js icon</title><path d="M24,1.61H14.06L12,5.16,9.94,1.61H0L12,22.39ZM12,14.08,5.16,2.23H9.59L12,6.41l2.41-4.18h4.43Z"/>
</svg>
      </button>
</div>

      <div class="grid grid-cols-2 gap-4">
        <CardWork
        v-for="item in workWEB"
        :key="item.id"
        :id="item.id"
        :title="item.title"
        :description="item.description"
        :imageUrl="item.imageUrl"
        :stack_list="item.stack_list"
        :stack_list_title="item.stack_list_title"
        :links="item.links"
        />
        


        
      </div>
    </div>

  </div>        

</div>

</template>

<style scoped>


.tabs_btn:hover{
  background-color: #7f5af0;
}

.tabs_btn:hover svg{

  fill: white;
}

li{
  
}


</style>