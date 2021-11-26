<template>
  <section id="SongsContainer">
    <SongsCard v-for="Song, i in SongsList" :key="i" :details="Song"/>
  </section>
</template>

<script>
import axios from "axios";
import SongsCard from './SongsCard.vue';

export default {
  name: 'SongsContainer',
  components: {
    SongsCard
  },
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      SongsList: [],
    }
  },
  created() {
    this.getMusic();
  },
  methods: {
    getMusic() {
      axios
      .get(this.apiUrl)
      .then((result) => {
        this.SongsList = result.data.response;
      })
    }
  }
}
</script>

<style scoped lang="scss">
#SongsContainer {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 100px 0;
}
</style>