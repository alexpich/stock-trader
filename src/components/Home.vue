<template>
  <div>
    <h1>View or Trade Your Portfolio</h1>
    <h6>Save & Load Data</h6>
    <h6>End Day</h6>
    <hr />
    <p>Funds: {{ funds | currency }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    funds() {
      return this.$store.getters.funds;
    }
  }
};
</script>