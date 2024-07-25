<template>
  <div class="section_work">
    <div class="container max-w-7xl mx-auto pl-4 pr-4">
      <div class="py-4 text-white">
        <h2
          style="
            text-align: center;
            margin-bottom: 32px;
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 900;
          "
        ></h2>
        <div class="flex justify-center gap-4">
          <button
            @click="showFirstCards = true"
            class="tabs_btn cursor-pointer flex justify-center items-center gap-1 rounded"
            style="
              font-size: 16px;
              border: 1px solid #7f5af0;
              padding: 12px 16px;
              transition:
                background-color 0.2s linear,
                fill 0.2s linear;
            "
          >
            Показать первые карточки
          </button>
          <button
            @click="showFirstCards = false"
            class="tabs_btn tabs_btn--active cursor-pointer flex justify-center items-center gap-1 rounded"
            style="
              font-size: 16px;
              border: 1px solid #7f5af0;
              padding: 12px 16px;
              transition:
                background-color 0.2s linear,
                color 0.2s linear;
            "
          >
            Показать вторые карточки
          </button>
        </div>

        <div v-if="showFirstCards" class="grid grid-cols-2 gap-4">
          <div
            v-for="(card, i) in cards.firstCards"
            :key="i"
            class="item flex flex-col rounded-lg"
            style="
              box-shadow:
                0 3px 6px rgba(0, 0, 0, 0.16),
                0 3px 6px rgba(0, 0, 0, 0.23);
              background-color: #202020;
              overflow: hidden;
            "
          >
            <img :src="card.image" :alt="card.image" />
            <div class="p-6">
              <h3 class="mb-4 font-black text-2xl leading-tight">Лох</h3>
              <p>КОнчв</p>
              <div class="my-5" style="background-color: #7f5af0; padding: 1px"></div>
              <h4 class="mb-4 font-black text-2xl leading-tight">Палуба</h4>
              <ul>
                <li class=""><span>Палчик</span></li>
                <li class=""><span>аьм</span></li>
                <li class=""><span>Стоп</span></li>
                <li class=""><span>Стоп</span></li>
                <li class=""><span>Стоп</span></li>
                <li class=""><span>Стоп</span></li>
              </ul>
            </div>
          </div>
        </div>

        <div v-else class="grid grid-cols-2 gap-4">
          <div
            v-for="(card, i) in cards.secondCards"
            :key="i"
            class="item flex flex-col rounded-lg"
            style="
              box-shadow:
                0 3px 6px rgba(0, 0, 0, 0.16),
                0 3px 6px rgba(0, 0, 0, 0.23);
              background-color: #202020;
              overflow: hidden;
            "
          >
            <img :src="card.image" :alt="card.image" />
            <div class="p-6">
              <h3 class="mb-4 font-black text-2xl leading-tight">Лох</h3>
              <p>КОнчв</p>
              <div class="my-5" style="background-color: #7f5af0; padding: 1px"></div>
              <h4 class="mb-4 font-black text-2xl leading-tight">Палуба</h4>
              <ul>
                <li class=""><span>Палчик</span></li>
                <li class=""><span>аьм</span></li>
                <li class=""><span>Стоп</span></li>
                <li class=""><span>Стоп</span></li>
                <li class=""><span>Стоп</span></li>
                <li class=""><span>Стоп</span></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'App',
  setup() {
    const showFirstCards = ref(true)
    const cards = ref({
      firstCards: [
        { 
          title: "JED 3D STUDIO",
          description: "Созданный сайт для 3D студии специализируется на моушен дизайне и предлагает портфолио работ с использованием различных программ.",
          stack_list_title: "Стек технологий:",
          stack_list: "JavaScript (ES6)",
          links: "Less",
          image: '/public/Снимок экрана (152).jpg',
        
        },
        { title: "Salvator Cyber Club",
          description: "Разработка одностраничного сайта с использованием HTML, CSS и JavaScript.",
          stack_list_title: "Стек технологий:",
          stack_list: "VUE",
          links: "Tailwind",
          links1: "Vue Router",
          image: "/public/Снимок экрана (154).jpg",
        },
        { image: '/public/Снимок экрана (160).jpg', text: 'Карточка 3' }
      ],
      secondCards: [
        { image: '/public/Снимок экрана (160).jpg', text: 'Карточка 4' },
        { image: '/public/Снимок экрана (152).jpg', text: 'Карточка 5' },
        { image: '/public/Снимок экрана (154).jpg', text: 'Карточка 6' }
      ]
    })

    return {
      showFirstCards,
      cards
    }
  }
}
</script>

<style>
.tabs_btn:hover {
  background-color: #7f5af0;
}

.tabs_btn:hover svg {
  fill: white;
}
</style>
