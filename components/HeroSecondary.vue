<template>
  <div class="w-full h-[45dvh] relative flex justify-center">
    <img
      src="/images/hero-secondary.png"
      class="w-full h-full object-cover opacity-50 dark:opacity-70 object-top"
      alt="hero_image"
    />
    <div
      class="absolute bg-bg-primary dark:bg-dark-bg-secondary w-[30dvw] h-[18dvh] bottom-0 rounded-tl-[50px] rounded-tr-[50px] flex flex-col gap-y-3 justify-center items-center"
    >
      <h1 class="text-5xl font-bold dark:text-off-white">{{ title }}</h1>
      <p class="text-md dark:text-white-primary-2">{{ subtitle }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
  subtitle: string;
}>();
</script>

<style scoped></style>
