<template>
    <div id="">
        <select v-model="selectGenre" @change="$emit('selectEvent', selectGenre)">
            <option>Tutti</option>
            <option>Rock</option>
            <option>Pop</option>
            <option>Jazz</option>
            <option>Metal</option>
      </select>
    </div>
</template>

<script>
export default {
  name: 'MyFilter',
  data() {
      return {
          selectGenre: "",
      }
  },
}
</script>

<style scoped lang="scss">

</style>