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
    align-content: center;
    align-items: center;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    max-height: 1000px;
    width: 100%;
  }
</style>