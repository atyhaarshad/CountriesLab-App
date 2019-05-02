<template lang="html">
  <div class="">
  <!-- <li v-on:click="handleClick">{{country.name}}</li> -->

  <select v-on:click="handleClick">
    <option v-for="(for country in countries)">{{country.name}}</option>
  </select>
  </div>

</template>

<script>
import {eventBus} from '../main.js'

export default {
  name: 'list-component',
  props: ['country'],
  methods: {
    handleClick: function(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
