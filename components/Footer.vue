<template>
  <div class="bg-black-lighten text-[#F3F3F3] py-12 px-2">
    <div class="max-w-7xl mx-auto">
      <!-- infos  -->
      <div class="flex justify-between pt-8 pb-20">
        <!-- sunsigu info  -->
        <div class="flex-[2]">
          <Logo theme="dark" class="mb-4" />
          <div class="text-[#F9F9F9] w-[450px]">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </div>
        </div>

        <!-- project links  -->
        <div class="flex-[0.65]">
          <h2 class="mb-6 font-semibold text-[18px]">Projects</h2>
          <ul class="flex flex-col gap-2">
            <NuxtLink to="/contact-us">Contact Us</NuxtLink>
            <NuxtLink to="/#about-us">About Us</NuxtLink>
          </ul>
        </div>

        <!-- social media  -->
        <div class="flex-[0.65]">
          <h2 class="mb-6 font-semibold text-[18px]">Follow Us</h2>
          <ul class="flex flex-col gap-2">
            <li>
              <a href="https://www.facebook.com" target="_blank">Facebook</a>
            </li>
            <li>
              <a href="https://www.instagram.com" target="_blank">Instagram</a>
            </li>
          </ul>
        </div>
      </div>

      <!-- Copyright  -->
      <div class="mx-auto text-center">
        <hr />
        <p class="pt-4">Copyright © Sunsigu</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
