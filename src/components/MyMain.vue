<template>
    <main>
      <MyFilter @selectEvent="getGenre"/>
      <SongsContainer :selectOption="filteredSongsList"/>
    </main>
</template>

<script>
import SongsContainer from './SongsContainer.vue'
import MyFilter from './MyFilter.vue';

export default {
  name: 'MyMain',
  components: {
    SongsContainer,
    MyFilter
  },
  data() {
    return {
        SongsList: [],
        selectGenre: "",
        selectOption: "",
    }
  },
//   computed: {
//     filteredSongsList() {
//       if (this.selectOption === "Tutti") {
//         return this.SongsList;
//       }

//       return this.SongsList.filter((item) => {
//         return item.genre.includes(this.selectOption);
//       })
//     }
//   },
  methods: {
    getMusic() {
      axios
      .get(this.apiUrl)
      .then((result) => {
        this.SongsList = result.data.response;
      })
    },
    getGenre(genre) {
      this.selectOption = genre;
    }
  }
}
</script>

<style scoped lang="scss">
main {
  background-color: #1e2d3b;
}
</style>