<template>
   <YTHeader></YTHeader>
   <div 
   v-for="video in videos" :key="video"
   class="video-container">
      <CardVideo></CardVideo>
   </div>
   <YTNavbar></YTNavbar>
</template>

<script>
   //imports components
   import YTHeader from './components/Header.vue';
   import YTNavbar from './components/Navbar.vue';
   import CardVideo from './components/CardVideo.vue';
   
   export default {
      components: {
         'YTHeader': YTHeader,
         'YTNavbar': YTNavbar,
         'CardVideo': CardVideo
      },
      data() {
         return {
            videos: [1,2,3,4,5]
         }
      }
   }
</script>

<style lang="scss">
   .video-container {
      
   }
</style>

