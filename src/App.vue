<template>
  <v-app>
    <v-app-bar app height="90" elevation="20" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-card height="98" class="mb-2" dark tile flat>
        <v-row no-gutters dense>
          <v-col cols="12" sm="12">
            <v-card-title class="">
              <span>Maicol Hernandez Peralta</span>
            </v-card-title>
            <v-card-subtitle>
              <span>Desarrollador Frontend</span>
            </v-card-subtitle>
          </v-col>
        </v-row>
      </v-card>
      <v-spacer></v-spacer>
      <v-btn icon class="mr-3" @click="modoOscuro" v-model="darkMode">
        <v-icon>mdi-theme-light-dark</v-icon>
      </v-btn>
      <div class="mb-1">
        <v-menu bottom rounded max-width="200px" offset-y>
          <template v-slot:activator="{ on }">
            <v-btn icon x-large v-on="on">
              <v-avatar size="70">
                <v-img :src="user.foto"></v-img>
              </v-avatar>
            </v-btn>
          </template>
          <v-card elevation="1">
            <v-list-item-content class="justify-center">
              <div class="mx-auto text-center">
                <v-avatar>
                  <v-img :src="user.foto"></v-img>
                </v-avatar>

                <h3>{{ user.nombreCompleto }}</h3>
                <p class="text-caption mt-1">{{ user.email }}</p>

                <v-divider class="my-3"></v-divider>
                <v-btn depressed rounded text> Contactarme </v-btn>
                <v-divider class="my-3"></v-divider>
                <v-btn depressed rounded text> Email </v-btn>
              </div>
            </v-list-item-content>
          </v-card>
        </v-menu>
      </div>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    user: {
      foto: require("@/assets/avatar_maicol.jpeg"),
      email: "maicolhernandez420@gmail.com",
      nombreCompleto: "Maicol Fernando Hernandez Peralta",
      urlImg: require("@/assets/img_programming.jpg"),
      profesion: "Tecnologo/ Analisis y Desarrollo de Sistemas de Informacion",
    },
    darkMode: "",
  }),
  watch: {
    darkMode: function (val) {
      console.log(val);
    },
  },
  methods: {
    modoOscuro: function (val) {
      console.log(val);
      return "red";
    },
  },
};
</script>