<template>
   <!-- HEADER -->
   <section class="header">
      <div class="logo">
         <img class="yt-logo" src="src/assets/yt_logo_rgb_light.png" alt="YT-Logo" />
         <div class="icons">
            <i class="fab fa-chromecast"></i>
            <i class="far fa-bell"></i>
            <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/search/v15/24px.svg" ></object>
            <img
            @click="$emit('popup-click')"
            src="src/assets/hero.png" width="50" alt="profile" />
         </div>
      </div>
      <div class="menu">
         <span>
            <i class="far fa-compass"></i>
            Eksplorasi
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
      props: {
         darkMode: {
            required: true,
            type: Boolean,
            default: true
         }
      },
      data() {
         return {
            explores: [
               'Semua',
               'Live',
               'Kartun',
               'Video mix',
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
   @import "src/style/ClassMode.scss";
   
   #app {
      font-size: 24px;
      font-family: Sans-Serif;
      margin: 0;
      padding: 0;
      
      .header {
         background: white;
         
         .logo {
            margin-bottom: .2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 1rem;
            border-bottom: 2.5px solid $primary-light;
            
            .yt-logo {
               display: block;
               height: 20px;
            }
            
            .icons {
               width: 50%;
               height: 20px;
               display: flex;
               justify-content: space-between;
               align-items: center;
               
               object {
                  margin-right: 1rem;
               }
               
               i {
                  margin-right: 1rem;
                  font-size: 1.2rem;
                  &:nth-child(2) {
                     position: relative;
                     &::after {
                        display: block;
                        content: '9+';
                        color: white;
                        border-radius: 50%;
                        font-size: .6rem;
                        padding: .2rem;
                        background: #e02d2d;
                        position: absolute;
                        top: -5px;
                        right: -10px;
                     }
                  }
               }
               
               img {
                  width: 20%;
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
               font-size: .85rem;
               display: flex;
               align-items: center;
               border-radius: 16px;;
               padding: .1rem .5rem;
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
                  margin-left: 1rem;
                  padding: .5rem .75rem;
                  position: relative;
                  border-radius: 0;
                  border: none;
                  
                  i {
                     margin-right: .45rem;
                     font-size: 1.5em;
                  }
                  
                  &::after {
                     display: block;
                     content: '';
                     position: absolute;
                     right: -.65rem;
                     top: 0;
                     height: 100%;
                     width: 3px;
                     background: $primary-light;
                  }
               }
            }
         }
      }
   }
   
</style>