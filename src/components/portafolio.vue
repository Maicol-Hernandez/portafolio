<template>
  <v-container fluid>
    <v-card class="" flat tile width="100%">
      <v-row justify="start" align-content="space-between" class="mb-1">
        <v-col cols="12">
          <v-card-title
            class="
              text-h4
              justify-center
              text-uppercase
              font-weigth-bold
              blue-grey--text
              text--darken-4
            "
          >
            <strong> Portafolio </strong>
          </v-card-title>
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
      <!--  -->
      <v-row align="stretch" class="color-skills mb-1">
        <v-col cols="12" align-self="start" class="d-flext">
          <v-card-title
            class="
              white--text
              font-weigth-bold
              text-uppercase text-h4
              justify-center
            "
          >
            <strong>skillset</strong>
          </v-card-title>
          <v-card-text>
            <v-row>
              <v-col cols="2" v-for="img in imgsExperiencia" :key="img.nombre">
                <v-avatar rounded size="90" class="color-avatar" color=" ">
                  <v-img :src="img.foto"> </v-img>
                </v-avatar>
              </v-col>
            </v-row>
          </v-card-text>
        </v-col>
      </v-row>
      <!--  -->
      <v-row class="info" justify="start">
        <v-col cols="12" align-self="start" class="d-flext">
          <v-card-title class="text-uppercase justify-center">
            <strong>Experiencia</strong>
          </v-card-title>
        </v-col>
      </v-row>
      <!--  -->
    </v-card>

    <!--  -->
    <!-- <v-row justify="start" dense align="center" class="grey">
        <v-col cols="12">
          <v-card-title>
            <strong>Experiencia</strong>
          </v-card-title>
        </v-col>

      </v-row> -->

    <!--  -->
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
    imgsExperiencia: [
      {
        nombre: "Angular",
        foto: require("@/assets/Angularjs.png"),
      },
      { nombre: "CSS", foto: require("@/assets/CSS.png") },
      { nombre: "Javascript", foto: require("@/assets/Javascript.png") },
      {
        nombre: "Mysql Workbech",
        foto: require("@/assets/mysql_workbench.png"),
      },
      { nombre: "Python", foto: require("@/assets/python.png") },
      { nombre: "Vue2.js", foto: require("@/assets/vue2.png") },
      { nombre: "Vuetify", foto: require("@/assets/vuetify.png") },
      { nombre: "HTML", foto: require("@/assets/HTML.png") },
    ],
  }),
};
</script>

<style>
.color-avatar {
background: white;
/* background: -webkit-linear-gradient(to right, #f09819, #ff512f);
  background: linear-gradient(to right, #f09819, #ff512f); */
}
.color-skills {
  background: #00b0c7;
}
</style>