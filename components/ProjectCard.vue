<template>
  <div class="flex flex-col w-[520px]">
    <img
      src="https://images-cdn.ubuy.co.in/63717b97f1a8b5313b448ee5-mellcom-10x10-outdoor-patio-pergola.jpg"
      alt="project-image"
      class="h-[500px] w-full"
      :class="rounded[index]"
    />
    <div class="flex justify-between items-center pt-4">
      <div>
        <h4
          class="text-[20px] font-medium tracking-wide font-serif dark:text-white-primary-2 font-dm-serif"
        >
          GASTRO PROJECT
        </h4>
        <p class="dark:text-white-primary-2">Architecture</p>
      </div>
      <button
        class="rounded-full p-4 bg-yellow-primary flex items-center justify-center"
      >
        <Icon name="oui:arrow-right" color="black" />
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
const { index } = defineProps<{
  index: number;
}>();

const rounded = [
  'rounded-tr-[120px]',
  'rounded-tl-[120px]',
  'rounded-r-[120px]',
  'rounded-l-[120px]',
  'rounded-br-[120px]',
  'rounded-bl-[120px]',
];
</script>

<style scoped></style>
