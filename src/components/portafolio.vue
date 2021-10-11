<template>
  <v-container fluid class="text-center">
    <!-- <v-card dark flat tile class="text-center" > -->
    <v-row justify="start" align-content="space-between" class="mb-1">
      <v-col cols="12">
        <v-card-title
          class="
            text-h4
            justify-center
            text-uppercase
            font-weigth-bold
            white--text
          "
        >
          <strong>Portafolio</strong>
        </v-card-title>
        <hr class="mb-5" />
        <!--  -->
        <v-card
          v-for="card in 4"
          :key="card"
          class="mx-auto mb-10"
          height="260"
          max-width="500"
          tile
        >
          <v-img height="100%" :src="user.urlImg">
            <v-row align="end" class="fill-height">
              <v-col cols="12" align-self="start" class="pa-0">
                <v-avatar class="profile" color="grey" size="164" tile>
                  <v-img :src="user.foto"></v-img>
                </v-avatar>
              </v-col>
              <v-col class="py-0">
                <v-list-item color="rgba(0, 0, 0, .4)" dark>
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
            </v-row>
          </v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "portafolio",
  data: () => ({
    user: {
      foto: require("@/assets/avatar_maicol.jpeg"),
      nombreCompleto: "Maicol Fernando Hernandez Peralta",
      urlImg: require("@/assets/img_programming.jpg"),
      profesion: "Tecnologo/ Analisis y Desarrollo de Sistemas de Informacion",
    },
  }),
};
</script>
