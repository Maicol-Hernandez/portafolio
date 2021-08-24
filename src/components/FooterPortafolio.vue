<template>
  <v-footer dark padless>
    <v-card tile flat class="indigo lighten-1 white--text text-center">
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
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum minus
        mollitia magnam vel hic quae exercitationem odit placeat. Earum cumque
        eum pariatur officiis nobis cum harum a eveniet reiciendis mollitia.
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Error, enim
        iste beatae officiis reprehenderit optio est adipisci culpa. Saepe quam
        a explicabo quod dignissimos tempora ut nulla sequi magni repudiandae.
        <v-form>
          <v-container fluid>
            <v-row no-gutters justify="center">
              <v-col align-self="end" cols="12" md="5" lg="4">
                <v-text-field label="Nombres"></v-text-field>
                <v-text-field class="" label="Apellidos"></v-text-field>
                <v-text-field label="E-mail"> </v-text-field>
              </v-col>
              <v-col cols="12" md="5" lg="5" align-self="end">
                <v-row
                  class="mb-1"
                  style="height: 178px"
                  dense
                  justify-lg="center"
                  justify-sm="center"
                  justify-md="center"
                >
                  <v-col cols="12" class="ml-2" md="10" sm="12" lg="10">
                    <v-textarea label="Nota"></v-textarea>
                    <v-row
                      justify-lg="end"
                      justify-sm="center"
                      justify-md="end"
                    >
                      <v-btn> Enviar </v-btn>
                    </v-row>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-form>
      </v-card-text>

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