<template>
   <PopUp>
      <template v-slot:header>
         <img src="src/assets/hero.png" />
      </template>
      <p>OKA R ABDILLAH</p>
      <template v-slot:footer>
         <small>Junior Front End Developer</small>
      </template>
   </PopUp>
   
   <YTHeader :dark-mode="isLight"></YTHeader>
   <CardVideo
   :title="info.titleVideo"
   :subtitle="info.subTitleVideo"
   :src-thumb="info.thumb">
   </CardVideo>
   <!-- Shorts video wrapper -->
   <Shorts></Shorts>
   <div 
   v-for="video in videos" :key="video"
   class="video-container">
      <CardVideo 
      :title="info.titleVideo"
      :subtitle="info.subTitleVideo"
      :src-thumb="info.thumb">
      </CardVideo>
   </div>
   <YTNavbar></YTNavbar>
</template>

<script>
   //imports components
   import YTHeader from './components/Header.vue';
   import YTNavbar from './components/Navbar.vue';
   import CardVideo from './components/CardVideo.vue';
   import Shorts from './components/Shorts.vue';
   import DarkModeToggle from './components/DarkModeToggle.vue';
   import PopUp from './components/PopUp.vue';
   
   export default {
      components: {
         'YTHeader': YTHeader,
         'YTNavbar': YTNavbar,
         'CardVideo': CardVideo,
         'Shorts': Shorts,
         'DarkMode': DarkModeToggle,
         'PopUp': PopUp
      },
      data() {
         return {
            videos: [1,2,3,4],
            info: {
               titleVideo: 'FULL Tutorial Cloning Youtube UI Using Vue JS and SASS | or-abdillh',
               subTitleVideo: 'or-abdillh • 65rbx ditonton • 4 hari yang lalu',
               thumb: 'src/assets/thumb.png'
            },
            isLight: true
         }
      },
      methods: {
         setMode() {
            this.isLight = !this.isLight
         }
      }
   }
</script>

<style lang="scss">
   .video-container {
      
   }
</style>

