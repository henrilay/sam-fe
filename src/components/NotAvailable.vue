<template>
  <table class="ui inverted red selectable celled table">
    <thead>
      <tr>
        <th class="left aligned">NOT AVAILABLE</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="space in spaces">
        <td class="left aligned">{{space.id}} ({{space.reg}})</td>
      </tr>
    </tbody>
  </table>
</template>

<script type = "text/javascript" >

export default {
  name: 'NotAvailable',
  props: ['spaces']
}
</script>
<style>
</style>
