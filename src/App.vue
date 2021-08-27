<template>
  <h1>Swiper 7.0.1 bug</h1>
  <p>
    <code>display: flex</code>
    on swiper's parent
  </p>
  <p>
    <code>overlow: hidden</code>
    on swiper
  </p>

  <div style="display: flex">
    <swiper style="overflow: visible" :space-between="16" :slides-per-view="7">
      <swiper-slide v-for="client in clients" :key="client.img">
        <img :src="client.img" :alt="client.text" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';
import 'swiper/css/navigation';

const clients = [
  { img: 'https://picsum.photos/seed/42a/300/180' },
  { img: 'https://picsum.photos/seed/42b/300/180' },
  { img: 'https://picsum.photos/seed/42c/300/180' },
  { img: 'https://picsum.photos/seed/42d/300/180' },
  { img: 'https://picsum.photos/seed/42e/300/180' },
  { img: 'https://picsum.photos/seed/42f/300/180' },
  { img: 'https://picsum.photos/seed/42g/300/180' },
];
</script>

<style>
body {
  font-family: sans-serif;
}
img {
  width: 100%;
}
</style>
