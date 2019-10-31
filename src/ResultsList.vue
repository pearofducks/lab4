<template>
  <ul>
    <result v-for="(number, i) in list"
      :key="'result' + i"
      :number="number"
      :compareTo="compareTo" />
  </ul>
</template>

<script>
import Result from './Result'

export default {
  name: 'ResultsList',
  components: { Result },
  props: {
    filter: String,
    list: Array,
    compareTo: Number
  },
  computed: {
    filteredList() {
      // this should return a filtered list when 'filter' is set by the user
      return this.list
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
  padding-left: 0;
}
</style>
