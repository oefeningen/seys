<template>
  <div>
    <header-menu />
    <div id="home"><templateHero /></div>
    <!-- <div id="about"><aboutComponent /></div> -->
    <div id="portfolio"><portfolioGallery /></div>

    <div class="shane_tm_section" id="news">
      <div class="shane_tm_about">
        <div class="container">
          <hero-carousel w-full overflow />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import headerMenu from 'src/components/headerMenu.vue';
import heroCarousel from 'src/components/heroCarousel.vue';
import aboutComponent from 'src/components/aboutComponent.vue';
import templateHero from 'src/components/templateHero.vue';
import portfolioGallery from 'src/components/portfolioGallery.vue';
</script>

<style lang="scss" scoped></style>
