<template>
  <main id="app">
    <ProjectHeader />
    <ImageSearch @set:search-results="searchImages"/>
    <ImageSection :searchResults="searchResults"/>
  </main>
</template>

<script>
import ProjectHeader from './components/Header';
import ImageSearch from './components/ImageSearch';
import ImageSection from './components/ImageSection';

const API_KEY = process.env.VUE_APP_API_KEY

export default {
  name: 'app',
  components: {
    ProjectHeader,
    ImageSearch,
    ImageSection
  },
  data() {
    return {
      searchResults: [],
      errorMessage: '',
    }
  },
  methods: {
    async searchImages (searchParam) {
      try {
        const response = await fetch(`https://api.unsplash.com/search/photos?page=1&query=${searchParam}&client_id=${API_KEY}`);
        const results = await response.json();
        const cleanedData = results.results.map(data => {
          return { id: data.id, alt_description: data.alt_description, urls: data.urls }
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
