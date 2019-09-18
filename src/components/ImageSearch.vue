<template>
  <section>
    <form id="image-search" @submit.prevent="handleSubmit">
      <label>Search Image</label>
      <input type="text" v-model="search.param" />
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
      this.$emit('set:search-results', this.search.param)
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
    margin: 10px 0px;
    width: 15%;
  }
  label {
    font-size: 1.5em;
    margin: 10px 0 5px;
  }
  button,
  input {
    border: 1px solid black;
    border-radius: 20px;
    font-size: 1em;
    height: 30px;
    margin: 5px 0;
    padding: 0px 10px;
  }
</style>