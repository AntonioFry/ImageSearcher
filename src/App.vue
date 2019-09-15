<template>
  <main id="app">
    <ProjectHeader />
  </main>
</template>

<script>
import ProjectHeader from './components/Header';

export default {
  name: 'app',
  components: {
    ProjectHeader,
  }
}
</script>

<style>
  body {
    margin: 0;
  }
</style>
