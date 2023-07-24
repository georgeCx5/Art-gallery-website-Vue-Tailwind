<script>
import RouterBtn from '../components/RouterBtn.vue';
import FooterComponent from '../components/FooterComponent.vue';
export default {
   data() {
      return {
         imgMapMB: "bg-[url(@/assets/images/mobile/image-map@2x.png)]",
      };
   },
   components: {
      RouterBtn,
      FooterComponent,
   }
}
</script>
<template>
   <body class=" flex flex-col items-center text-neo-white font-shoulders">
      <header :class="` flex justify-start items-start w-full max-w-[425px] h-[550px] ${imgMapMB} bg-cover bg-center`">
         <RouterLink to="/" draggable="false">
            <RouterBtn router-text="Back to Home" />
         </RouterLink>
      </header>
      <main class=" flex flex-col items-start gap-12 max-w-[425px] px-4 py-12 bg-neo-black font-black">
         <h1 class=" text-[50px] leading-[45px] uppercase">
            Our location</h1>
         <div class=" flex flex-col gap-5">
            <h3 class=" text-neo-gold text-[32px] leading-[32px] uppercase">
               99 King Street</h3>
            <div class=" flex flex-col gap-5 text-[18px] leading-[28px] font-light font-outfit">
               <div class=" flex flex-col">
                  <h5>Newport</h5>
                  <h5>RI 02840</h5>
                  <h5>United States of America</h5>
               </div>
               <p>
                  Our newly opened gallery is located near the Edward King House on 99 King
                  Street, the Modern Art Gallery is free to all visitors and open seven days
                  a week from 8am to 9pm.
               </p>
            </div>
         </div>
      </main>
      <FooterComponent :is-main-footer="false" />
   </body>
</template>