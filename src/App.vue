<template>
  <div id="app">
    <div class="ui container">
      <img src="./assets/sam.png"/>
      <h1>SAM - Space Availability Monitor</h1>
      <actions class="ui segment"></actions>
      <space-list class="ui segment"></space-list>
      <h5>@Copyright Fighting Piledrivers</h5>
      <h3>Thanks to DDCT Hackday 2017 to make this happens.</h3>
    </div>
  </div>
</template>

<script>
import Actions from './components/Actions'
import SpaceList from './components/SpaceList'

export default {
  name: 'app',
  components: {
    Actions,
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
