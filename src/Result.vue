<template>
  <li>{{ output }}</li>
</template>

<script>
export default {
  name: 'Result',
  props: {
    number: Number,
    compareTo: Number
  },
  computed: {
    output() {
      // this should say "NUMBER is greater/less than NUMBER"
      return `${this.number} is being compared to ${this.compareTo}`
    }
  }
}
</script>

<style scoped>
li {
  color: purple;
}
</style>
