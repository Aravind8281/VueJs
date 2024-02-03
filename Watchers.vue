<template>
    <div>
      <input v-model="searchQuery" placeholder="Type to search" />
      <ul>
        <li v-for="result in searchResults" :key="result.id">{{ result.name }}</li>
      </ul>
    </div>
  </template>
  
  <script>
  
  export default {
    name:"watchers-vue",
    data() {
      return {
        searchQuery: '',
        searchResults: [],
      };
    },
    watch: {
      searchQuery: {
        handler: 'fetchSearchResults',
        immediate: false,
        deep: false,
      },
    },
    methods: {
      async fetchSearchResults() {
        // Simulate an API call
        // Replace this with your actual API call logic
        await new Promise(resolve => setTimeout(resolve, 500));
        
        // Update searchResults based on the API response
        this.searchResults = [
          { id: 1, name: 'Result A' },
          { id: 2, name: 'Result B' },
          // ... other results
        ];
      },
    },
  };
  </script>
  
