<template>
  <div>
    <templateHero />
    <hero-carousel w-full overflow />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import heroCarousel from 'src/components/heroCarousel.vue';
import templateHero from 'src/components/templateHero.vue';
</script>

<style lang="scss" scoped></style>
