<template>
  <div>
    <!-- swiper -->
    <swiper :options="swiperOption" style="padding:25px;">
      <swiper-slide>
        <div style>
          <img src="https://via.placeholder.com/150&text=Slide1+a" alt />
        </div>
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
    return {
      swiperOption: {
        slidesPerView: 4,
        spaceBetween: 30,
        centeredSlides: true,
        autoHeight: true,
        // initialSlide: 2,
        loop:true,
        on: {
          slideChange: function() {
            // eslint-disable-next-line no-console
            // eslint-disable-next-line no-undef
          }
        }
      }
    };
  }
};
</script>

<style>
.swiper-slide-active {
  border-radius: 10px;
  overflow: hidden;
  /* box-shadow: 0 1px 4px 0 rgba(0, 0, 0, 0.16); */
  -webkit-box-shadow: 0px 0px 24px -5px rgba(0, 0, 0, 0.72);
  -moz-box-shadow: 0px 0px 24px -5px rgba(0, 0, 0, 0.72);
  box-shadow: 0px 0px 24px -5px rgba(0, 0, 0, 0.72);
  background-color: #ffffff;
}
</style>