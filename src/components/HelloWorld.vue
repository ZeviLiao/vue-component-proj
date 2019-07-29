<template>
  <div>
    <!-- swiper -->
    <swiper :options="swiperOption">
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide1+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide2+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide3+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide4+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide5+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide6+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide7+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide8+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide9+a" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://via.placeholder.com/150&text=Slide10+a" alt />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
    {{currentIndex}}
  </div>
</template>

<script>
import "swiper/dist/css/swiper.css";

import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  components: {
    swiper,
    swiperSlide
  },
  data() {
    const currentInstance = this;
    return {
      // swiperOption: {
      //   slidesPerView: 4,
      //   spaceBetween: 30,
      //   centeredSlides: true
      // }

      swiperOption: {
        loop: true,
        slidesPerView: "auto",
        centeredSlides: true,
        spaceBetween: 30,
        on: {
          slideChange() {
            currentInstance.currentIndex =
              this.activeIndex % currentInstance.banners.length || 0;
          }
        },
        autoplay: {
          delay: 5000
        },
        speed: 1000
      }
    };
  }
};
</script>