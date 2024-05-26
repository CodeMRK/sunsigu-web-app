<template>
  <div
    class="bg-[#fff8f8] dark:bg-gray-primary w-[620px] shadow-xl py-3 px-6 flex flex-col gap-4 rounded-md"
  >
    <img src="/images/quote-up.png" alt="qoute" class="w-[45px]" />
    <p class="text-[18px] text-gray-lighten dark:text-off-white tracking-wider">
      Pellentesque etiam blandit in tincidunt at donec. Eget ipsum dignissim
      placerat nisi, adipiscing mauris non.
    </p>
    <div class="flex flex-row justify-between items-center">
      <div class="flex flex-row items-center gap-4">
        <img
          src="/images/user-image-placeholder.png"
          alt="user-placeholder"
          class="rounded-full w-12 h-12"
        />
        <p class="text-[18px] font-bold dark:text-off-white">Jane Cooper</p>
      </div>
      <div class="flex items-center justify-center gap-2">
        <Icon name="noto:star" size="24px" />
        <p class="font-bold text-[18px] dark:text-off-white">4.3</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
