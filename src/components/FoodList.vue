<template>
  <v-container>
    <v-layout>
      <draggable v-model="foodList">
      <v-flex class="food-item" style="border:1px solid green;" :key="food.name" v-for="food in foodList">
        {{food.name}}
        <v-select :items="qtySelect" v-model="food.qty" />
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
      ],
      qtySelect: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
    })
  }
</script>

<style>
.food-item:hover{
  cursor:move;
}
</style>


--TO DO--
()
---------