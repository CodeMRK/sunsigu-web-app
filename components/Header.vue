<template>
    <div class="bg-white  text-black  px-2 py-6 items-center z-[50]"
        :class="isFixedTop ? 'navbar-fixed-top' : ''">
        <div class="mx-auto max-w-7xl w-full flex justify-between">
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
    </div>
</template>

<script setup lang="ts">

const isFixedTop = ref(false);

watchEffect(() => {
    if (process.client) {
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 0) return isFixedTop.value = true;
            isFixedTop.value = false;
        })
    }
})

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
