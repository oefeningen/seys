<template>
  <div class="about_inner" pa-5>
    <!-- <div class="left">
      <div class="image">
        <img src="/portfolio/sociale_pervijze/01.jpg" alt="placeholder" />
        <div
          class="main"
          v-scroll-reveal="{ delay: 20 }"
          :style="{ backgroundImage: 'url(' + aboutImg + ')' }"
        ></div>
      </div>
    </div> -->

    <div class="right">
      <div class="shane_tm_title">
        <span v-scroll-reveal="{ delay: 20 }">Over ons</span>
        <h3 v-scroll-reveal="{ delay: 40 }">Architecten Seys</h3>
      </div>
      <div class="text" v-scroll-reveal="{ delay: 60 }">
        <p>
          Architectenbureay Seys is een gerenommeerd architectenbureau in de
          westhoek dat al meer dan 50 jaar actief is in de branche. <br />Ons
          bureau heeft een rijke geschiedenis en heeft gedurende de jaren een
          sterke reputatie opgebouwd op het gebied van architectuur, design en
          vakmanschap. <br />Met vijf decennia aan ervaring streven we ernaar om
          tijdloze ontwerpen te creëren die zowel functioneel als esthetisch
          zijn. <br />Ons team van ervaren architecten en ontwerpers heeft
          expertise in diverse architecturale stijlen en disciplines, variërend
          van klassiek tot modern en alles daartussenin. Wij begrijpen dat elk
          project uniek is en zijn eigen uitdagingen met zich meebrengt. We
          luisteren aandachtig naar de wensen en behoeften van onze klanten en
          streven ernaar om ontwerpen te leveren die naadloos aansluiten bij hun
          visie. Of het nu gaat om de bouw van luxe villa's, grootschalige
          complexen of openbare gebouwen, we leveren hoogwaardige ontwerpen die
          zowel esthetisch indrukwekkend als functioneel zijn. <br />Ons bureau
          heeft door de jaren heen een uitgebreid netwerk van professionals
          opgebouwd, waaronder bouwexperts, ingenieurs en aannemers. We werken
          nauw met hen samen om ervoor te zorgen dat elk project voldoet aan de
          hoogste normen van kwaliteit en vakmanschap. <br />Bij
          Architectenbureay Seys geloven we in het behoud van een duurzame
          erfenis. <br />We streven ernaar om ontwerpen te creëren die niet
          alleen voldoen aan de huidige behoeften, maar ook rekening houden met
          toekomstige generaties en duurzame bouwpraktijken integreren.
          <br />Als je op zoek bent naar een ervaren architectenbureau met een
          rijke geschiedenis, zijn we de perfecte keuze.<br />Neem contact met
          ons op om te bespreken hoe we onze jarenlange expertise kunnen
          inzetten om jouw architecturale visie tot leven te brengen.
        </p>
      </div>
      <div class="shane_tm_button" v-scroll-reveal="{ delay: 80 }">
        <a :href="cv" download> Download CV </a>
      </div>
    </div>
    <!-- End right -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      // aboutImg: require("../../assets/img/about/1.jpg"),
      // cv: require("../../assets/img/resume/resume.jpg"),
      imagePath: '/src/assets/slide1.jpg',
      cv: '/src/assets/slide1.jpg',
      aboutImg: '/src/assets/slide1.jpg',
    };
  },
  mounted() {
    this.cv = url('/src/assets/slide1.jpg');
    this.aboutImg = url('/src/assets/slide1.jpg');
  },
};
</script>
