<template>
  <div>
    <app-stock v-for="stock in stocks" :stock="stock"></app-stock>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import Stock from "./Stock.vue";

export default {
  computed: {
    ...mapGetters({
      stocks: "stockPortfolio" // portfolio data
    })
  },
  components: {
    appStock: Stock
  }
};
</script>