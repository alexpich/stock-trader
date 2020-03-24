<template>
  <div class="row">
    <app-stock v-for="(stock, i) in stocks" v-bind:key="i" :stock="stock"></app-stock>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import Stock from "./Stock.vue";

export default {
  components: {
    appStock: Stock
  },
  computed: {
    ...mapGetters({
      stocks: "stockPortfolio"
    })
  }
};
</script>