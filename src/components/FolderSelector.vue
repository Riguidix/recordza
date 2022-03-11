<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-icon x-large class="icon-badge white--text">mdi-music-circle</v-icon>
        <h4>Selecciona las grabaciones</h4>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="12">
        <v-file-input
          counter
          multiple
          show-size
          truncate-length="1"
        ></v-file-input>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'FolderSelector',

    data: () => ({
      //
    }),
  }
</script>