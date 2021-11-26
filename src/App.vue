<template>
  <div id="app">
    <header>
      <img src="../assets/logo.png" alt="logo">
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
}
</style>