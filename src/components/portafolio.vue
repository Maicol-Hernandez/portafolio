<template>
  <v-container fluid class="text-center">
    
    <p
      class="text-h4 justify-center text-uppercase font-weigth-bold white--text"
    >
      <strong>Portafolio</strong>
    </p>
    <hr class="mb-5" />
    <!-- 
        <v-hover>
          <template v-slot:default="{ hover }">
            <v-card class="mx-auto" max-width="344">
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/forest-art.jpg"
              ></v-img>

              <v-card-text>
                <h2 class="text-h6 primary--text">Magento Forests</h2>
                Travel to the best outdoor experience on planet Earth. A
                vacation you will never forget!
              </v-card-text>

              <v-card-title>
                <v-rating
                  :value="4"
                  dense
                  color="orange"
                  background-color="orange"
                  hover
                  class="mr-2"
                ></v-rating>
                <span class="primary--text text-subtitle-2">64 Reviews</span>
              </v-card-title>

              <v-fade-transition>
                <v-overlay v-if="hover" absolute color="#036358">
                  <v-btn>See more info</v-btn>
                </v-overlay>
              </v-fade-transition>
            </v-card>
          </template>
        </v-hover> -->
    <div v-for="card in 4" :key="card">
      <v-hover>
        <template v-slot:default="{ hover }">
          <v-card class="mx-auto mb-10" height="260" max-width="500" tile>
            <v-img height="100%" :src="user.urlImg">
              <v-row align="end" class="fill-height">
                <v-col cols="12" align-self="start" class="pa-0">
                  <v-avatar
                    class="pt-4  profile"
                    dark
                    width="100%"
                    size="199"
                    tile
                  >
                    <v-img  max-width="90%" max-height="90%"  :src="user.foto"></v-img>
                  </v-avatar>
                </v-col>
                <v-card-text>
                  <v-col class="py-0">
                    <v-list-item>
                      <v-list-item-content>
                        <v-list-item-title class="text-h6">
                          {{ user.nombreCompleto }}
                        </v-list-item-title>
                        <v-list-item-subtitle>
                          {{ user.profesion }}
                        </v-list-item-subtitle>
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-card-text>
              </v-row>
            </v-img>

            <v-fade-transition>
              <v-overlay v-if="hover" absolute color="#036358">
                <v-btn block>ver mas</v-btn>
              </v-overlay>
            </v-fade-transition>
          </v-card>
        </template>
      </v-hover>
    </div>

  </v-container>
</template>

<script>
export default {
  name: "portafolio",
  data: () => ({
    user: {
      foto: require("../assets/img-card.jpg"),
      nombreCompleto: "Maicol Fernando Hernandez Peralta",
      urlImg: require("@/assets/img_programming.jpg"),
      profesion: "Tecnologo/ Analisis y Desarrollo de Sistemas de Informacion",
    },
  }),
};
</script>
