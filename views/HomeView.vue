<script>
import RouterBtn from '../components/RouterBtn.vue';
import FooterComponent from '../components/FooterComponent.vue';

import imgHero from '@/assets/images/mobile/image-hero@2x.jpg'

export default {
   data() {
      return {
         imgHero,
      }
   },
   components: {
      RouterBtn,
      FooterComponent,
   }
}
</script>
<template>
   <body class=" flex flex-col items-center gap-[120px] text-neo-black font-shoulders">
      <header class=" flex flex-col gap-8 relative max-w-[425px]">
         <img class=" select-none" :src="imgHero" alt="imgHero" draggable="false">
         <div class=" flex flex-col gap-8 px-4">
            <h1 class=" text-[60px] leading-[55px] font-black uppercase">
               Modern Art Gallery</h1>
            <div class=" flex flex-col gap-8">
               <p class=" text-neo-gray text-[18px] leading-[28px] font-outfit font-light">
                  The arts in the collection of the Modern Art Gallery all started
                  from a spark of inspiration. Will these pieces inspire you? Visit
                  us and find out.
               </p>
               <RouterLink to="/location" draggable="false">
                  <RouterBtn router-text="Our location" :is-main="true" />
               </RouterLink>
            </div>
         </div>
      </header>
      <FooterComponent :is-main-footer="true" />
   </body>
</template>