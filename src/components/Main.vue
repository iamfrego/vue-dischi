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
  background-color: $primary;
}
</style>