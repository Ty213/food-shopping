<template>
  <v-container>
    <v-layout>
      <v-flex :key="food.name" v-for="food in foodList">
        {{food.name}}
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
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
