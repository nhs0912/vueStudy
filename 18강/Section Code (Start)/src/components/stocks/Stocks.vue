<template>
  <div>
    <app-stock
      v-for="stock in stocks"
      :key="stock.id"
      :stock="stock"
    ></app-stock>
  </div>
</template>

<script>
import Stock from "./Stock.vue";

export default {
  // data(){
  //     return {
  //         stocks: [
  // { id: 1, name: 'BMW', price: 50},
  // { id: 2, name: 'Google', price: 150},
  // { id: 3, name: 'Apple', price: 10},
  // { id: 4, name: 'Samsung', price: 310},
  // { id: 5, name: 'LG', price: 210}
  //         ]
  //     }
  // },
  components: {
    appStock: Stock,
  },
  computed : {
      stocks(){
          return this.$store.getters.stocks;
      }
  }
};
</script>
