<template>
  <v-footer dark padless>
    <v-card tile flat class="warning lighten-1 white--text text-center">
      <v-card-title class="text-uppercase justify-center">
        <strong>Contactame</strong>
      </v-card-title>
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="white--text pt-0">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aut, eum
        magnam corrupti alias animi eaque maiores saepe corporis ipsa qui
        quibusdam, quasi optio omnis exercitationem aperiam, natus ratione
        commodi officiis! Lorem ipsum dolor sit amet, consectetur adipisicing
        elit. Rem, maxime modi? Molestias, magnam fugiat ipsum distinctio vel
        architecto pariatur. Deserunt ab veritatis minima magni, earum atque
        tenetur nulla animi voluptatibus.
      </v-card-text>
      <!-- </v-card> -->
      <v-divider></v-divider>
      <v-card-text class="py-2 white--text" id="footer">
        Desarrollado y diseñado por Michael Fernando Hernandez Peralta. &copy;{{
          new Date().getFullYear()
        }}. Todos los derechos reservados
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "FooterPortafolio",
  data: () => ({
    icons: ["mdi-github", "mdi-linkedin", "mdi-facebook"],
  }),
};
</script>

<style>
#footer {
  font: caption;
  letter-spacing: 0.0333333333em;
  font-weight: 400;
  /* background-color: #424242; */
  font-size: 0.75rem;
}
</style>