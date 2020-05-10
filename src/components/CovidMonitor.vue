<template>
  <div v-if="data">
    <h2>COVID-19 Monitor</h2>
    <global-data :globalData="data"></global-data>
    <area-list :areas="data.areas"></area-list>
  </div>
</template>

<script>
import AreaList from "~/components/AreaList.vue";
import GlobalData from "~/components/GlobalData.vue";
export default {
  components: {
    AreaList,
    GlobalData,
  },
  props: {
    data: {
      required: true,
      type: Object,
    },
  },
};
</script>

<style></style>
