<template>
  <main id="app">
    <ProjectHeader />
    <ImageSearch />
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
  }
}
</script>

<style>
  body {
    margin: 0;
  }
</style>
