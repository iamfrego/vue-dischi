<template>
  <div>
    <div class="row row-cols-6 justify-content-center pt-3 g-5" v-if="!loading">
      <div class="col" v-for="music in musics" :key="music.title">
        <div class="music mt-5">
          <div class="image d-flex justify-content-center pt-5">
            <img :src="music.poster" :alt="music.title" class="img-fluid" />
          </div>
          <p class="title text-center text-white text-uppercase">
            {{ music.title }}
          </p>
          <p class="author text-center">{{ music.author }}</p>
          <p class="years text-center">{{ music.year }}</p>
        </div>
      </div>
    </div>
    <div class="text-white" v-else>Loading...</div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      musics: [],
      API_URL: "https://flynn.boolean.careers/exercises/api/array/music",
      loading: true,
      error: "",
    };
  },

  mounted() {
    setTimeout(this.callAPI, 3000);
  },

  methods: {
    callAPI() {
      axios.get(this.API_URL).then((r) => {
        console.log(r.data.response);
        this.musics = r.data.response;
        this.loading = false;
      });
    },
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.music {
  background-color: $secondary;
  height: 100%;
  width: 75%;
  margin: auto;

  img {
    width: 50%;
  }

  p {
    color: gray;
  }

  .title {
    padding: 1rem;
    font-size: 1.5rem;
    font-weight: bolder;
  }
}
</style>