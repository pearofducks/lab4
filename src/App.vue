<template>
  <div id="app">
    <div>
      <h4>Compare</h4>
      <label for="compare" style="padding-right: 8px">Enter a number to compare to</label>
      <input id="compare" type="number" number v-model.number="compareNumber">
    </div>
    <div>
      <h4>Generate</h4>
      <button @click="addRandomNumber">Generate a number</button>
    </div>
    <div>
      <h4>Filter</h4>
      <button>Show only odd numbers</button>
      <button>Show only even numbers</button>
      <button>Show all numbers</button>
    </div>
    <div>
      <h4>Results</h4>
      <results-list :list="numbers" :compareTo="compareNumber" />
    </div>
  </div>
</template>

<script>
import ResultsList from './ResultsList'

export default {
  name: 'app',
  data: () => ({
    compareNumber: 0,
    numbers: []
  }),
  components: { ResultsList },
  methods: {
    addRandomNumber() {
      this.numbers.push(this.generateRandom())
    },
    generateRandom() {
      return Math.round(Math.random() * 1000)
    }
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
