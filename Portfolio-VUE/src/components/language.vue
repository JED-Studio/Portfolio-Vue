<template>
    <div class="dropdown">
                            <button class="dropdown__btn" type="button">
                                <img class="dropdown__btn-flag" src="/public/russia_twlp5xbebtio.svg" alt="">
                                <span class="dropdown__btn-text">RU</span>
                                <svg class="dropdown__btn-icon" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 512 512" style="enable-background:new 0 0 512 512" xml:space="preserve">
                                    <path d="M505.183,123.179c-9.087-9.087-23.824-9.089-32.912,0.002l-216.266,216.27L39.729,123.179
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
                            <ul class="dropdown__list">
                                <li>
                                    <button class="dropdown__list-btn" data-value="ru">
                                        <img class="dropdown__btn-flag" src="/public/russia_twlp5xbebtio.svg" alt="">
                                        <span class="dropdown__lang-caption">RU</span>
                                    </button>
                                </li>
                                <li>
                                    <button class="dropdown__list-btn" data-value="kk">
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

.dropdown__btn-icon {
    transform: rotate(180deg);
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