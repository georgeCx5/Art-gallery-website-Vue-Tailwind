<script>
import FooterNetwork from '@/components/FooterNetwork.vue';

import logoLight from '@/assets/images/logo-light.svg?url'
import logoDark from '@/assets/images/logo-dark.svg?url'
export default {
   data() {
      return {
         logoLight,
         logoDark,
      }
   },
   components: {
      FooterNetwork,
   },
   computed: {
      getStyle() {
         return this.isMainFooter ? 'bg-neo-black text-neo-white' : 'bg-neo-gold text-neo-black'
      }
   },
   props: {
      isMainFooter: {
         Boolean,
         default: false,
      }
   }
}
</script>
<template>
   <footer :class="` flex flex-col items-start gap-y-9 max-w-[425px] px-8 py-12 ${getStyle}`">
      <div class=" select-none">
         <img v-show="isMainFooter" class=" h-10" :src="logoLight" alt="logoLight" draggable="false">
         <img v-show="!isMainFooter" class=" h-10" :src="logoDark" alt="logoDark" draggable="false">
      </div>
      <p class=" text-[16px] leading-[26px] font-outfit font-light">
         The Modern Art Gallery is free to all visitors and open seven days a week
         from 8am to 9pm. Find us at 99 King Street, Newport, USA.
      </p>
      <div class=" flex items-center gap-5">
         <FooterNetwork v-for="item in 3" :is-main="isMainFooter" :data-index="item - 1" />
      </div>
   </footer>
</template>