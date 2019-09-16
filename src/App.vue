<template>
  <main id="app">
    <ProjectHeader />
    <ImageSearch @set:search-result="searchImages"/>
  </main>
</template>

<script>
import ProjectHeader from './components/Header';
import ImageSearch from './components/ImageSearch';

export default {
  name: 'app',
  components: {
    ProjectHeader,
    ImageSearch,
  },
  data() {
    return {
      searchResults: [],
    }
  }
}
</script>

<style>
  body {
    margin: 0;
  }
</style>
