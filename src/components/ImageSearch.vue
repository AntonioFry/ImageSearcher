<template>
  <section id="image-search">
    <form @submit.prevent="handleSubmit">
      <label>Search Image</label>
      <input type="text"/>
      <button>Search</button>
    </form>
  </section>
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

<style scoped>
  section {
    display: flex;
    justify-content: center;
    width: 100%;
  }
  form {
    display: flex;
    flex-direction: column;
    width: 25%;
  }
  label {
    font-size: 1.5em;
    margin: 10px 0 5px;
  }
  button,
  input {
    font-size: 1em;
    height: 20px;
    margin: 5px 0;
  }
</style>