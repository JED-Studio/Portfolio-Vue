<script>
import { ref, computed } from 'vue';
import { useI18n } from 'vue-i18n';
export default {
  setup() {
    const isDropdownOpen = ref(false);

    const toggleDropdown = () => {
      isDropdownOpen.value = !isDropdownOpen.value;
    };

    
    const i18n = useI18n({ useScope: 'global' });
    const currentLocale = ref(localStorage.getItem('locale') || 'ru');
    i18n.locale.value = currentLocale.value;

 // Функция для смены языка
 const switchLang = (lang) => {
      i18n.locale.value = lang; 
      currentLocale.value = lang;
      localStorage.setItem('locale', lang);
    };

    // Вычисляемый свойство для флага
    const currentFlag = computed(() => {
      return currentLocale.value === 'ru' ? '/public/russia_twlp5xbebtio.svg' : '/public/united_kingdom_nsuhf1vy7yn3.svg';
    });

    return {
      isDropdownOpen,
      toggleDropdown,
      switchLang,
      currentLocale,
      currentFlag,
    };
  },
};



</script>


<template>
    <div class="dropdown" style="">
                            <button class="dropdown__btn" type="button" @click="toggleDropdown">
                                <img class="dropdown__btn-flag"  :src="currentFlag"  alt="">
                                <span class="dropdown__btn-text" style="color: var(--background-color-luna);">{{ currentLocale.toUpperCase() }}</span>
                                <svg class="dropdown__btn-icon" :class="{'dropdown__btn-icon--rotated': isDropdownOpen}"  version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 512 512" style="enable-background:new 0 0 512 512" xml:space="preserve">
                                    <path style="fill: var(--background-color-luna);" d="M505.183,123.179c-9.087-9.087-23.824-9.089-32.912,0.002l-216.266,216.27L39.729,123.179
	c-9.087-9.087-23.824-9.089-32.912,0.002c-9.089,9.089-9.089,23.824,0,32.912L239.55,388.82c4.364,4.364,10.283,6.816,16.455,6.816
	c6.172,0,12.092-2.453,16.455-6.817l232.721-232.727C514.272,147.004,514.272,132.268,505.183,123.179z"/>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                    <g></g>
                                </svg>
                            </button>
                            <ul class="dropdown__list" :class="{'dropdown__list--active': isDropdownOpen}" style="background-color: var( --background-color-luna); color: var(--background-color-primary); transition: background-color 0.2s linear,color 0.2s linear;">
                                <li>
                                    <button @click="switchLang('ru')"  class="dropdown__list-btn" data-value="ru">
                                        <img class="dropdown__btn-flag" src="/public/russia_twlp5xbebtio.svg" alt="">
                                        <span class="dropdown__lang-caption">RU</span>
                                    </button>
                                </li>
                                <li>
                                    <button @click="switchLang('en')" class="dropdown__list-btn" data-value="kk">
                                        <img class="dropdown__btn-flag" src="/public/united_kingdom_nsuhf1vy7yn3.svg" alt="">
                                        <span class="dropdown__lang-caption">KK</span>
                                    </button>
                                </li>
                                
                            </ul>
                        </div>
                
</template>

<style scoped>
.dropdown {
    position: relative;
    max-width: 100px;
}

.dropdown__btn {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 5px;
    width: 100%;
    padding: 10px;
    font-size: 16px;
    border: none;
    background-color: rgba(0,0,0,0);
    color: var(--text-color);
    cursor: pointer;
    font-family: "Museo","Segoe UI",Tahoma,Geneva,Verdana,sans-serif;
    -webkit-tap-highlight-color: rgba(0,0,0,0);
}

.dropdown__btn::after {
    display: none;
    position: absolute;
    left: 50%;
    bottom: -17px;
    content: "";
    width: 16px;
    height: 16px;
    transform: rotate(45deg) translateX(-50%);
    background-color: var(--white)
}
.dropdown__btn:focus-visible {
    outline: 2px solid var(--primary)
}

.dropdown__btn--active::after {
    display: block;
}

.dropdown__list {
    width: 100%;
    position: absolute;
    top: 50px;
    overflow: hidden;
    left: 0;
    max-height: 0;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
    background-color: white;
}

.dropdown__list--active {
    max-height: max-content;
}



.dropdown__list--active::before {
    display: block;
}

.dropdown__list-btn {
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 10px;
    border: none;
    padding: 10px;
    background-color: rgba(0,0,0,0);
}

.dropdown__lang-caption {
    display: inline-block;
    width: 100%;
    font-size: 1rem;
    text-decoration: none;
    color: var(--dark);
}

.dropdown__btn-icon {
    width: 16px;
    height: 16px;
    transition: transform .2s ease;
    
    
}

.dropdown__btn-icon path {
    fill: var(--text-color);
}

.dropdown__btn-flag {
    width: 32px;
    height: 32px;
}

.dropdown__btn-icon--rotated {
    transform: rotate(180deg);
}
</style>