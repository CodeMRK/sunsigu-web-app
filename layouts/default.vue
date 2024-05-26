<template>
  <div :class="darkMode" class="">
    <Header @toggleTheme="toggleDarkMode" :darkMode="darkMode" />
    <slot />
  </div>
  <Footer />
</template>

<script setup lang="ts">
const darkMode = ref('');

const toggleDarkMode = () => {
  const newValue = darkMode.value === '' ? 'dark' : '';
  darkMode.value = newValue;
};
</script>

<style scoped></style>
