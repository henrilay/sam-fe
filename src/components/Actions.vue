<template>
  <div class="ui container">
    <div class="ui animated fade blue fluid button" tabindex="0" v-on:click="predictAvailability">
      <div class="visible content">Hey Sam</div>
      <div class="hidden content">
        I'm leaving now!
      </div>
    </div>
    <div class='ui segment' v-show="isPredicting">
      <div class='content'>
        You should reach Plaza 2 Car Park 5 in about 32 minutes, you have 10% chance to find an available space...Good luck!
      </div>
    </div>
  </div>
</template>

<script type = "text/javascript" >

export default {
  name: 'Actions',
  data () {
    return {
      isPredicting: false
    }
  },
  methods: {
    predictAvailability () {
      this.isPredicting = true
    }
  }
}
</script>
<style>
</style>
