<template>
  <div
    class="bg-white flex justify-between text-black max-w-7xl mx-auto px-2 py-6 items-center"
  >
    <NuxtLink to="/" class="font-bold text-[20px]">Sunsigu</NuxtLink>
    <div class="flex gap-12 font-medium">
      <NuxtLink to="/projects">Projects</NuxtLink>
      <NuxtLink to="/contact-us">Contact Us</NuxtLink>
      <NuxtLink to="/about-us">About Us</NuxtLink>
      <NuxtLink to="/policies">Policies</NuxtLink>
    </div>
    <div>
      <button class="text-yellow-primary font-medium">Translate</button>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
