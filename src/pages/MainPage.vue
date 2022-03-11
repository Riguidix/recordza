<template>
  <v-container class="inputs">
    <v-row>
      <v-col cols="6">
        <FolderSelector />
      </v-col>

      <v-divider vertical></v-divider>

      <v-col cols="6">
        <ReportSelector />
      </v-col>
    </v-row>

    <v-row>
      <v-divider></v-divider>
    </v-row>

    <v-row>
      <v-col cols="12">
        <DraggableLists />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import FolderSelector from '../components/FolderSelector';
import ReportSelector from '../components/ReportSelector';
import DraggableLists from '../components/DraggableLists';
import ProgressBar from '../components/ProgressBar';

export default {
  name: 'MainPage',

  components: {
    FolderSelector,
    ReportSelector,
    DraggableLists,
    ProgressBar
  },

  data: () => ({
    //
  }),
}
</script>

<style>
  hr {
    margin: 10px 0;
  }

  .icon-badge {
    position: absolute;
    padding: 10px;
    background-color: #000;
    color: #fff;
    border-radius: 50px;
    top: -50%;
  }

  .inputs .col > .container {
    border: 2px solid #000;
    border-radius: 15px;
    text-align: center;
  }
</style>
