<template>
   <section v-if="showModal" class="layer">
      <div class="modal">
         <i class="fa fa-times"></i>
         <slot name="header"></slot>
         <slot></slot>
         <slot name="footer"></slot>
      </div>
   </section>
</template>

<script>
   export default {
      name: 'PopUp',
      data() {
         return {
            showModal: true
         }
      }
   }
</script>

<style lang="scss">
   
   @import 'src/style/variabel.scss';
   
   .layer {
      position: fixed;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      z-index: 999;
      background: rgba(black, .7);
      display: grid;
      place-items: center;
      
      .modal {
         width: 65%;
         padding: 1.75rem 1.5rem;
         background: white;
         border-radius: 12px;
         box-shadow: 8px 8px 12px $secondary-dark;
         border: 2px solid $primary-dark;
         display: flex;
         justify-content: center;
         align-items: center;
         flex-direction: column;
         position: relative;
         
         img {
            width: 50%;
            background: whitesmoke;
            border-radius: 50%;
            padding: .35rem;
         }
         
         p {
            font-weight: bold;
            font-size: 1.5rem;
            margin-bottom: .25rem;
         }
         
         small {
            font-size: .95rem;
            color: $secondary-light;
         }
         
         i {
            position: absolute;
            top: 12px;
            right: 24px;
            transition: .3s ease;
            
            &:active {
               transform: scale(1.5rem);
            }
         }
      }
   }
   
</style>