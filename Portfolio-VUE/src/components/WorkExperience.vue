<template>
<div class="section_itemJob">
  <div class="container mx-auto pl-4 pr-4" style="max-width: 1400px;">
    <div class="py-4">
  <div class=" text-white" style="color: var(--background-color-luna);">
        <h2 style="text-align: center; margin-bottom: 32px; font-size: clamp(2rem,4vw,3rem); font-weight: 900;">{{$t('itemJob')}}</h2>
        <div class="flex  gap-4">

          <div>
            <img src="/public/vecteezy.svg" alt="" width="80px">
          </div>

          <div>
            <h3 class="font-bold text-xl ">{{$t('job_title')}}</h3>

            <div class="flex flex-col gap-2 py-2">
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

      <ul class="job_responsibilities flex flex-col gap-2 py-4">
        <li>- Вёрстка виртуальных витрин товаров и лендингов под масштабные акции;</li>
        <li>- Рефакторинг и переписывание старого кода;</li>
        <li>- Оптимизация JavaScript-кода;</li>
        <li>- Работа с внутренним API при создании проектов, связанными с товарами.</li>
      </ul>

      <h4 class="pb-1 inline-block text-lg font-bold" style="margin-bottom: 10px;border-bottom: 2px solid #7f5af0; ">Достижения:</h4>

      <ul class="job_responsibilities flex flex-col gap-2 py-4">
        <li>- Вёрстка виртуальных витрин товаров и лендингов под масштабные акции;</li>
        <li>- Рефакторинг и переписывание старого кода;</li>
        <li>- Оптимизация JavaScript-кода;</li>
        <li>- Работа с внутренним API при создании проектов, связанными с товарами.</li>
      </ul>

      <h4 class="pb-1 inline-block text-lg font-bold" style="margin-bottom: 10px;border-bottom: 2px solid #7f5af0; ">Стек технологий:</h4>

      <ul class="job_responsibilities flex flex-col gap-2 py-4 " style="">
        <li>• HTML5</li>
        <li>• CSS 3</li>
        <li>• SCSS</li>
        <li>• JavaScript</li>
        <li>• VUE</li>
      </ul>
      <h4 class="pb-1 inline-block text-lg font-bold" style="margin-bottom: 10px;border-bottom: 2px solid #7f5af0; ">Стек технологий:</h4>

      <ul class="job_responsibilities flex flex-col gap-2 py-4 " style="">
        <li>• HTML5</li>
        <li>• CSS 3</li>
        <li>• SCSS</li>
        <li>• JavaScript</li>
        <li>• VUE</li>
      </ul>



      </div>
      </div>
      </div>
    
    </div>

  </div>        

</div>
</template>