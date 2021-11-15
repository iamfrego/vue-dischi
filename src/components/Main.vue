<template>
  <div class="main">
    <CardList />
  </div>
</template>


<script>
import CardList from "./CardList.vue";
export default {
  components: {
    CardList,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.main {
  height: calc(100vh - 75px);
  background-color: $primary;
  overflow-x: hidden;
  overflow-y: hidden;
}
</style>