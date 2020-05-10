<template>
  <div v-if="areas" class="flex flex-col">
    <area-list-item
      v-for="(area, index) in areas"
      :key="area.index"
      :areaData="area"
    ></area-list-item>
  </div>
</template>

<script>
import AreaListItem from "~/components/AreaListItem.vue";
export default {
  components: {
    AreaListItem,
  },
  props: {
    areas: {
      required: true,
      type: Array,
    },
  },
};
</script>

<style></style>
