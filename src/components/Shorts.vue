<template>
   <section class="shorts-wrapper">
      <div class="short-title">
         <object data="https://uxwing.com/wp-content/themes/uxwing/download/10-brands-and-social-media/youtube-shorts.png"></object>
         <p>
            Shorts
            <sup>beta</sup>
         </p>
      </div>
      <div>
         <template v-for="short in shorts" :key="short">
            <ShortVideo 
            thumb="src/assets/shorts.png"
            title="5 Minutes to relax your soul"
            views="1.7jt"></ShortVideo>
         </template>
      </div>
   </section>
</template>

<script>
   
   import ShortVideo from './ShortVideo.vue';

   export default {
      name: 'Shorts',
      components: {
         'ShortVideo': ShortVideo
      },
      data() {
         return {
            shorts: [1, 2, 3, 4, 5]
         }
      }
   }
</script>

<style lang="scss">
   
   @import 'src/style/variabel.scss';
   
   .shorts-wrapper {
      width: 100%;
      border-bottom: 5px solid $primary-light;
      box-sizing: border-box;
      padding-bottom: .55rem;
      
      div {
         display: flex;
         flex-wrap: nowrap;
         padding-top: 0;
         
         &:last-child {
            overflow: scroll;
            
            &::-webkit-scrollbar {
               display: none;
            }
         }
      }
      .short-title {
         padding: 0 .75rem;
         align-items: center;
         
         p {
            font-size: 1.2rem;
         }
         object {
            margin-right: .75rem;
            width: 24px;
            height: 24px;
         }
      }
   }
</style>