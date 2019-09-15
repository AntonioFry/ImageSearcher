<template>
  <form id="image-search">
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
}
</script>

<style lang="stylus" scoped>

</style>