<template>
  <Carousel v-bind="settings" :breakpoints="breakpoints" :autoplay="2000" :wrap-around="true">
    <Slide v-for="slide in slides" :key="slide">
      <img :src="slide.src" alt="" class="carousel__item">
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Pagination, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'App',
  components: {
    Carousel,
    Slide,
    Navigation,
    Pagination
  },
  data: () => ({
    slides: [
      { index: 1,
        src: require('@/assets/001.jpg')},
      { index: 2,
        src: require('@/assets/002.jpg')},
      { index: 3,
        src: require('@/assets/003.jpg')},
      { index: 4,
        src: require('@/assets/004.jpg')},
      { index: 5,
        src: require('@/assets/005.jpg')}
      ],
    // carousel settings
    settings: {
      itemsToShow: 1,
      snapAlign: 'start',
    },
    // breakpoints are mobile first
    // any settings not specified will fallback to the carousel settings
    breakpoints: {
      // 1024 and up
      1024: {
        itemsToShow: 3,
        snapAlign: 'start',
      },
    },
  }),
})
</script>


<style>
.carousel__item {
  object-fit: cover;
  height: 100%;
  width: 100%;
  background-color: var(--vc-clr-primary);
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 16px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
