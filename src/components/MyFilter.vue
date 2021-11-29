<template>
    <div>
        <select @change="$emit('select', selectGenre)">
            <option >Tutti</option>
            <option >Rock</option>
            <option >Pop</option>
            <option >Jazz</option>
            <option >Metal</option>
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
  methods: {
      resetSelect() {
          this.selectGenre = "";
          this.$emit('select', this.selectGenre);
      }
  }
}
</script>

<style scoped lang="scss">

</style>