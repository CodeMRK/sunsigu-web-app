<template>
  <div class="flex items-center gap-1">
    <img
      :src="theme === 'dark' ? '/logo-dark.png' : '/logo.png'"
      alt="logo"
      class="w-10 h-10"
    />
    <NuxtLink
      to="/"
      class="font-bold text-[28px] dark:text-white-primary font-dm-serif tracking-wide"
      >Sunsigu</NuxtLink
    >
  </div>
</template>

<script setup lang="ts">
const { theme } = defineProps<{
  theme: string;
}>();
</script>

<style scoped></style>
