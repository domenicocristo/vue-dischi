<template>
  <section id="SongsContainer">
    <MyFilter @select="getGenre"/>
    <div v-if="SongsList.length === 10">
      <SongsCard v-for="Song, i in SongsList" :key="i" :details="Song"/>
    </div>
    <div v-else>
      <h1>Loading...</h1>
    </div>
  </section>
</template>

<script>
import axios from "axios";
import SongsCard from './SongsCard.vue';
import MyFilter from './MyFilter.vue';

export default {
  name: 'SongsContainer',
  components: {
    SongsCard,
    MyFilter
  },
  data() {
    return {
      apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      SongsList: [],
      selectGenre: "",
      selectOption: "",

    }
  },
  created() {
    this.getMusic();
  },
  computed: {
    filteredSongsList() {
      if (this.selectOption === "") {
        return this.SongsList;
      }

      return this.SongsList.filter((item) => {
        return item.genre.includes(this.selectOption);
      })
    }
  },
  methods: {
    getMusic() {
      axios
      .get(this.apiUrl)
      .then((result) => {
        this.SongsList = result.data.response;
      })
    }
  },
  getGenre(genre) {
    this.selectOption = genre;
  }
}
</script>

<style scoped lang="scss">
#SongsContainer {
  padding: 100px 0;
  div {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
}
</style>