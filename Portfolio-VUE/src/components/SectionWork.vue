
<script setup>
import { ref, computed} from 'vue';
import CardWork from './CardWork.vue';

defineProps({
    workWeb:Array,

})

const activeTab = ref('layout');

const workWebCards = [
  {
    id: 1,
    title: "JED 3D STUDIO",
    description: "Созданный сайт для 3D студии специализируется на моушен дизайне и предлагает портфолио работ с использованием различных программ.",
    stack_list_title: "Стек технологий:",
    stack_list: "JavaScript (ES6)",
    links: "Less",
    imageUrl: "/public/Снимок экрана (155).png",
  },
  {
    id: 2,
    title: "JED 3D STUDIO",
    description: "Созданный сайт для 3D студии специализируется на моушен дизайне и предлагает портфолио работ с использованием различных программ.",
    stack_list_title: "Стек технологий:",
    stack_list: "JavaScript (ES6)",
    links: "Less",
    imageUrl: "/public/Снимок экрана (155).png",
  },
];

const workVUECards = [
  {
    id: 3,
    title: "Salvator Cyber Club",
    description: "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
    stack_list_title: "Стек технологий:",
    stack_list: "VUE",
    links: "Tailwind",
    links1: "Vue Router",
    imageUrl: "/public/Снимок экрана (154).png",
  },
  {
    id: 4,
    title: "Salvator Cyber Club",
    description: "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
    stack_list_title: "Стек технологий:",
    stack_list: "VUE",
    links: "Tailwind",
    links1: "Vue Router",
    imageUrl: "/public/Снимок экрана (154).png",
  },
];

const displayedCards = computed(() => {
  return activeTab.value === 'layout' ? workWebCards : workVUECards;
});

</script>






<template>
  
<div class="section_work">
  <div class="container max-w-7xl mx-auto pl-4 pr-4">
    <div class="py-4 text-white">
      <h2 style="text-align: center; margin-bottom: 32px; font-size: clamp(2rem,4vw,3rem); font-weight: 900;">{{$t('itemJob')}}</h2>
<div class="flex justify-center gap-4">
  
      <button :class="{ 'tabs_btn--active': activeTab === 'layout' }" @click="activeTab= 'layout'" class="tabs_btn cursor-pointer flex justify-center items-center gap-1 rounded"  style="font-size: 16px; border: 1px solid #7f5af0; padding: 12px 16px; transition: background-color .2s linear, fill .2s linear;" data-type="layout">
        <span   data-localization-key="layout">Вёрстка</span>
         
</button>


      <button  :class="{ 'tabs_btn--active': activeTab === 'projects' }" @click="activeTab = 'projects'" class="tabs_btn tabs_btn--active cursor-pointer flex justify-center items-center gap-1 rounded"  style="font-size: 16px; border: 1px solid #7f5af0; padding: 12px 16px; transition: background-color .2s linear, color .2s linear;" data-type="projects">
        <span>VUE / JS</span> 

      </button>
</div>

<div v-if="activeTab === 'layout' || activeTab === 'projects'" class="grid grid-cols-2 gap-4">
          <CardWork
            v-for="item in (activeTab === 'layout' ? workWebCards : workVUECards)"
            :key="item.id"
            :id="item.id"
            :title="item.title"
            :description="item.description"
            :imageUrl="item.imageUrl"
            :stack_list="item.stack_list"
            :stack_list_title="item.stack_list_title"
            :links="item.links"
            :links1="item.links1"
            :links2="item.links2"
            :links3="item.links3"
            :links4="item.links4"
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