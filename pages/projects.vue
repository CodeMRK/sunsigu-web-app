<template>
  <section>
    <HeroSecondary title="Projects" subtitle="Home / Projects" />
    <div class="bg-primary flex flex-col justify-center py-12">
      <select
        class="bg-[#faf3ea] text-4xl font-bold py-3 px-6 rounded-md mx-auto"
      >
        <option value="">Gastro Project</option>
        <option value="">asd</option>
        <option value="">asd</option>
        <option value="">asd</option>
        <option value="">asd</option>
        <option value="">asd</option>
      </select>
      <div class="flex flex-col items-center justify-center pt-8">
        <img
          :src="imageView"
          alt="proj-img"
          class="h-[420px] w-[750px] object-cover"
        />

        <swiper
          :slidesPerView="3"
          :spaceBetween="8"
          :navigation="true"
          class="mySwiper mt-2"
          :modules="modules"
        >
          <swiper-slide
            v-for="(data, i) in Data"
            :key="i"
            class="mySwiper"
            @mouseover="imageView = data.image"
          >
            <img
              :src="data.image"
              alt="proj-img"
              class="object-cover h-[130px] w-[250px] hover:opacity-75"
            />
          </swiper-slide>
        </swiper>
      </div>
      <p class="text-gray-primary text-center max-w-[610px] mx-auto pt-8">
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
        ut aliquip ex ea commodo consequat. Duis aute irure dolor in
        reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
        pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa
        qui officia deserunt mollit anim id est laborum.
      </p>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper/modules';
import Data from '~/utils/dummyData';

import 'swiper/css';
import 'swiper/css/navigation';

const modules = [Navigation];

const imageView = ref(Data[0].image);
</script>

<style scoped>
.swiper {
  width: 750px;
  height: 100%;
}

.swiper-slide {
  width: 120px;
}
</style>
