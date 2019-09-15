<template>
  <form id="image-search" @submit.prevent="handleSubmit">
    <label>Search Image</label>
    <input type="text"/>
    <button>Search<button>
  </form>
</template>

<script>
export default {
  name: 'image-search',
  data() {
    return {
      search: {
        param: ''
      },
    }
  },
  methods: {
    handleSubmit() {
      this.$emit('set:search-results', this.search)
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>