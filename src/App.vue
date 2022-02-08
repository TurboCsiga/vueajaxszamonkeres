<template>
  <div id="app">
    <table>
      <tr>
        <th>Személy</th>
        <th>Magasság</th>
        <th>Ár</th>
        <th>Műveletek</th>
      </tr>
      <Tablazat v-for="s in statues" :key="s.id" :statue="s"/>
    </table>
  </div>
</template>

<script>
import Tablazat from './components/Tablazat.vue'

export default {
  name: 'App',
  components: {
    Tablazat
  },
  data: function() {
    return {
      statues: {},
    }
  },
  mounted() {
    fetch('http://localhost:8000/api/statues')
    .then(response => response.json())
    .then(data => this.statues = data);
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
