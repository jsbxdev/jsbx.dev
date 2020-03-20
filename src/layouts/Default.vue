<template>
  <div class="bg-white h-screen flex flex-col items-center">
    <Header></Header>
    <div class="container">
      <slot />
    </div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Header from "~/components/Header.vue";
export default {
  components: {
    Header
  }
};
</script>

<style>
.body {
  font-family: "Roboto", sans-serif;
}
</style>
