<template>
  <div class="row row-cols-6">
    <div class="col" v-for="music in musics" :key="music.title">
      <div class="music my-4">
        <img :src="music.poster" :alt="music.title" class="img-fluid" />
        <p class="title text-center text-white">{{ music.title }}</p>
        <p class="author text-center">{{ music.author }}</p>
        <p class="years text-center">{{ music.year }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      musics: [],
      API_URL: "https://flynn.boolean.careers/exercises/api/array/music",
    };
  },

  mounted() {
    axios.get(this.API_URL).then((r) => {
      console.log(r.data.response);
      this.musics = r.data.response;
    });
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.row {
  overflow-x: hidden;
}

.music {
  background-color: $secondary;
  height: 350px;

  img {
  }
}
</style>