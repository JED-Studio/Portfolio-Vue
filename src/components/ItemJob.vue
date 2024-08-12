<template> 
<div class="section_itemJob">
  <div class="container  mx-auto pl-4 pr-4" style="max-width: 1400px;">
    <div class="py-4" style="color: var(--background-color-luna);">
      <h2 style="text-align: center; margin-bottom: 32px; font-size: clamp(2rem,4vw,3rem); font-weight: 900;">{{$t('itemJob_stack')}}</h2>

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

      <h2 style=" margin-bottom: 32px; font-size: clamp(1.5rem,4vw,2rem); ">{{$t('itemTools')}}</h2>

      <ul class="job_responsibilities grid  gap-12 py-4 grid-cols-4">
        <li><img width="48" src="/public/vscode (1).svg" alt="">               <p>VS code</p></li>
        <li><img width="48" src="/public/webpack (1).svg" alt="">              <p>Webpack</p></li>
        <li><img width="48" src="/public/git (1).svg" alt="">                <p>Git</p></li>
      </ul>
    </div>

  </div>        

</div>
</template>

<style scoped>
li{
display: flex;
align-items: center;
flex-direction: column;
justify-content: center;
gap: 8px;
}
</style>