<template>
  <section id="SongsCard">
      <img :src="details.poster" alt="poster">
      <h3>{{details.title}}</h3>
      <div>{{details.author}}</div>
      <div>{{details.year}}</div>
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
#SongsCard {
    height: 400px;
    width: 220px;
    display: inline-block;
    background-color: #2e3a46;
    margin: 10px;
    text-align: center;
    img {
        height: 200px;
        width: 200px;
    }
    h3 {
        color: #fff;
    }
    div {
        color: #6f6962;
    }
}
</style>