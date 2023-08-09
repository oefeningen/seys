<template>
  <div>
    <FsLightbox :toggler="toggler" :sources="image.slides" />
    <q-img
      ma-10
      :src="image.thumb"
      spinner-color="white"
      style="height: 333px; max-width: 350px; width: 333px"
      @mouseover="showCaption = true"
      @mouseleave="showCaption = false"
      @click="toggler = !toggler"
    >
      <div
        class="caption absolute-bottom text-subtitle1 text-center"
        :class="{ 'slide-up': showCaption }"
      >
        {{ image.portfolioName }}
      </div>
    </q-img>
  </div>
</template>

<style>
.caption {
  transition: transform 0.3s ease;
  transform: translateY(100%);
}

.slide-up {
  transform: translateY(0);
}
</style>

<script>
import FsLightbox from 'fslightbox-vue/v3';
export default {
  data() {
    return {
      showCaption: false,
      toggler: false,
    };
  },
  components: {
    FsLightbox,
  },
  props: {
    image: {
      type: Object,
      required: true,
    },
  },
};
</script>
