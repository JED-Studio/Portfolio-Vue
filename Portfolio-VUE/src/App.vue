<script setup>
import {useI18n} from 'vue-i18n'

const { t } = useI18n({useScope:'global'})


import Switch from './components/Switch.vue'
import language from './components/language.vue';
import Main from './components/Main.vue'
import AboutMe from './components/AboutMe.vue'
import WorkExperience from './components/WorkExperience.vue'
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

<div class="section_itemJob">
  <div class="container max-w-7xl mx-auto pl-4 pr-4">
    <div class="py-4 text-white">
      <h2 style="text-align: center; margin-bottom: 32px; font-size: clamp(2rem,4vw,3rem); font-weight: 900;">{{$t('itemJob')}}</h2>

      <ul class="job_responsibilities grid  gap-12 py-4 grid-cols-4">
        <li><img width="48" src="/public/html.svg" alt="">              <p>HTML5</p></li>
        <li><img width="48" src="/public/css.svg" alt="">               <p>CSS3</p></li>
        <li><img width="48" src="/public/scss.svg" alt="">              <p>SCSS</p></li>
        <li><img width="48" src="/public/js.svg" alt="">                <p>JavaSccript</p></li>
        <li><img width="48" src="/public/ts.svg" alt="">                <p>TypeScript</p></li>
        <li><img width="48" src="/public/vue-svgrepo-com.svg" alt="">   <p>VUE</p></li>
        <li><img width="48" src="/public/nuxt-svgrepo-com.svg" alt="">  <p>Nuxt</p></li>
        <li><img width="48" src="" alt="">                              <p></p></li>
      </ul>
    </div>

  </div>        

</div>


 </div>
</template>

<style >
:root {
  --background-color-primary: #090b16;
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
