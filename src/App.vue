<template>
  <div id="app">
    <Table type="cat"/>
    <Table type="dog"/>
  </div>
</template>

<script>
import Table from './components/Table.vue'
export default {
  name: 'App',
  components: {
    Table,
  },
  data(){
    return{


    }
  },
 
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
