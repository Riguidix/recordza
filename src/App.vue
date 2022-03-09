<template>
  <v-app>
    <v-main>
      <MainPage />
    </v-main>

    <v-footer padless class="black white--text lighten-1 text-center">
      <v-container>
        <v-row class="text-center">
          <v-col cols="6">
            <v-icon color="primary">mdi-code-tags</v-icon>
            with
            <v-icon color="error">mdi-heart</v-icon>
          </v-col>

          <v-col cols="6">
            0.0.1
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
import MainPage from './pages/MainPage';

export default {
  name: 'App',

  components: {
    MainPage,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
  .v-main__wrap {
    padding: 20px;
  }
</style>
