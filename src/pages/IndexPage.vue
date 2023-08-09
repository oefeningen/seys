<template>
  <div>
    <header-menu />
    <templateHero />

    <portfolioGallery id="portfolio" />

    <div class="shane_tm_section" id="about">
      <div class="shane_tm_about">
        <div class="container">
          <hero-carousel w-full overflow />
        </div>
        <!--  End container -->
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import headerMenu from 'src/components/headerMenu.vue';
import heroCarousel from 'src/components/heroCarousel.vue';
import templateHero from 'src/components/templateHero.vue';
import portfolioGallery from 'src/components/portfolioGallery.vue';
</script>

<style lang="scss" scoped></style>
