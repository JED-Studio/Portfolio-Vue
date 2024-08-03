<template>
<div class="section_main">
  <div class="container  mx-auto pl-4 pr-4" style="max-width: 1400px;">
    <div class="block items-center justify-center gap-6 py-4 sm:flex">
      <div class="basis-2/4" style="color: var(--background-color-luna);">
        <h2 style="margin-bottom: 16px; font-size: clamp(2rem,4vw,4rem); font-weight: 900;">{{$t('hello')}}</h2>
        <p style="font-size: clamp(1.5rem,4vw,2.5rem); font-weight: 700;">
          {{$t('text')}}
        </p>
      </div>
      <div class="basis-2/4"><img src="/public/developer.svg" alt=""></div>
    </div>

  </div>        

</div>
</template>