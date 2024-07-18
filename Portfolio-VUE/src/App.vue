<script setup>
import {useI18n} from 'vue-i18n'

const { t } = useI18n({useScope:'global'})


import Switch from './components/Switch.vue'
import language from './components/language.vue';
import Main from './components/Main.vue'
import AboutMe from './components/AboutMe.vue'
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

<div class="section_itemJob">
  <div class="container max-w-7xl mx-auto pl-4 pr-4">
    <div class="py-4">
      <div class=" text-white">
        <h2 style="text-align: center; margin-bottom: 32px; font-size: clamp(2rem,4vw,3rem); font-weight: 900;">{{$t('itemJob')}}</h2>
        <div class="flex  gap-4">

          <div>
            <img src="/public/vecteezy.svg" alt="" width="80px">
          </div>

          <div>
            <h3 class="">{{$t('job_title')}}</h3>

            <div class="flex flex-col gap-2">
              <p style="font-size: .875rem;">
                {{$t('job_info')}}
              </p>
              <p style="font-size: .875rem;">
                  {{$t('job_term')}}

              </p>
              <p style="font-size: .875rem;">
                  {{$t('job_location')}}

              </p>
      </div>

      <ul class="job_responsibilities">
        <li>- Вёрстка виртуальных витрин товаров и лендингов под масштабные акции;</li>
        <li>- Рефакторинг и переписывание старого кода;</li>
        <li>- Оптимизация JavaScript-кода;</li>
        <li>- Работа с внутренним API при создании проектов, связанными с товарами.</li>

      </ul>

      </div>
      </div>
      </div>
    
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
