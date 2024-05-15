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
            <img src="/p1.jpg" alt="p1" srcset="" />
          </swiper-slide>
          <swiper-slide>
            <img src="/p2.jpg" alt="p2" srcset="" />
          </swiper-slide>
          <swiper-slide>
            <img src="/p3.jpg" alt="p3" srcset="" />
          </swiper-slide>
          <swiper-slide>
            <img src="/pgif.gif" alt="pgif" srcset="" />
          </swiper-slide>
          <swiper-slide>
            <img src="/pkart.webp" alt="pkart" srcset="" />
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
