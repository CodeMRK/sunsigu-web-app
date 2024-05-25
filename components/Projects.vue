<template>
  <section class="bg-bg-primary py-12 px-2">
    <div class="max-w-7xl mx-auto">
      <div class="text-center">
        <h3 class="text-black-lighten text-[40px] font-bold mx-auto">
          Our Projects
        </h3>
        <p class="md:w-[50%] mx-auto text-gray-primary mt-2">
          Discover our range of expertly crafted products designed to elevate
          your outdoor living experience. Explore our collection and transform
          your terrace into an elegant retreat!
        </p>
      </div>

      <div class="flex flex-wrap justify-center gap-12 mt-12">
        <ProjectCard v-for="i in 6" :key="i" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped></style>
