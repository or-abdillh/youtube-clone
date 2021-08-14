<template>
   
   <section class="navbar">
      <span>
         <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/home/v14/24px.svg"></object>
         <small>Home</small>
      </span>
      <span>
         <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/smart_display/v8/24px.svg"></object>
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
         <small>Collections</small>
      </span>
   </section>
   
</template>

<script>
   
   export default {
      name: 'YTNavbar',
      data() {
         return { }
      }
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
      
      span {
         display: flex;
         width: 20%;
         justify-content: center;
         align-items: center;
         flex-direction: column;
         margin-bottom: .75rem;
         
         object {
            width: 25px;
         }
         
         small {
            font-size: .6rem;
         }
         
         &:nth-child(3) {
            object {
               width: 40px;
            }
         }
      }
   }
   
</style>