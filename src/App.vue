<template>
   <YTHeader></YTHeader>
   <YTNavbar></YTNavbar>
</template>

<script>
   
   //imports components
   import YTHeader from './components/Header.vue';
   import YTNavbar from './components/Navbar.vue';
   
   export default {
      data(){},
      components: {
         'YTHeader': YTHeader,
         'YTNavbar': YTNavbar
      }
   }


   
</script>