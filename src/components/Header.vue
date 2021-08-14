<template>
   
   <!-- HEADER -->
   <section class="header" >
      <div class="logo">
         <img class="yt-logo" src="src/assets/yt_logo_rgb_light.png" alt="YT-Logo" />
         <div class="icons">
            <i class="far fa-bell"></i>
            <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/search/v15/24px.svg" width="30%"></object>
            <img src="src/assets/hero.png" width="50" alt="profile" />
         </div>
      </div>
      <div class="menu">
         <span>
            <i class="far fa-compass"></i>
            Explore
         </span>
         <template v-for="explore in explores" :key="explore">
            <span @click="setCurrent(explore)" :class="explore === itemActive ? 'active' : ''">
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
               'Semua',
               'Live',
               'video mix',
               'Entertainment',
               'Music',
               'Sports',
               'Games'
               ],
            itemActive: 'Semua'
         }
      },
      methods: {
         setCurrent(value) {
            this.itemActive = value;
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
            margin-bottom: .2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 0 .8rem;
            border-bottom: 2px solid $primary-light;
            
            .yt-logo {
               display: block;
               width: 110px;
               height: 28px;
            }
            
            .icons {
               width: 30%;
               height: 20px;
               display: flex;
               justify-content: space-between;
               align-items: center;
               
               i {
                  &:first-child {
                     
                     position: relative;
                     &::after {
                        display: block;
                        content: '9+';
                        color: white;
                        border-radius: 50%;
                        font-size: .7rem;
                        padding: .2rem;
                        background: #e02d2d;
                        position: absolute;
                        top: -8px;
                        right: -8px;
                     }
                  }
               }
               
               img {
                  width: 30%;
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
            margin-top: 1rem;
            
            &::-webkit-scrollbar {
               display: none;
            }
            
            .active {
               background: $secondary-light;
               color: white;
            }
            
            span {
               font-size: 1rem;
               border-radius: 12px;
               padding: .4rem .5rem;
               margin-right: .5rem;
               background: $primary-light;
               color: $secondary-light;
               white-space: nowrap;
               text-overflow: ellipsis;
               border: 1px solid $secondary-light;
                  
               &:first-child {
                  color: black;
                  background: $primary-light;
                  margin-right: 1.5rem;
                  padding: .5rem .75rem;
                  position: relative;
                  border-radius: 0;
                  border: none;
                  
                  &::after {
                     display: block;
                     content: '';
                     position: absolute;
                     right: -.65rem;
                     top: 0;
                     height: 100%;
                     width: 1px;
                     background: $secondary-light;
                  }
               }
            }
         }
      }
   }
   
</style>