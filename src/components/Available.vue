<template>
<table class="ui inverted green selectable celled table">
    <thead>
      <tr>
        <th class="left aligned">AVAILABLE</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="space in spaces">
        <td class="left aligned">{{space.id}}</td>
      </tr>
    </tbody>
  </table>
</template>

<script type = "text/javascript" >

export default {
  name: 'Available',
  props: ['spaces']
}
</script>
<style>
</style>
