<template>
  <div id="image-card">
    <img :src='data.urls.thumb' />
    <p>{{ data.alt_description }}</p>
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
  div {
    width: 300px;
  }
  image {
    height: 100px;
    width: 100px;
  }
</style>