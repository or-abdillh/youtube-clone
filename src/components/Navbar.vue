<template>
   
   <section class="navbar">
      <span>
         <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/home/v14/24px.svg"></object>
         <small>Home</small>
      </span>
      <span>
         <object data="https://uxwing.com/wp-content/themes/uxwing/download/10-brands-and-social-media/youtube-shorts.png"></object>
         <small>Shorts</small>
      </span>
      <span>
         <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/add_circle_outline/v14/24px.svg"></object>
      </span>
      <span>
         <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/subscriptions/v10/24px.svg"></object>
         <small>Subscription</small>
      </span>
      <span>
         <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/video_library/v12/24px.svg"></object>
         <small>Koleksi</small>
      </span>
   </section>
   
</template>

<script>
   
   export default {
      name: 'YTNavbar'
   }
   
</script>

<style lang="scss">
   
   @import 'src/style/variabel.scss';
   
   .navbar {
      width: 100%;
      position: fixed;
      bottom: 0;
      display: flex;
      justify-content: space-between;
      border-top: 1px solid $secondary-light;
      padding-top: .5rem;
      background: white;
      
      span {
         display: flex;
         width: 20%;
         justify-content: center;
         align-items: center;
         flex-direction: column;
         margin-bottom: .5rem;
         
         object {
            width: 25px;
            margin-bottom: .25rem;
         }
         
         small {
            font-size: .6rem;
         }
         
         &:nth-child(2) {
            object {
               width: 20px;
            }
         }
         &:nth-child(3) {
            object {
               width: 40px;
            }
         }
      }
   }
   
</style>