<template>
  <div class="section_work">
    <div class="container  mx-auto pl-4 pr-4" style="max-width: 1280px;">
      <div class="py-4 ">
        <h2
          style="
            text-align: center;
            margin-bottom: 32px;
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 900;
          "
        ></h2>
        <div class="flex justify-center gap-4 mb-12" style="color: #7f5af0;">
          <button
            @click="showFirstCards = true"
            :class="['tabs_btn', { active: showFirstCards }]"

            class="tabs_btn cursor-pointer flex justify-center items-center gap-1 rounded"
            style="
              font-size: 16px;
              border: 1px solid #7f5af0;
              padding: 12px 16px;
              transition:
                background-color 0.2s linear,color 0.2s linear,
                fill 0.2s linear;
            "
          >
            {{$t('button')}}
            <svg :class="{ active: showFirstCards }"  version="1.1" xmlns="http://www.w3.org/2000/svg" width="24" height="24" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" fill="#6c63ff" viewBox="0 0 502.664 502.664" style="enable-background:new 0 0 502.664 502.664; transition:background-color 0.2s linear,fill 0.2s linear;" xml:space="preserve"><g><g><path fill="#6c63ff;" d="M153.821,358.226L0,274.337v-46.463l153.821-83.414v54.574L46.636,250.523l107.185,53.431
			C153.821,303.954,153.821,358.226,153.821,358.226z"></path><path fill="#6c63ff;" d="M180.094,387.584L282.103,115.08h32.227L212.084,387.584H180.094z"></path><path fill="#6c63ff;" d="M348.843,358.226v-54.272l107.164-52.999l-107.164-52.59v-53.927l153.821,83.522v46.183
			L348.843,358.226z"></path></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g><g></g></svg>
          </button>
          <button
            @click="showFirstCards = false"
            :class="['tabs_btn', { active: !showFirstCards }]"
            class="tabs_btn cursor-pointer flex justify-center items-center gap-1 rounded"
            style="
              font-size: 16px;
              border: 1px solid #7f5af0;
              padding: 12px 16px;
              transition:
                background-color 0.2s linear,
                color 0.2s linear;
            "
          >
            Vue / JS
            <svg :class="{ active: !showFirstCards }" fill="#6c63ff" width="24px" height="24px" viewBox="0 0 24 24" role="img" xmlns="http://www.w3.org/2000/svg" style="transition:background-color 0.2s linear,fill 0.2s linear;"><title>Vue.js icon</title><path d="M24,1.61H14.06L12,5.16,9.94,1.61H0L12,22.39ZM12,14.08,5.16,2.23H9.59L12,6.41l2.41-4.18h4.43Z"/>
            </svg>
          </button>
        </div>

        <div v-if="showFirstCards" class="grid grid-cols-1 gap-4 md:grid-cols-2" style="color: var(--background-color-luna);">
          <div
            v-for="(card, i) in cards.firstCards"
            :key="i"
            class="item flex flex-col rounded-lg"
            style="
              box-shadow:
                0 3px 6px rgba(0, 0, 0, 0.16),
                0 3px 6px rgba(0, 0, 0, 0.23);
              background-color: var( --background-color-primary);
              overflow: hidden;
            "
          >
            <img :src="card.image" :alt="card.image" />
            
            <div class="p-6">
              <h3 class="mb-4 font-black text-2xl leading-tight">{{card.title}}</h3>
              <p>{{$t(card.description)}}</p>
              <div class="my-5" style="background-color: #7f5af0; padding: 1px"></div>
              <h4 class="mb-4 font-black text-2xl leading-tight">{{ $t(card.stack_list_title) }}</h4>
              <ul style="list-style: square inside;">

                <li v-for="(item, index) in card.list" :key="index" style="display: list-item;"><span>{{item}}</span></li>
    
              </ul>
              <div class="flex items-center gap-4 " style="margin-top: auto;">
                <a href="" style="display: flex; align-items: center; gap: 16px; padding: 8px; border-radius: 4px; text-decoration: none; font-size: 16px; color: white; background-color: #7f5af0;"> 
                  <img width="24" height="24" src="/public/github-icon.svg" alt="">
                  <span class="">{{$t('button_span') }}</span>
                </a>
                <a href="" style="display: flex; align-items: center; gap: 16px; padding: 8px; border-radius: 4px; text-decoration: none; font-size: 16px; color: white; background-color: #7f5af0;"> 
                  <img width="24" height="24" src="/public/external-icon.svg" alt="">
                  <span class="">{{$t('button_span_1') }}</span>
                </a>
              </div>
            </div>
          </div>
        </div>

        <div v-else class="grid grid-cols-1 gap-4 md:grid-cols-2" style="color: var(--background-color-luna);">
          <div
            v-for="(card, i) in cards.secondCards"
            :key="i"
            class="item flex flex-col  rounded-lg"
            style="
              box-shadow:
                0 3px 6px rgba(0, 0, 0, 0.16),
                0 3px 6px rgba(0, 0, 0, 0.23);
              background-color: var( --background-color-primary);
              overflow: hidden;
            "
          >
          <div style="display: block;
    width: 100%;
    height: 400px;
    object-fit: cover;
    border-top-left-radius: 4px;
    border-top-right-radius: 4px; position: relative;">
          <span class="absolute top-2/4 left-2/4 text-6xl" style="transform: translate(-50%, -50%); color: white;">{{$t(card.soon)}}</span>
            <img v-bind:src="card.image" v-bind:alt="card.image"/>
    </div>
            <div class="flex flex-col p-6 h-full">
              <h3 class="mb-4 font-black text-2xl leading-tight">{{card.title }}</h3>
              <p>{{$t(card.description)}}</p>
              <div class="my-5" style="background-color: #7f5af0; padding: 1px"></div>
              <h4 class="mb-4 font-black text-2xl leading-tight">{{ $t(card.stack_list_title) }}</h4>
              <ul style="list-style: square inside;">
                <li v-for="(item, index) in card.list_dom" :key="index" style="display: list-item;"><span>{{item}}</span></li>
 
              </ul>
              <div class="flex items-center gap-4" style="margin-top: auto;">
                <a :href="card.Github" style="display: flex; align-items: center; gap: 16px; padding: 8px; border-radius: 4px; text-decoration: none; font-size: 16px; color: white; background-color: #7f5af0;"> 
                  <img width="24" height="24" src="/public/github-icon.svg" alt="">
                  <span class="">{{$t('button_span') }}</span>
                </a>
                <a :href="card.public" style="display: flex; align-items: center; gap: 16px; padding: 8px; border-radius: 4px; text-decoration: none; font-size: 16px; color: white; background-color: #7f5af0;"> 
                  <img width="24" height="24" src="/public/external-icon.svg" alt="">
                  <span class="">{{$t('button_span_1') }}</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import { useI18n } from 'vue-i18n';

