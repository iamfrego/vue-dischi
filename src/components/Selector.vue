<template>
  <div class="selector text-center">
    <label for="select">Choose a genre</label>
    <select
      id="select"
      class="mx-3"
      v-model="genreSelect"
      @change="$emit('filtered-genre', genreSelect)"
    >
      <option value="All">All</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      genreSelect: "",
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.selector {
  line-height: 75px;
  label {
    color: $third;
  }
}
</style>