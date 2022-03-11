<template>
  <v-container>
    <v-row>
      <v-col cols="6">
        <h4 class="text-center">Columnas del Reporte</h4>
        <v-divider></v-divider>

        <draggable class="list-group" :list="columns" group="columns"  v-model="columns" @change="log" handle=".handle">
          <transition-group name="list">
            <div class="handle todo" v-for="(item, index) in columns" :key="item.name">
              <v-icon>mdi-drag</v-icon>
              <span>{{item.name}}</span>
            </div>
          </transition-group>
        </draggable>
      </v-col>

      <v-col cols="6">
        <h4 class="text-center">Nombre de los Archivos</h4>
        <v-divider></v-divider>

        <draggable class="list-group" :list="names" group="columns" v-model="name" @change="log" handle=".handle">
          <transition-group name="list">
            <div class="handle todo" v-for="(item, index) in names" :key="item.name">
              <v-icon>mdi-drag</v-icon>
              <span>{{item.name}}</span>
            </div>
          </transition-group>
        </draggable>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import draggable from 'vuedraggable';

export default {
  name: 'DraggableLists',

  components: {
    draggable
  },

  data: () => ({
    columns: [],
    names: [
      { name: "Item 4", id: 4 },
      { name: "Item 5", id: 5 },
    ],
  }),
  methods: {
    log: function(evt) {      
      window.console.log(evt);
    }
  }
}
</script>

<style scoped>
  .container, draggable {
    height: 320px;
    overflow: hidden;
    padding: 20px;
  }

  .col {
    height: 320px;
    overflow-y: scroll;
  }

  .todo {
    border-radius: 5px;
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.1);
    margin-bottom: 2px;
    padding: 10px;
    user-select: none;
  }

  .list-group {
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    min-height: 20px;
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.1);
  }

  .list-move {
    transition: .5s;
  }

  .handle {
    cursor: move;
  }
</style>