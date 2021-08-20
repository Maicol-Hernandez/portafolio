<template>
  <v-main>
    <v-container>
      <!--  -->
      <v-card class="mx-auto" height="206" max-width="434" tile>
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
    </v-container>
  </v-main>
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