export default {
  name: 'App',
  
  setup() {
    const showFirstCards = ref(true)
    const { t } = useI18n();
    const cards = ref({
      firstCards: [
        { 
          title: 'JED 3D STUDIO',
          description: 'component.card.description_layout1',
          stack_list_title: "component.card.stack",
          list: [
            "html",
            "css",
          ],
          image: new URL('@/assets/Image (152).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio',
          public:''
        },
      
        
      ],
      secondCards: [
      { 
          title: 'JED 3D STUDIO',
          description: 'component.card.description1',


          stack_list_title: "component.card.stack",
          soon:'component.card.soon1',

          list_dom: [
            'JavaScript (ES6)',
            'Less',
            
          ],
          image: new URL('@/assets/Image (155).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/3d_jed',
          public:''
        },
        { title: 'Salvator Cyber Club',
          description: 'component.card.description2',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon2',

          list_dom:[
             "VUE",
             "Tailwind",
             "Vue Router"
          ],
          image: new URL('@/assets/Image (154).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/Salvator',
          public:''
        },
        { title: 'Vue-Shop',
          description: 'component.card.description3',

          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon3',

          list_dom:[
             "VUE",
             "Tailwind",
             "Vue Router"
          ],
          image: new URL('@/assets/Image (160).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/VUE-Shop',
          public:''
        },
        { title: 'ZABITOV',
          description: 'component.card.description4',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon4',
          list_dom:[
             "JavaScript (ES6)",
             "less",
          ],
          image: new URL('@/assets/Image (164).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/turism',
          public:'https://zabitov-tour05.ru'
        },
        { title: 'Weather forecast',
          description: 'component.card.description5',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon5',
          list_dom:[
             "VUE",
             "Tailwind",
             "API"
          ],
          image: new URL('@/assets/Image (150).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/Weather-Forecast-VUE-',
          public:''
        },
        { title: 'Portfolio',
          description: 'component.card.description6',
          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon4',

          list_dom:[
             'Vue',
             'Vue i18n',
             'Tailwind',

          ],
          image: new URL('@/assets/Image (161).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/Portfolio-Vue',
          public:''
        },
        { title: 'Тестовое задание 1',
          description: 'component.card.description7',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon6',

          list_dom:[
             'JavaScript (ES6)',
             'Less',
             'Swiper',
          ],
          image: new URL('@/assets/Image (152).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/Test-task',
          public:''
        },

        { title: 'Тестовое задание 2',
          description: 'component.card.description8',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon5',
          list_dom:[
             "VUE",
             "Tailwind",
             "API"
          ],
          image: new URL('@/assets/Image (150).jpg', import.meta.url).href,
          Github: 'https://github.com/JED-Studio/Weather-Forecast-VUE-',
          public:''
        },
        { title: 'Тестовое задание 3',
          description: 'component.card.description9',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon7',
          list_dom:[
             "VUE",
             "Vue Router",
             "Tailwind",
             
          ],
          image: new URL('@/assets/Image (121).png', import.meta.url).href,
          Github: 'https://jed-studio.github.io/Qpick/',
          public:''
        },
        { title: 'Тестовое задание 4',
          description: 'component.card.description10',


          stack_list_title: "component.card.stack",
          stack_list: "VUE",
          soon:'component.card.soon7',
          list_dom:[
             "VUE"
          ],
          image: new URL('@/assets/Image (120).png', import.meta.url).href,
          Github: 'https://jed-studio.github.io/Qpick/',
          public:''
        },
      ]
    })

    return {
      showFirstCards,
      cards
    }
  }
}


</script>

<style scoped>
.tabs_btn:hover{
  background-color: #7f5af0;
  color: rgb(255, 255, 255);
}

.tabs_btn.active, .tabs_btn.active svg {
  background-color: #7f5af0;
  color: rgb(255, 255, 255) !important;
  fill: white;
}

.tabs_btn:hover svg {
  fill: white;
}

li::marker{
  color: #7f5af0;
}

@media (max-width: 768px) {

}
</style>
