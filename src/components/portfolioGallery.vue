<template>
  <div relative>
    <p text-white>-</p>
    <q-tabs v-model="tab" class="text-grey">
      <q-tab name="alles" label="alles" />
      <q-tab
        :name="rubriek"
        :label="rubriek"
        v-for="rubriek in rubrieken"
        :key="rubriek"
      />
    </q-tabs>
    <div class="fit row wrap justify-center items-start content-start">
      <div v-for="(image, index) in FilteredImages" :key="image.portfolioName">
        <portfolioItem
          :image="image"
          @click="initLightbox(index)"
          animate-fade-in
        />
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
const tab = ref('alles');
const slides = ref([]);

const initLightbox = (id) => {
  // slides.value = image.slides;
  productIndex = id;
  toggler.value = true;
};

const rubrieken = computed(() => {
  var rub = [];
  for (var i = 0; i < images.value.length; i++) {
    if (!rub.includes(images.value[i].portfolioType)) {
      rub.push(images.value[i].portfolioType);
    }
  }
  return rub;
});

const FilteredImages = computed(() => {
  var filtered = [];
  for (var i = 0; i < images.value.length; i++) {
    if (images.value[i].portfolioType == tab.value || tab.value == 'alles') {
      filtered.push(images.value[i]);
    }
  }

  return filtered;
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
    portfolioName: 'Melkweg',
    portfolioType: 'Modern wonen',
    categorie: 'wonen',
    thumb: '/portfolio/melkweg/01.jpg',
    slides: [
      '/portfolio/melkweg/01.jpg',
      '/portfolio/melkweg/02.jpg',
      '/portfolio/melkweg/03.jpg',
      '/portfolio/melkweg/04.jpg',
      '/portfolio/melkweg/05.jpg',
      '/portfolio/melkweg/06.jpg',
      '/portfolio/melkweg/07.jpg',
    ],
  },
  {
    portfolioName: 'Landelijke hoeve Vana',
    portfolioType: 'Landelijk wonen',
    categorie: 'wonen',
    thumb: '/portfolio/landelijk_vana/01.jpg',
    slides: [
      '/portfolio/landelijk_vana/01.jpg',
      '/portfolio/landelijk_vana/02.jpg',
      '/portfolio/landelijk_vana/03.jpg',
      '/portfolio/landelijk_vana/04.jpg',
      // '/portfolio/landelijk_vana/05.jpg',
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
    portfolioName: 'Speelplaats basisschool Merkem',
    portfolioType: 'openbaar nut',
    categorie: 'openbaar',
    thumb: '/portfolio/merkem/01.jpg',
    slides: [
      '/portfolio/merkem/01.jpg',
      '/portfolio/merkem/02.jpg',
      '/portfolio/merkem/03.jpg',
      '/portfolio/merkem/04.jpg',
      '/portfolio/merkem/05.jpg',
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
  {
    portfolioName: 'Koppelwoning Ichtegem',
    portfolioType: 'Modern wonen',
    categorie: 'wonen',
    thumb: '/portfolio/koppelwoning_ichtegem/01.jpg',
    slides: [
      '/portfolio/koppelwoning_ichtegem/01.jpg',
      '/portfolio/koppelwoning_ichtegem/02.jpg',
      '/portfolio/koppelwoning_ichtegem/03.jpg',
    ],
  },
  {
    portfolioName: 'Koppelwoning Kaaskerke',
    portfolioType: 'Modern wonen',
    categorie: 'wonen',
    thumb: '/portfolio/koppelwoning_kaaskerke/01.jpg',
    slides: [
      '/portfolio/koppelwoning_kaaskerke/01.jpg',
      '/portfolio/koppelwoning_kaaskerke/02.jpg',
      // '/portfolio/koppelwoning_kaaskerke/03.jpg',
    ],
  },
]);
</script>

<style lang="scss" scoped></style>
