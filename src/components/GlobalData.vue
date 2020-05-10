<template>
  <div v-if="globalData">
    <h3>{{ globalData.displayName }}</h3>
    <p>{{ globalData.totalConfirmed }} infectados</p>
    <p>{{ globalData.totalDeaths }} mortes</p>
    <p>{{ globalData.totalRecovered }} recuperados</p>
  </div>
</template>

<script>
export default {
  props: {
    globalData: {
      required: true,
      type: Object,
    },
  },
};
</script>

<style></style>
