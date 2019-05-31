<template>
  <v-container>
    <v-layout>
      <draggable v-model="foodList">
      <v-card :color="food.color" class="food-item" :key="food.name" v-for="food in foodList">
        {{food.name}}
        <v-select :items="qtySelect" v-model="food.qty" />
        <v-btn flat @click="food.menu = true"><v-icon>palette</v-icon></v-btn>
        <v-layout v-if="food.menu">
          <v-flex><v-btn @click="food.color = '#4d5057'" color="#4d5057"></v-btn></v-flex>
          <v-flex><v-btn @click.native="food.color = '#c33c54'" color="#c33c54"></v-btn></v-flex>
          <v-flex><v-btn @click="food.color = '#4da167'" color="#4da167"></v-btn></v-flex>

          <v-flex><v-btn @click="food.color = '#c6ca53'" color="#c6ca53"></v-btn></v-flex>
          <v-flex><v-btn @click="food.color = '#058ed9'" color="#058ed9"></v-btn></v-flex>

        </v-layout>
      </v-card>
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
        {name: 'Apple', color: 'green', qty: 3, menu: false, color: '#4d5057' },
        {name: 'Orange', color: 'green', qty: 2, menu: false, color: '#4d5057'},
        {name: 'Lettuce', color: 'green', qty:1, menu: false, color: '#4d5057'},
        {name: 'Milk', color: 'yellow', qty: 1, menu: false, color: '#4d5057'},
      ],
      qtySelect: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
    }),
    methods: {
      setFoodColor(food,color){
        console.o
      }
    }
  }
</script>

<style>
.food-item:hover{
  cursor:move;
}
.food-item{
  color:white;
  margin: .5rem;
}
</style>


--TO DO--
()
---------