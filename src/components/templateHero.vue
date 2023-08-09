<template>
  <div class="shane_tm_hero" id="home" data-style="one">
    <div class="background">
      <div
        class="image transition"
        :style="{
          backgroundImage: bg,
        }"
      ></div>
    </div>
    <!-- End .background -->

    <div class="container">
      <div class="content">
        <transition-group
          transition-show="jump-down"
          enter-active-class="animated fadeIn"
          leave-active-class="animated fadeOut"
        >
          <div class="name_wrap2">
            <h3>
              <span>architecten</span> Seys<span class="overlay_effect2"></span>
            </h3>
          </div>
        </transition-group>
        <!-- End title -->

        <div class="job_wrap">
          <span class="job">
            architectenbureau Diksmuide
            <span class="overlay_effect2"></span>
          </span>
        </div>
        <!-- End designation -->
      </div>
      <!-- End content -->

      <div class="shane_tm_down loaded">
        <div class="line_wrapper">
          <div class="line"></div>
        </div>
      </div>
    </div>
    <!-- End .container -->
  </div>
</template>

<script>
// import inplantingImage /from '@/assets/inplanting.png';
export default {
  data() {
    return {
      // sliderHero: require('../../assets/img/slider/4.jpg'),
      // sliderHero: require('https://images.pexels.com/photos/937465/pexels-photo-937465.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1'),
      bg1: 'url(https://images.pexels.com/photos/937465/pexels-photo-937465.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)',
      imagePath: '/src/assets/inplanting.png',
      bg: null,
    };
  },
  mounted() {
    this.bg = `url(${this.imagePath})`;
    setInterval(() => {
      this.imagePath =
        this.imagePath === '/src/assets/inplanting.png'
          ? '/src/assets/slide1.jpg'
          : '/src/assets/inplanting.png';
      this.bg = `url(${this.imagePath})`;
    }, 10000);
  },
};
</script>

<style lang="scss" scoped>
.transition {
  transition: background-image 1s ease;
}
</style>
