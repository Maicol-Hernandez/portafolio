<template>
  <v-container fluid>
    <v-card dark flat tile class="text-center">
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
            <v-row dense>
              <v-col v-for="img in imgsExperiencia" :key="img.id">
                <v-avatar rounded size="90" class="color-avatar">
                  <v-img :src="img.foto"> </v-img>
                </v-avatar>
              </v-col>
            </v-row>
          </v-card-text>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "Skillset",
  data: () => ({
    imgsExperiencia: [
      {
        id: 1,
        nombre: "Angular",
        foto: require("@/assets/Angularjs.png"),
      },
      { id: 2, nombre: "CSS", foto: require("@/assets/CSS.png") },
      { is: 3, nombre: "Javascript", foto: require("@/assets/Javascript.png") },
      {
        id: 4,
        nombre: "Mysql Workbech",
        foto: require("@/assets/mysql_workbench.png"),
      },
      { id: 5, nombre: "Python", foto: require("@/assets/python.png") },
      { id: 6, nombre: "Vue2.js", foto: require("@/assets/vue2.png") },
      { id: 7, nombre: "Vuetify", foto: require("@/assets/vuetify.png") },
      { id: 8, nombre: "HTML", foto: require("@/assets/HTML.png") },
      { id: 9, nombre: "HTML", foto: require("@/assets/HTML.png") },
    ],
  }),
};
</script>