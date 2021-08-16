<template>
   <span 
   v-on:click="$emit('change-mode')"
   :class="isLight ? 'bg-dark' : 'bg-light'" class="toogle">
      <i 
      @click="changeMode" 
       v-if="isLight === false" class="fas fa-moon" ></i>
      <i 
      @click="changeMode" 
       v-else class="fas fa-sun" ></i>
   </span>
</template>

<script>
   export default {
      name: 'DarkModeToggle',
      data() {
         return {
            isLight: false
         }
      },
      methods: {
         changeMode() {
            this.isLight = !this.isLight;
         }
      }
   }
</script>

<style lang="scss">
   
   @import 'src/style/variabel.scss';
   
   .bg-dark {
      background: $primary-dark;
      color: $primary-light;
   }
   
   .bg-light {
      background: $primary-light;
      color: $primary-dark;
   }
   
   .toogle {
      width: 30px;
      height: 30px;
      position: fixed;
      padding: .5rem;
      display: grid;
      place-items: center;
      top: 50%;
      right: 1rem;
      border-radius: 50%;
      border: 1px solid;
      z-index: 9;
      transition: .3s;
      
      &:active {
         border-color: navy;
      }
   }   
   
</style>



