<template>
  <Layout>
    <div class="hero p-3">
      <covid-monitor v-if="fetchedData" :data="fetchedData"></covid-monitor>
    </div>
  </Layout>
</template>

<script>
import axios from "axios";
import CovidMonitor from "~/components/CovidMonitor.vue";
export default {
  metaInfo: {
    title: "JSBX Consulting",
  },
  components: {
    CovidMonitor,
  },
  data() {
    return {
      fetchedData: false,
      apiURL:
        "https://www.bing.com/covid/data?fbclid=IwAR0H3Pf41agrGI7BFRj-YpSujrSnpXt7VRQ-4geg9BtsxCZPZGCQDFD4X8Y&IG=5478213FEBF343D89A5F43FAC6815CCD",
    };
  },
  created() {
    axios.get(this.apiURL).then(response => {
      console.log(response.data);
      this.fetchedData = response.data;
    });
  },
};
</script>

<style>
.hero {
  background-image: radial-gradient(
    70% 70% at 50% 100%,
    rgb(232, 232, 232) 0%,
    rgb(250, 250, 250) 100%
  );
  height: 800px;
}
</style>
