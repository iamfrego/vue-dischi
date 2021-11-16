<template>
  <div class="selector">
    <label>Choose a genre</label>
    <select name="genre" id="" class="mx-3">
      <option value="">Rock</option>
      <option value="">Pop</option>
      <option value="">Jazz</option>
      <option value="">Metal</option>
    </select>
  </div>
</template>

<script>
export default {};
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