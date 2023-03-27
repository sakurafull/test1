<template>
  <div class="hello">
  <swiper 
    :modules="modules"
    navigation
    :pagination="{ clickable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
  >
      <swiper-slide>
        <img src="../assets/tp5.jpg" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/tp2.jpg" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/tp3.jpg" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/tp4.jpg" alt="">
      </swiper-slide>
  </swiper>
  </div>
</template>

<script>
import { Autoplay, Navigation, Pagination, A11y } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';


export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Autoplay,Navigation, Pagination, A11y],
      };
    },
  };
</script>

<style scoped>
img{
  width: 100%;
}
</style>
