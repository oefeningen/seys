<template>
  <div class="hero-carousel">
    <!-- <q-carousel infinite autoplay control-type="flat" :height="windowHeight">
      <q-carousel-slide
        v-for="(slide, index) in slides"
        :key="index"
        :img-src="slide.imgSrc"
      ></q-carousel-slide>
    </q-carousel> -->

    <q-carousel
      v-model="slide"
      :height="windowHeight"
      autoplay
      infinite
      w-full
      navigate
      arrows
    >
      <q-carousel-slide name="style" class="column no-wrap flex-center">
        <!-- <q-img
          p-0
          m-0
          src="https://images.pexels.com/photos/534228/pexels-photo-534228.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          fit="none"
          spinner-color="primary"
          spinner-size="82px"
          h-full
        /> -->
        <img
          src="https://images.pexels.com/photos/937465/pexels-photo-937465.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
        />
      </q-carousel-slide>
      <q-carousel-slide name="tv" class="column no-wrap flex-center">
        <img
          src="https://images.pexels.com/photos/534228/pexels-photo-534228.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
        />
      </q-carousel-slide>
    </q-carousel>
  </div>
</template>

<script>
export default {
  name: 'HeroCarousel',
  data() {
    return {
      slide: 'style',
      slides: [
        {
          imgSrc:
            'https://images.pexels.com/photos/937465/pexels-photo-937465.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
        },
        {
          imgSrc:
            'https://images.pexels.com/photos/534228/pexels-photo-534228.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
        },
      ],
    };
  },
  computed: {
    windowHeight() {
      return window.innerHeight + 'px';
    },
  },
};
</script>

<style scoped>
.hero-carousel {
  width: 100%;
  overflow: hidden;
}
</style>
