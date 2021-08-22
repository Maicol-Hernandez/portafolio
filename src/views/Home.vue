<template>
  <v-container>
    <portafolio />
    <footer-portafolio />
  </v-container>
</template>

<script>
import FooterPortafolio from "../components/FooterPortafolio.vue";
import Portafolio from "../components/portafolio.vue";

export default {
  name: "Home",

  components: {
    Portafolio,
    FooterPortafolio,
  },
};
</script>
