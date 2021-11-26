<template>
  <section id="SongsContainer">
    <SongsCard v-for="Song, i in Songs" :key="i" :details="Song"/>
  </section>
</template>

<script>
import SongsCard from './SongsCard.vue';

export default {
  name: 'SongsContainer',
  components: {
    SongsCard
  }
}
</script>

<style scoped lang="scss">

</style>