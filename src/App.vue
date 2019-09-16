<template>
  <main id="app">
    <ProjectHeader />
    <ImageSearch @set:search-result="searchImages"/>
  </main>
</template>

<script>
import ProjectHeader from './components/Header';
import ImageSearch from './components/ImageSearch';
import { accessKey } from '../apiKeys';

export default {
  name: 'app',
  components: {
    ProjectHeader,
    ImageSearch,
  },
  data() {
    return {
      searchResults: [],
      errorMessage: '',
    }
  },
  methods: {
    searchImages = async (searchParam) => {
      try {
        const response = await fetch(`https://api.unsplash.com/search/photos?page=1&query=${searchParam}&client_id=${accessKey}`);
        const results = await response.json();
        const cleanedData = results.map(data => {
          return { alt_description: data.alt_description, urls: data.urls }
        });
        this.searchResults = cleanedData;
      } catch (error) {
        this.error = error.message
      }
    }
  }
}
</script>

<style>
  body {
    margin: 0;
  }
</style>
