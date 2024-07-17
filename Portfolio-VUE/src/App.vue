<script setup>
import {useI18n} from 'vue-i18n'

const { t } = useI18n({useScope:'global'})


import Switch from './components/Switch.vue'
import language from './components/language.vue';
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

<div class="section_main">
  <div class="container max-w-7xl mx-auto pl-4 pr-4">
    <div class="flex items-center justify-center gap-6 py-4">
      <div class="basis-2/4 text-white">
        <h2 style="margin-bottom: 16px; font-size: clamp(2rem,4vw,4rem); font-weight: 900;">{{$t('hello')}}</h2>
        <p style="font-size: clamp(1.5rem,4vw,2.5rem); font-weight: 700;">
          {{$t('text')}}
        </p>
      </div>
      <div class="basis-2/4"><img src="/public/developer.svg" alt=""></div>
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
