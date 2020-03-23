<template>
  <div class="row">
    <app-stock v-for="(stock, i) in stocks" v-bind:key="i" :stock="stock"></app-stock>
  </div>
</template>

<script>
import Stock from "./Stock.vue";

export default {
  data() {
    return {
      stocks: [
        { id: 1, name: "AMD", price: 45 },
        { id: 2, name: "BLUE", price: 48 },
        { id: 3, name: "SPCE", price: 12 },
        { id: 4, name: "UBER", price: 22 }
      ]
    };
  },
  components: {
    appStock: Stock
  }
};
</script>