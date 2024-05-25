<template>
  <div
    className="green-pink-gradient rounded-2xl transition-all duration-300  hover:shadow-lg hover:shadow-[#00ff754d]"
  >
    <div
      className="flex flex-col items-center bg-tertiary  rounded-2xl transition-all duration-300  w-full relative hover:scale-[0.99] "
    >
      <div className=" bg-transparent relative w-full h-[230px]">
        <img
          src="~assets/images/placeholder-image.png"
          alt="project_image"
          className="aspect-[16/9] w-full  object-cover rounded-t-2xl"
        />
      </div>

      <div className="mt-8 px-5">
        <h3 className="text-white font-bold text-[24px]">name</h3>
        <p className="mt-2 text-secondary text-[14px]">description</p>
      </div>

      <div className="flex gap-2">
        <a
          href="{link}"
          target="_blank"
          className="bg-[#804dee] my-8 text-white font-bold px-8 py-2  rounded-lg hover:bottom-[6.1rem] hover:sm:bottom-[4.1rem] hover:shadow-violet-300 hover:shadow-md transition-all"
        >
          Visit
        </a>

        <a
          href="https://github.com"
          target="_blank"
          className="bg-[#ED9E4C] my-8 text-white font-bold px-8 py-2  rounded-lg hover:bottom-[6.1rem] hover:sm:bottom-[4.1rem] hover:shadow-violet-300 hover:shadow-md transition-all"
        >
          Source
        </a>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped></style>
