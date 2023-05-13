<template>
  <div class="search-filter">
    <h2 class="search-filter-title">Search Your Name</h2>
    <div class="search-filter-input">
      <input type="text" v-model="searchQuery" placeholder="Search ...." class="search-filter__input">
    </div>
    <div class="search-filter-list">
      <ul class="search-filter-name">
        <li v-for="(name, index) in filteredNames" :key="index" class="search-filter-listname">{{ name }}</li>
        <li v-if="filteredNames.length === 0" class="search-filter-notfound">No names match!</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchFilter',
  props: {
    names: Array 
  },
  data() {
    return {
      searchQuery: ''
    }
  },
  computed: {
    filteredNames() {
      return this.names.filter(name =>
        name.toLowerCase().includes(this.searchQuery.toLowerCase())
      )
    }
  }
}
</script>

<style scoped>
.search-filter {
  max-width: 600px;
  margin: 0 auto;
  font-family: Arial, sans-serif;
}

.search-filter-title {
  font-size: 32px;
  margin-bottom: 20px;
}

.search-filter-input {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
  border-bottom: 2px solid #eee;
}

.search-filter__input {
  flex: 1;
  padding: 10px;
  font-size: 16px;
  border: none;
  background-color: transparent;
  outline: none;
}

.search-filter-list {
  max-height: 600px; 
  overflow-y: auto;
}

.search-filter-name {
  list-style-type: none;
  padding: 0;
}

.search-filter-listname {
  padding: 10px;
  border-bottom: 1px solid #eee;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.search-filter-listname:hover {
  background-color: #f5f5f5;
}

.search-filter-notfound {
  color: #aaa;
  font-size: 14px;
  margin-top: 20px;
}
</style>
