<template>
  <section class="bg-bg-secondary flex flex-col items-center py-12 px-2">
    <div class="flex flex-col items-center">
      <h4 class="text-yellow-primary text-[18px] font-semibold text-center">
        Testimonials
      </h4>
      <h2 class="text-black-primary font-bold text-[52px] text-center">
        What our customer say
      </h2>
      <p class="text-gray-lighten text-[18px] text-center md:max-w-[60%]">
        Read their testimonials and discover why our expertise and dedication
        make us the top choice for high-quality outdoor design.
      </p>
    </div>

    <swiper
      :breakpoints="bp"
      :spaceBetween="50"
      :centeredSlides="true"
      :loop="true"
      :grabCursor="true"
      :modules="[Autoplay, EffectCoverflow]"
      :autoplay="{
        delay: 3000,
        disableOnInteraction: true,
      }"
      class="mySwiper mt-6"
      :effect="'coverflow'"
      :coverflowEffect="{
        rotate: 0,
        stretch: 0,
        depth: 100,
        modifier: 1,
        scale: 0.95,
        slideShadows: false,
      }"
    >
      <swiper-slide v-for="i in 10" :key="i" class="pb-8">
        <TestimonialsCard />
      </swiper-slide>
    </swiper>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/effect-coverflow';

import { Autoplay, EffectCoverflow } from 'swiper/modules';

const bp = {
  0: {
    slidesPerView: 'auto',
  },

  1800: {
    slidesPerView: 3.5,
  },
};
</script>

<style scoped>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  width: 600px;
}
</style>
