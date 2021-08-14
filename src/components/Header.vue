<template>
   
   <!-- HEADER -->
   <section class="header" >
      <div class="logo">
         <img class="yt-logo" src="src/assets/yt_logo_rgb_light.png" alt="YT-Logo" />
         <div class="icons">
            <i class="far fa-bell"></i>
            <i class="fa fa-search"></i>
            <div>
               <img src="src/assets/hero.png" width="50" alt="profile" />
            </div>
         </div>
      </div>
      <div class="menu">
         <span>
            <i class="far fa-compass"></i>
            Explore
         </span>
         <template v-for="explore in explores" :key="explore">
            <span>
               {{ explore }}
            </span>            
         </template>
      </div>
      
   </section>
   
</template>

<script>
   
   export default {
      name: 'YTHeader',
      data() {
         return {
            explores: [
               'Live',
               'Entertainment',
               'Music',
               'Sports',
               'Games'
               ]
         }
      }
   }
   
</script>

<style lang="scss">
   
   @import "src/style/variabel.scss";
   
   #app {
      font-size: 24px;
      font-family: Sans-Serif;
      margin: 0;
      padding: 0;
      
      .header {
         padding: 1.5rem 1rem;
         
         .logo {
            background: white;
            margin-bottom: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            
            .yt-logo {
               display: block;
               width: 110px;
               height: 32px;
            }
            
            .icons {
               width: 30%;
               height: 20px;
               display: flex;
               justify-content: space-between;
               align-items: center;
               
               img {
                  width: 30px;
                  background: white;
                  border-radius: 50%;
                  border: 2px solid whitesmoke;
               }
            }
         }
         
         .menu {
            display: flex;
            min-width: 100%;
            overflow: scroll;
            overflow-y: hidden;
            margin-top: 1.5rem;
            
            &::-webkit-scrollbar {
               display: none;
            }
            
            span {
               font-size: 1rem;
               border-radius: 12px;
               padding: .2rem .5rem;
               margin-right: .5rem;
               background: $secondary-light;
               color: white;
               border: 1px solid $primary-light;
                  
               &:first-child {
                  color: black;
                  border: 1px solid $secondary-light;
                  background: $primary-light;
                  margin-right: 1.5rem;
                  min-width: 25%;
                  position: relative;
                  
                  &::after {
                     display: block;
                     content: '';
                     position: absolute;
                     right: -.65rem;
                     top: 0;
                     height: 100%;
                     width: 2px;
                     background: $secondary-light;
                  }
               }
            }
         }
      }
   }
   
</style>