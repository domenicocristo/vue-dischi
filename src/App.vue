<template>
  <div id="app">
    <header>
      <img src="./assets/logo.png" alt="logo">
      <h1>Music</h1>
    </header>

    <main>
      <SongsContainer/>
    </main>
  </div>
</template>

<script>
import SongsContainer from './components/SongsContainer.vue'

export default {
  name: 'App',
  components: {
    SongsContainer
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif;
}

header {
  display: flex;
  align-items: center;
  background-color: #2e3a46;
}
  img {
    height: 50px;
    margin: 10px;
  }
  h1 {
    display: inline-block;
    color: #fff;
    margin-left: 10px;
  }

main {
  background-color: #1e2d3b;
}
</style>