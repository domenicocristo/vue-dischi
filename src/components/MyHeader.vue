<template>
    <header>
        <img src="../assets/logo.png" alt="logo">
        <h1>Music</h1>
    </header>
</template>

<script>
export default {
  name: 'MyHeader',
}
</script>

<style scoped lang="scss">
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
</style>