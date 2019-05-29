<template>
  <v-app>
    <v-content>
      <FoodList/>
    </v-content>
  </v-app>
</template>

<script>
import FoodList from './components/FoodList'

export default {
  name: 'App',
  components: {
    FoodList
  },
  data () {
    return {
      //
    }
  }
}
</script>
