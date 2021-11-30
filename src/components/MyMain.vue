<template>
    <main>
      <MyFilter @selectEvent="getGenre"/>
      <SongsContainer/>
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
      selectGenre: "",
      selectOption: "",
    }
  },
  computed: {
    filteredSongsList() {
      if (this.selectOption === "Tutti") {
        return this.SongsList;
      }

      return this.SongsList.filter((item) => {
        return item.genre.includes(this.selectOption);
      })
    }
  },
  methods: {
    getGenre(genre) {
      this.selectOption = genre;
      console.log(genre);
    }
  }
}
</script>

<style scoped lang="scss">
main {
  background-color: #1e2d3b;
}
</style>