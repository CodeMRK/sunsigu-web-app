<template>
  <section
    class="py-12 px-2 bg-bg-primary dark:bg-dark-bg-primary"
    id="about-us"
  >
    <h3
      class="text-black-lighten dark:text-white-primary text-[58px] font-bold mx-auto text-center mb-16"
    >
      About Us
    </h3>

    <div class="flex items-center flex-col gap-y-36">
      <AboutUsCard
        v-for="item in aboutItems"
        :key="item.title"
        :item="item"
        :image-position="item.imagePosition"
      />
    </div>
  </section>
</template>

<script setup lang="ts">
const aboutItems = [
  {
    title: 'Your First Class Home',
    description:
      'Enjoy first-class moments of peace and luxury during your free time! We realize that First class sunscreen for your home. Günther Sieb and his team have been creating fantastic first-class solutions for the home of discerning customers in the field of privacy and sun protection for 15 years. Sunsigu also develops inspiring solutions together with you and the best suppliers for your individual situation.',
    image:
      'https://images-cdn.ubuy.co.in/63717b97f1a8b5313b448ee5-mellcom-10x10-outdoor-patio-pergola.jpg',
    buttonText: 'Our Projects',
    imagePosition: 'end',
  },
  {
    title: 'Your Dream Space Awaits',
    description:
      'For customers, architects and services, sunsigu stands for real dream living as well as for expertise, reliability and top products! Contact us with your appointment requests, we will visit you on site and transform Your home in your luxury living space',
    image:
      'https://images-cdn.ubuy.co.in/63717b97f1a8b5313b448ee5-mellcom-10x10-outdoor-patio-pergola.jpg',
    buttonText: 'Contact Us',
    imagePosition: 'start',
  },
];
</script>

<style scoped></style>
