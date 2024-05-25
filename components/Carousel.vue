<template>
  <Swiper
    :breakpoints="bp"
    :slidesPerView="1"
    :spaceBetween="5"
    :centeredSlides="true"
    :modules="[Navigation, A11y, Autoplay, EffectCoverflow]"
    :navigation="true"
    :pagination="{ clickable: true }"
    :scrollbar="{ draggable: true }"
    effect="coverflow"
    :coverflowEffect="{
      rotate: 0,
      stretch: 0,
      depth: 80,
      modifier: 1,
      slideShadows: true,
      scale: 0.75,
    }"
  >
    <SwiperSlide v-for="i in 10">
      <CarouselCard />
    </SwiperSlide>
  </Swiper>
</template>

<script>
import {
  Navigation,
  Pagination,
  Scrollbar,
  A11y,
  Autoplay,
  EffectCoverflow,
} from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/effect-coverflow';

const bp = {
  550: {
    slidesPerView: 1.5,
    spaceBetween: 10,
  },
  750: {
    slidesPerView: 2,
    spaceBetween: 10,
  },
  1000: {
    slidesPerView: 2.5,
    spaceBetween: 15,
  },
  1200: {
    slidesPerView: 3,
    spaceBetween: 15,
  },
};
</script>

<style scoped></style>
