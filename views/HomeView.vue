<script>
import RouterBtn from '../components/RouterBtn.vue';
import FooterComponent from '../components/FooterComponent.vue';

import imgHero from '@/assets/images/mobile/image-hero@2x.jpg'
import imgGridOneMB from '@/assets/images/mobile/image-grid-1.jpg'
import imgGridTwoMB from '@/assets/images/mobile/image-grid-2.jpg'
import imgGridThreeMB from '@/assets/images/mobile/image-grid-3.jpg'

export default {
   data() {
      return {
         imgHero,
         dataImg: [
            {
               imgMB: imgGridOneMB,
            },
            {
               imgMB: imgGridTwoMB,
            },
            {
               imgMB: imgGridThreeMB,
            },
         ]
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
      <main class=" flex flex-col gap-8 max-w-[425px] px-4">
         <div class=" flex flex-col gap-6">
            <img class=" select-none" :src="dataImg[0].imgMB" alt="imgOneMB" draggable="false">
            <div class=" flex flex-col gap-5">
               <div class=" text-[50px] leading-[45px] font-black uppercase">
                  <h2>Your day</h2>
                  <h2>at the gallery</h2>
               </div>
               <p class=" text-neo-gray text-[18px] leading-[28px] font-outfit font-light">
                  Wander through our distinct collections and find new insights about
                  our artists. Dive into the details of their creative process.
               </p>
            </div>
         </div>
         <div class=" grid grid-cols-1 gap-4">
            <img class=" w-full select-none" :src="dataImg[1].imgMB" alt="imgTwoMB" draggable="false">
            <img class=" w-full select-none" :src="dataImg[2].imgMB" alt="imgTwoMB" draggable="false">
            <div class=" flex flex-col gap-6 px-6 py-12 bg-neo-black text-neo-white">
               <div class=" text-[50px] leading-[45px] font-black uppercase">
                  <h2>Come &amp; be</h2>
                  <h2>inspired</h2>
               </div>
               <p class=" text-[18px] leading-[28px] font-outfit font-light">
                  We’re excited to welcome you to our gallery and see how our collections
                  influence you.
               </p>
            </div>
         </div>
      </main>
      <FooterComponent :is-main-footer="true" />
   </body>
</template>