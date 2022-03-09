<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-icon x-large class="icon-badge white--text">mdi-file-find</v-icon>
        <h4>Selecciona los reportes de grabaciones</h4>
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
    name: 'ReportSelector',

    data: () => ({
      //
    }),
  }
</script>
