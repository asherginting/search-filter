<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo-search.png" style="height: 100px; width: 100px;">
    <SearchFilter :names="Dummynames" />
  </div>
</template>

<script>
import SearchFilter from './components/SearchFilter.vue'

export default {
  name: 'App',
  components: {
    SearchFilter
  },
  data() {
    return {
      Dummynames: [
        'Asher Azriel Ginting', 'Donny S', 'Judika S', 'Rael Bangun', 'Kristanto G',
        'Dian Lestari', 'tanto wijaya', 'hendra pratama', 'Indah Permata', 'Joko Santoso',
        'Kartika Sari', 'lia indriani', 'Mega Kurniawan', 'Nina Amelia', 'dicky zulkarnain',
        'Putri Anggraini', 'Joel S', 'Sari Kusumawati', 'Taufik Rahman', 'Nurul Fauziah',
        'Vita Fitriani', 'Sarmila', 'budiman harjono', 'Yanti', 'Sri Kartika Sari',
        'Abdul Hakim', 'budi jhon', 'santania aldita', 'galuh sekar', 'Yenni Sinta',
      ]

    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
