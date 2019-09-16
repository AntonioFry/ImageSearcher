<template>
  <section id="image-section">
    <ImageCard v-for="data in searchResults" v-bind:data="data" v-bind:key="data.id" />
  </section>
</template>

<script>
import ImageCard from './ImageCard';

export default {
  name: "image-section",
  props: {
    searchResults: Array,
  },
  components: {
    ImageCard
  }
}
</script>

<style scoped>
  section {
    min-height: 500px;
    width: 100%;
  }
</style>