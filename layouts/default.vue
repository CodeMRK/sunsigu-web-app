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
  darkMode.value === '' ? (darkMode.value = 'dark') : (darkMode.value = '');
};
</script>

<style scoped></style>
