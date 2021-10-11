<template>
  <v-container fluid>
    <!-- <v-card  width="100%" class="justify-center" > -->
    <!-- <v-row class="mb-1" align="center" justify="center"> -->
    <!-- <v-col cols="12"  lg="12" sm="12" md="12"> -->
    <v-card-title
      class="white--text font-weigth-bold text-uppercase text-h4 justify-center"
    >
      <strong>Experiencia</strong>
    </v-card-title>
    <hr class="mb-5" />
    <v-card-text>
      <v-row dense justify="center">
        <v-col cols="12" lg="7">
          <v-row dense id="boder-content">
            <v-col
              cols="12"
              lg="6"
              v-for="n of 6"
              :key="n"
              class="d-flex child-flex"
            >
              <v-hover v-slot="{ hover }" close-delay="200" open-delay="200">
                <v-card
                  id="boder"
                  shaped
                  :elevation="hover ? 12 : 2"
                  :class="{ 'on-hover': hover }"
                >
                  <v-img
                    contain
                    :src="`https://picsum.photos/500/300?image=${n + 160 + 9}`"
                    :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                    aspect-ratio="2"
                    max-height="200"
                    class="grey darken-4"
                  >
                    <template v-slot:placeholder>
                      <v-row
                        dense
                        class="fill-height ma-0"
                        justify="center"
                        align="center"
                      >
                        <v-progress-circular
                          color="grey lighten-5"
                          indeterminate
                        ></v-progress-circular>
                      </v-row>
                    </template>
                  </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <!-- 
      <v-row justify="center" class="red">
        <v-col cols="12" lg="8">
          <v-row justify="center" class="info d-flex">
            <v-col
              cols="12"
              lg="4"
              v-for="item of 5"
              :key="item"
              class="mx-2 d-flex child-flex success"
            >
              <v-card dark shaped width="350" id="boder">
                <v-img
                  contain
                  height="200"
                  width="430"
                  src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ></v-img>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row> -->
    </v-card-text>
  </v-container>
</template>

<script>
export default {
  name: "Experiencia",
  data: () => ({}),
};
</script>
<style scoped>
#boder {
  border: 4px solid #00b0c7;
}
</style>