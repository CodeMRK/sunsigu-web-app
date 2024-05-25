<template>
    <div class="w-full h-[45dvh] relative flex justify-center">
        <img src="/images/hero-secondary.png" class="w-full h-full object-cover opacity-50 object-top" alt="hero_image">
        <div class="absolute bg-white w-[30dvw] h-[18dvh] bottom-0 rounded-tl-[50px] rounded-tr-[50px] flex flex-col gap-y-3 justify-center items-center">
            <h1 class="text-6xl font-bold">{{ title }}</h1>
            <p class="text-md">{{ subtitle }}</p>
        </div>
    </div>
</template>

<script setup lang="ts">
defineProps<({
    title: string,
    subtitle: string,
})>()

</script>

<style scoped>

</style>