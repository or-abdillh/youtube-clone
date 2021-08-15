<template>
   <YTHeader></YTHeader>
      <CardVideo></CardVideo>
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
      }
   }
</script>