<template>
  <section
    class="bg-bg-secondary dark:bg-dark-bg-secondary flex flex-row justify-center items-center gap-12 pb-24 pt-20 px-2"
  >
    <div>
      <h2
        class="text-center text-yellow-primary text-[85px] font-serif leading-[110px] font-dm-serif"
      >
        12
      </h2>
      <p class="dark:text-off-white">Years Of Experience</p>
    </div>

    <div class="border-yellow-primary border border-l h-[100px]"></div>

    <div>
      <h2
        class="text-center text-yellow-primary text-[85px] font-serif leading-[110px] font-dm-serif"
      >
        85
      </h2>
      <p class="dark:text-off-white">Successful Project</p>
    </div>

    <div class="border-yellow-primary border border-l h-[100px]"></div>

    <div>
      <h2
        class="text-center text-yellow-primary text-[85px] font-serif leading-[100px] font-dm-serif"
      >
        15
      </h2>
      <p class="dark:text-off-white">Active Project</p>
    </div>
  </section>
</template>

<script setup lang="ts">
const items = [
  {
    number: 12,
    title: 'Years Of  Experience',
  },
  {
    number: 85,
    title: 'Successful Project',
  },
  {
    number: 15,
    title: 'Active Project',
  },
];
</script>

<style scoped></style>
