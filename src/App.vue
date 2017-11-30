<template>
  <div id="app">
    <div class="ui container">
      <img src="./assets/sam.png"/>
      <h1>SAM - Space Availability Monitor</h1>
      <space-list></space-list>
    </div>
  </div>
</template>

<script>
import SpaceList from './components/SpaceList'

export default {
  name: 'app',
  components: {
    SpaceList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
