<template>
  <v-container fluid>
    <v-parallax dark height="100%" class="fondo-img" src="@/assets/img_fondo.jpg">
      <!-- src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg" -->
      <!-- src="@/assets/img_fondo.jpg" -->
      <portafolio />
      <skillset />
      <experiencia />
      <footer-portafolio />
    </v-parallax>
  </v-container>
</template>

<script>
import Experiencia from "../components/Experiencia.vue";
import FooterPortafolio from "../components/FooterPortafolio.vue";
import Portafolio from "../components/portafolio.vue";
import Skillset from "../components/Skillset.vue";

export default {
  name: "Home",

  components: {
    Portafolio,
    FooterPortafolio,
    Skillset,
    Experiencia,
  },
};
</script>

<style>
/* .fondo-img {
  background: url("../assets/img_fondo.jpg") no-repeat center center fixed;
} */
</style>
