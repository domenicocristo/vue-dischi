<template>
  <section id="SongsCard">
      <img src="details.poster" alt="poster">
      <h3>{{details.title}}</h3>
  </section>
</template>

<script>
export default {
  name: 'SongsCard',
  props: {
      details: Object
  }
}
</script>

<style scoped lang="scss">

</style>