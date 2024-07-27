<script setup>
import {useI18n} from 'vue-i18n'

const { t } = useI18n({useScope:'global'})


import Switch from './components/Switch.vue'
import language from './components/language.vue';
import Main from './components/Main.vue'
import AboutMe from './components/AboutMe.vue'
import WorkExperience from './components/WorkExperience.vue'
import ItemJob from './components/ItemJob.vue'
import SectionWork from './components/SectionWork.vue';




</script>

<template>
 <div class="wrapper">
  <div class="header">
    <div class="container max-w-7xl mx-auto pl-4 pr-4">
      <div class="flex items-center justify-end gap-6 py-4">
      <Switch/>
      <language/>
      </div>
    </div>
</div>

<Main/>
<AboutMe/>
<WorkExperience/>
<ItemJob/>
<SectionWork/>











 </div>
</template>

<style >
:root {
  --background-color-primary: #202020;
  --background-color-secondary:#090b16;
  --background-color-luna:#ffffff ;
  --background-color-ul:rgba(255, 255, 255, .05);
  --accent-color: #cacaca;
  --text-primary-color:  white;
  --text-color:white;
  --text-color-h1:rgb(255, 255, 255);
  --text-color-h2:rgba(255, 255, 255, .5);
  --element-size: 4rem;
  transition: 0.5s;
  
}

/* Define styles for the root window with dark - mode preference */
:root.dark-theme {
  --background-color-primary: #ffffff;
  --background-color-secondary: #2d2d30;
  --background-color-luna:#000000 ;
  --background-color-ul:rgb(0, 0, 0);
  --accent-color: #3f3f3f;
  --text-primary-color: #ddd;
  --text-color:rgb(255, 255, 255);
  --text-color-h1:rgb(0, 0, 0);
  --text-color-h2:rgba(0, 0, 0, 0.5);

}
</style>
