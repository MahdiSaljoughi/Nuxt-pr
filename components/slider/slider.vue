<template>
  <div>
    <swiper
      :spaceBetween="30"
      :centeredSlides="true"
      :autoplay="{
        delay: 5000,
        disableOnInteraction: false,
      }"
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :modules="modules"
      id="slider"
    >
      <swiper-slide>
        <img class="hidden md:block" src="/p1.jpg" alt="p1" srcset="" />
        <img class="block md:hidden" src="/public/posterMobileTcl.jpg" alt="" srcset="" />
      </swiper-slide>
      <swiper-slide>
        <img class="hidden md:block" src="/p2.jpg" alt="p2" srcset="" />
        <img class="block md:hidden" src="/public/posterMobileHonor.webp" alt="" srcset="" />
      </swiper-slide>
      <swiper-slide>
        <img class="hidden md:block" src="/p3.jpg" alt="p3" srcset="" />
        <img class="block md:hidden" src="/posterMobileKart.webp" alt="" srcset="" />
      </swiper-slide>
      <swiper-slide>
        <img class="hidden md:block" src="/pgif.gif" alt="pgif" srcset="" />
        <img class="block md:hidden" src="/posterMobileSaat.jpg" alt="" srcset="" />
      </swiper-slide>
      <swiper-slide>
        <img class="hidden md:block" src="/pkart.webp" alt="pkart" srcset="" />
        <img class="block md:hidden" src="/posterMobileUltra.jpg" alt="" srcset="" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<style>
#slider {
  z-index: 20;
}
</style>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Autoplay, Pagination, Navigation } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>
