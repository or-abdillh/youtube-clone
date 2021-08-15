<template>
   <div class="video-wrapper">
      <img :src="thumb" alt="thumbnail" />
      <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/more_vert/v17/24px.svg"></object>
      <div class="info-video">
         <p>{{ title }}</p>
         <small>{{ views }}x ditonton</small>
      </div>
   </div>
</template>

<script>
  export default {
     name: 'ShortVideo',
     inheritAttrs: false,
     props: {
        thumb: String,
        title: String,
        views: String
     }
  }
</script>

<style lang="scss">
   
   @import 'src/style/variabel.scss';
   
   .video-wrapper {
      min-width: 45%;
      max-width: 45%;
      position: relative;
      padding: .65rem .55rem;
      box-sizing: border-box;
      
     img {
        max-width: 100%;
     }
     
     object {
        position: absolute;
        top: .75rem;
        right: .75rem;
     }
     
     .info-video {
        position: absolute;
        bottom: 0;
        color: white;
        padding: 0 .65rem;
        word-wrap: break-word;
        display: flex;
        flex-wrap: wrap;
        
        p {
           font-size: 1rem;
           display: block;
           margin-bottom: .35rem;
        }
        small {
           font-size: .8rem;
           display: block;
           margin-bottom: 1rem;
           color: $primary-light;
        }
     }
   }
   
</style>