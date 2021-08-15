<template>
   <section class="card-video">
      <div class="thumb">
         <img :src="srcThumb" />
         <span class="minutes">10:21</span>
      </div>
      <div class="info">
         <span>
            <img src="src/assets/hero.png" />
         </span>
         <span>
            <p class="title">
               {{ title }}
               <object data="https://fonts.gstatic.com/s/i/materialiconsoutlined/more_vert/v17/24px.svg" type=""></object>
            </p>
            <p class="subtitle">
               {{ subtitle }}
            </p>
         </span>
      </div>
   </section>
</template>

<script>
   export default {
      name: 'CardVideo',
      inheritAttrs: false,
      props: {
         title: String,
         subtitle: String,
         srcThumb: String
      }
   }
</script>

<style lang="scss">

   @import 'src/style/variabel.scss';

   .card-video {
      width: 100%;
      margin-top: 1rem;
      margin-bottom: 1.5rem;
      border-bottom: 5px solid $primary-light;
      
      .thumb {
         position: relative;
         
         img {
            max-width: 100%;
            line-height: 0;
            display: block;
         }
         
         .minutes {
            color: white;
            background: black;
            font-size: .75rem;
            padding: .2rem .4rem;
            position: absolute;
            right: 10px;
            bottom: 10px;
         }
      }
      
      .info {
         width: 100%;
         padding: 0;
         display: flex;
         flex-wrap: nowrap;
         align-items: center;
         
         span {
            display: block;
            max-width: 80%;
            
            
            &:first-child {
               width: 12%;
               margin-left: .5rem;
               
               img {
                  width: 100%;
                  line-height: 0;
                  display: block;
                  background: $primary-light;
                  border-radius: 50%;
               }
            }
            
            &:nth-child(2) {
               margin-left: .5rem;
               
               .title {
                  font-size: .9rem;
                  color: black;
                  display: flex;
                  align-items: center;
                  padding: 0;
                  margin-bottom: .5rem;
                  
                  object {
                     margin-left: .5rem;
                  }
               }
               
               .subtitle {
                  font-size: .8rem;
                  margin-top: 0;
                  color: $secondary-light;
               }
            }
         }
      }
   }
</style>