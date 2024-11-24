<template>
<div class="portfolio-vue__section-aboutMe">
  <div class="container  mx-auto pl-4 pr-4" style="max-width: 1400px;">
    <div class="py-4">
      <div class="" style="color: var(--background-color-luna);">
        <h2 class="portfolio-vue__aboutMe">{{$t('aboutMe')}}</h2>
        <div class="flex flex-col gap-5">
        <p class="portfolio-vue__aboutMe-p" >🧑🏽‍💻
          {{$t('aboutMe1')}}
        </p>
        <p class="portfolio-vue__aboutMe-p">🖥️
          {{$t('aboutMe2')}}
        </p>
        <p class="portfolio-vue__aboutMe-p">📚
          {{$t('aboutMe3')}}
        </p>
      </div>
      </div>
    
    </div>

  </div>        

</div>
</template>

<style scoped>
.portfolio-vue__aboutMe{
  text-align: center; 
  margin-bottom: 32px; 
  font-size: clamp(2rem,4vw,3rem); 
  font-weight: 900;
}

.portfolio-vue__aboutMe-p{
  font-size: clamp(1.125rem,2vw,1.25rem);
}
</style>

