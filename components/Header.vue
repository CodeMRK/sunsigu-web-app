<template>
  <div
    class="bg-white dark:bg-dark-bg-primary text-black px-2 py-6 items-center z-[50]"
    :class="isFixedTop ? 'navbar-fixed-top' : ''"
  >
    <div class="mx-auto max-w-7xl w-full flex justify-between">
      <Logo :theme="darkMode === 'dark' ? 'dark' : 'light'" />

      <div
        class="flex justify-center items-center gap-12 font-medium dark:text-white-primary-2"
      >
        <NuxtLink to="/projects">Projects</NuxtLink>
        <NuxtLink to="/contact-us">Contact Us</NuxtLink>
        <NuxtLink to="/#about-us">About Us</NuxtLink>
        <div class="relative group">
          <button to="/policies ">
            Policies
            <Icon name="ep:arrow-down" size="22px" class="pl-1" />
          </button>
          <div
            class="absolute hidden group-hover:flex flex-col left-0 z-10 bg-white p-4 rounded-md w-[170px]"
          >
            <NuxtLink to="/" class="py-2 border-b border-gray-primary">
              Data Protection</NuxtLink
            >
            <NuxtLink to="/" class="py-2 border-b border-gray-primary"
              >AGB SEITE 1</NuxtLink
            >
            <NuxtLink to="/" class="py-2">AGB SEITE 2</NuxtLink>
          </div>
        </div>
      </div>
      <div class="flex justify-center items-center">
        <button @click="$emit('toggleTheme')">
          <Icon
            v-if="darkMode === 'dark'"
            name="material-symbols:light-mode-sharp"
            color="white"
            size="26px"
          />
          <Icon
            v-else-if="darkMode === ''"
            name="tdesign:mode-dark"
            color="black"
            size="26px"
          />
        </button>
        <div class="relative group">
          <button class="text-yellow-primary font-medium ml-4">
            Translate
            <Icon name="emojione:flag-for-germany" size="22px" class="ml-1" />
            <Icon name="ep:arrow-down" size="24px" class="pl-1" />
          </button>
          <div
            class="absolute right-0 hidden group-hover:flex flex-col gap-3 z-10 bg-white p-4 rounded-md"
          >
            <button>
              <Icon name="emojione:flag-for-germany" size="24px" class="pr-2" />
              <span>Deutsch</span>
            </button>
            <button>
              <Icon name="circle-flags:us" size="24px" class="pr-2" />
              <span>Deutsch</span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const { darkMode } = defineProps<{
  darkMode: string;
}>();

const isFixedTop = ref(false);

watchEffect(() => {
  if (process.client) {
    window.addEventListener('scroll', () => {
      if (window.pageYOffset > 0) return (isFixedTop.value = true);
      isFixedTop.value = false;
    });
  }
});
</script>

<style scoped>
.navbar-fixed-top {
  animation-duration: 0.5s;
  animation-name: fadeInDown;
  animation-timing-function: ease-in-out;
  left: 0;
  position: fixed !important;
  right: 0;
  top: 0;
  box-shadow: 0 4px 12px -4px rgba(0, 0, 0, 0.75);
}

@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
