<template>
  <v-app>
    <v-container fluid>
      <v-card width="100%" tile>
        <v-card-title> </v-card-title>
      </v-card>
    </v-container>

    <v-app-bar app color="#00b0c7" prominent dark>
      <v-card class="mt-1" tile color="#00b0c7" flat>
        <v-row justify="center" align="center">
          <v-col cols="12" sm="12">
            <v-card-title>
              <span>Maicol Fernando Hernandez Peralta</span>
            </v-card-title>
            <v-card-subtitle>
              <span> Desarrollador Frontend </span>
            </v-card-subtitle>
          </v-col>
        </v-row>
      </v-card>
      <v-spacer></v-spacer>

      <div class="mt-5">
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
  }),
};
</script>
