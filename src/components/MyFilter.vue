<template>
    <div id="selectGenre">
        <h3>Genere:</h3>
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
#selectGenre {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 50px;
    h3 {
        color: #fff;
        margin-right: 5px;
    }
    select {
        padding: 5px 10px;
        color: #fff;
        background-color: #2e3a46;
        cursor: pointer;
        border-radius: 10px;
    }
}
</style>