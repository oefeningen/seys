<template>
  <div relative>
    <div class="fit row wrap justify-center items-start content-start">
      <div v-for="(image, index) in images" :key="image.portfolioName">
        {{ index }}
        <portfolioItem :image="image" @click="initLightbox(index)" />
        <!-- <FsLightbox
          :toggler="toggler"
          :sources="images[productIndex].slides"
          :key="productIndex"
          @onClose="toggler = false"
        /> -->
      </div>
    </div>
  </div>
</template>

<script setup>
import FsLightbox from 'fslightbox-vue/v3';
import portfolioItem from 'src/components/portfolioItem.vue';
import { ref, computed } from 'vue';

const toggler = ref(false);
const productIndex = ref(0);
const tab = ref(false);
const slides = ref([]);

const initLightbox = (id) => {
  // slides.value = image.slides;
  productIndex = id;
  toggler.value = true;
};

const rubrieken = computed(() => {
  return ['alles'];
});

const images = ref([
  {
    portfolioName: 'Sociale woningen Pervijze',
    portfolioType: 'Sociale woningen',
    categorie: 'wonen',
    thumb: '/portfolio/sociale_pervijze/01.jpg',
    slides: [
      '/portfolio/sociale_pervijze/01.jpg',
      '/portfolio/sociale_pervijze/02.jpg',
      '/portfolio/sociale_pervijze/03.jpg',
      '/portfolio/sociale_pervijze/04.jpg',
      '/portfolio/sociale_pervijze/05.jpg',
    ],
  },
  {
    portfolioName: 'Landelijke woning Beauvoorde',
    portfolioType: 'Landelijk wonen',
    categorie: 'wonen',
    thumb: '/portfolio/landelijk_beauvoorde/01.jpg',
    slides: [
      '/portfolio/landelijk_beauvoorde/01.jpg',
      '/portfolio/landelijk_beauvoorde/02.jpg',
    ],
  },
  {
    portfolioName: 'projectsite te Beerst',
    portfolioType: 'Landelijk wonen',
    categorie: 'wonen',
    thumb: '/portfolio/landelijk_beerst/01.jpg',
    slides: [
      '/portfolio/landelijk_beerst/01.jpg',
      '/portfolio/landelijk_beerst/02.jpg',
      '/portfolio/landelijk_beerst/03.jpg',
    ],
  },
  {
    portfolioName: 'Landelijke hoeve van Tuinen Bert',
    portfolioType: 'Landelijk wonen',
    categorie: 'wonen',
    thumb: '/portfolio/landelijk_tuinenbert/01.jpg',
    slides: [
      '/portfolio/landelijk_tuinenbert/01.jpg',
      '/portfolio/landelijk_tuinenbert/02.jpg',
      '/portfolio/landelijk_tuinenbert/03.jpg',
      '/portfolio/landelijk_tuinenbert/04.jpg',
      '/portfolio/landelijk_tuinenbert/05.jpg',
    ],
  },
  {
    portfolioName: 'Sociale woningen Hooglede',
    portfolioType: 'Sociale woningen',
    categorie: 'wonen',
    thumb: '/portfolio/sociale_hooglede/01.jpg',
    slides: [
      '/portfolio/sociale_hooglede/01.jpg',
      '/portfolio/sociale_hooglede/02.jpg',
      '/portfolio/sociale_hooglede/03.png',
    ],
  },
  {
    portfolioName: 'Landelijk Westkerke',
    portfolioType: 'Landelijk wonen',
    categorie: 'wonen',
    thumb: '/portfolio/landelijk_westkerke/01.jpg',
    slides: [
      '/portfolio/landelijk_westkerke/01.jpg',
      '/portfolio/landelijk_westkerke/02.jpg',
      '/portfolio/landelijk_westkerke/03.png',
    ],
  },
]);
</script>

<style lang="scss" scoped></style>
