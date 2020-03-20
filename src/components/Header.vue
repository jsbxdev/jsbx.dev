<template>
  <header
    class="header flex justify-between items-center h-20 p-5 mt-0 w-full max-w-screen-lg bg-white"
  >
    <Logo></Logo>
    <nav class="">
      <g-link class="nav__link" to="/about/">sobre</g-link>
    </nav>
  </header>
</template>

<script>
import Logo from "~/components/Logo.vue";
export default {
  components: {
    Logo
  }
};
</script>

<style>
.header {
  border-bottom: solid 1px #dddddd;
}
</style>