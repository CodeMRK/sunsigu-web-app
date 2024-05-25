<template>
  <div
    class="flex max-w-5xl gap-12"
    :class="imagePosition === 'start' ? 'flex-row-reverse' : 'flex-row'"
  >
    <div class="flex-1 flex flex-col justify-center gap-6">
      <h1 class="text-black-lighten text-[42px] font-bold font-serif">
        {{ item.title }}
      </h1>
      <p class="md:w-[70%] tracking-wider">{{ item.description }}</p>
      <button
        class="bg-black-lighten text-white py-3 rounded-2xl w-[215px] flex items-center justify-center gap-2"
      >
        <span>
          {{ item.buttonText }}
        </span>
        <Icon name="typcn:arrow-right" color="white" size="28px" />
      </button>
    </div>
    <img
      :src="item.image"
      alt="about-us-image"
      class="h-[500px] rounded-tr-[140px] rounded-bl-[140px] flex-1"
    />
  </div>
</template>

<script setup lang="ts">
const { item, imagePosition } = defineProps<{
  item: {
    title: string;
    description: string;
    image: string;
    buttonText: string;
  };
  imagePosition: string;
}>();
</script>

<style scoped></style>
