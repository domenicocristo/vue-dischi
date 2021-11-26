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
    cursor: pointer;
    border: 1px solid #6f6962;
    img {
        height: 200px;
        width: 200px;
    }
    img:hover {
        border: 5px solid #3fb983;
    }
    h3 {
        color: #fff;
        margin: 10px 0;
    }
    div {
        color: #6f6962;
    }
}
</style>