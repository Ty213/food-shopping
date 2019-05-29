<template>
  <v-container>
    <v-layout>
      <draggable v-model="foodList">
      <v-flex :key="food.name" v-for="food in foodList">
        {{food.name}}
      </v-flex>
      </draggable>
    </v-layout>
  </v-container>
</template>

<script>
import draggable from 'vuedraggable'
  export default {
    components: {
      draggable
    },
    data: () => ({
      foodList: [
        {name: 'Apple', color: 'green', qty: 3},
        {name: 'Orange', color: 'green', qty: 2},
        {name: 'Lettuce', color: 'green', qty:1},
        {name: 'Milk', color: 'yellow', qty: 1},
      ]
    })
  }
</script>

<style>

</style>

--TO DO--
()
---------