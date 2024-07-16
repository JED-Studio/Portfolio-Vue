<template>
    <div class="flex">
      <input
        @change="toggleTheme"
        id="checkbox"
        type="checkbox"
        class="switch-checkbox"
      />
      <label for="checkbox" class="switch-label">
        <span></span>
        <span></span>
        <div
          class="switch-toggle flex items-center justify-center"
          :class="{ 'switch-toggle-checked': userTheme === 'dark-theme' }"
        >
        
<svg  class="" width="20px" height="20px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path id="luna" d="M3.32031 11.6835C3.32031 16.6541 7.34975 20.6835 12.3203 20.6835C16.1075 20.6835 19.3483 18.3443 20.6768 15.032C19.6402 15.4486 18.5059 15.6834 17.3203 15.6834C12.3497 15.6834 8.32031 11.654 8.32031 6.68342C8.32031 5.50338 8.55165 4.36259 8.96453 3.32996C5.65605 4.66028 3.32031 7.89912 3.32031 11.6835Z" stroke="#ffffff"  stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

</div>
      </label>
    </div>
  </template>
  
  <script>
  export default {
    mounted() {
      const initUserTheme = this.getTheme() || this.getMediaPreference();
      this.setTheme(initUserTheme);
    },
  
    data() {
      return {
        userTheme: "light-theme",
      };
    },
  
    methods: {
      toggleTheme() {
        const activeTheme = localStorage.getItem("user-theme");
        if (activeTheme === "light-theme") {
          this.setTheme("dark-theme");
        } else {
          this.setTheme("light-theme");
        }
      },
  
      getTheme() {
        return localStorage.getItem("user-theme");
      },
  
      setTheme(theme) {
        localStorage.setItem("user-theme", theme);
        this.userTheme = theme;
        document.documentElement.className = theme;
      },
  
      getMediaPreference() {
        const hasDarkPreference = window.matchMedia(
          "(prefers-color-scheme: dark)"
        ).matches;
        if (hasDarkPreference) {
          return "dark-theme";
        } else {
          return "light-theme";
        }
      },
    },
  };
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  .switch-checkbox {
    display: none;
  }
  
  .switch-label {
    align-items: center;
    background: var(--text-primary-color);
    border: calc(var(--element-size) * 0.025) solid var(--accent-color);
    border-radius: var(--element-size);
    cursor: pointer;
    display: flex;
    font-size: calc(var(--element-size) * 0.3);
    height: 30px;
    position: relative;
    padding: calc(var(--element-size) * 0.1);
    transition: background 0.5s ease;
    justify-content: center;
    width: var(--element-size);
    z-index: 1;
  }
  
  .switch-toggle {
    
    position: absolute;
    
    background-color: var(--background-color-primary);
    border-radius: 50%;
    top: 2,5px;
    left: 0px;
    height: 22px;
    width: 22px;
    transform: translateX(3px);
    transition: transform 0.3s ease, background-color 0.5s ease;
    
  }
  
  .switch-toggle-checked {
    transform: translateX(37px) !important;
  }

  #luna{
    stroke: var(--background-color-luna);
  }
 
  </style>
  