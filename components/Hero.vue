<template>
  <section
    class="bg-bg-secondary dark:bg-dark-bg-secondary py-12 px-2 rounded-bl-[150px]"
  >
    <div class="max-w-[1450px] mx-auto flex justify-center items-center">
      <div class="text-black font-semibold flex-1">
        <h1 class="text-[52px] leading-[62px] dark:text-off-white">
          Elevate Your
          <span class="text-yellow-primary">Outdoor Lifestyle</span> Experience
        </h1>
        <p class="text-gray-lighten font-normal text-[18px] mt-2 md:w-[80%]">
          Benefit from our extensive experience in creating high-quality open
          spaces! Ensuring your terrace can be enjoyed all year-round.
        </p>
      </div>
      <swiper
        :slidesPerView="2.6"
        :centeredSlides="true"
        :loop="true"
        :grabCursor="true"
        :pagination="{ clickable: true }"
        :modules="[EffectCoverflow, Pagination]"
        class="flex-[1.25]"
        :effect="'coverflow'"
        :coverflowEffect="{
          rotate: 0,
          stretch: 0,
          depth: 100,
          modifier: 0.9,
          scale: 0.7,
          slideShadows: false,
        }"
      >
        <swiper-slide v-for="i in 5" :key="i" class="pb-8">
          <img
            src="/images/placeholder-image.png"
            alt="placeholder"
            class="h-[550px] w-[450px] object-cover rounded-bl-[130px]"
          />
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import 'swiper/css/effect-coverflow';

import { Autoplay, EffectCoverflow, Pagination } from 'swiper/modules';
</script>

<style scoped>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  width: 100%;
  height: 100%;
}
</style>
