<template>
  <div id="image-card">
    <!-- <img /> -->
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

</style>