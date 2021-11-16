<template>
  <div class="header d-flex justify-content-between">
    <img src="../assets/image/Spotify-Logo.svg" alt="Logo" />
    <Selector />
  </div>
</template>

<script>
import Selector from "./Selector.vue";
export default {
  components: { Selector },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.header {
  background-color: $secondary;
  img {
    padding: 1rem 2rem;
    height: 75px;
  }
}
</style>