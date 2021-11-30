<template>
    <main>
      <MyFilter @selectEvent="getGenre"/>
      <SongsContainer :selectOption="selectOption"/>
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
  methods: {
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