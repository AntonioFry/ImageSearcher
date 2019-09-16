<template>
  <div id="image-card" class="main-container">
    <img :src='data.urls.thumb' :alt="data.alt_description"/>
    <div class="text-container">
      <p>{{ data.alt_description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'image-card',
  props: {
    data: Object
  }
}
</script>

<style scoped>
  .main-container {
    border: 1px solid rgb(223, 223, 223);
    margin: 7px;
    width: 200px;
  }
  p {
    text-align: center;
  }
  .text-container {
    padding: 0px 4px;
  }
</style>