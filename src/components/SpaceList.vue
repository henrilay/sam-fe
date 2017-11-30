<template>
  <div class="ui container">
    <total-count v-bind:count="totalAvailable"></total-count>
    <div class="ui two column grid">
      <div class="column">
        <available v-bind:spaces="availableSpaces"></available>
      </div>
      <div class="column">
        <not-available v-bind:spaces="notAvailableSpaces"></not-available>
      </div>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
  import TotalCount from './TotalCount'
  import Availability from './Availability'
  import Available from './Available'
  import NotAvailable from './NotAvailable'

  export default {
    name: 'SpaceList',
    data () {
      return {
        allSpaces: []
      }
    },
    mounted () {
      this.getLatest()
    },
    methods: {
      getLatest () {
        axios.get('http://localhost:9001/sam-be/events/read/latest').then(res => {
          this.allSpaces = res.data
        }).catch(err => {
          console.log(err)
          this.allSpaces = [
            {
              id: 'space1',
              in: true,
              reg: 'AA11BB3'
            }, {
              id: 'space2',
              in: false
            }, {
              id: 'space3',
              in: true,
              reg: 'GG56CD9'
            }, {
              id: 'space4',
              in: false
            }
          ]
        })
      }
    },
    computed: {
      totalAvailable () {
        return this.allSpaces.filter(s => { return s.in === false }).length
      },
      availableSpaces () {
        return this.allSpaces.filter(s => { return s.in === false })
      },
      notAvailableSpaces () {
        return this.allSpaces.filter(s => { return s.in === true })
      }
    },
    components: {
      TotalCount,
      Availability,
      Available,
      NotAvailable
    }
  }
</script>
