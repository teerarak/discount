<template>
  <div id="app">
    <h1>{{ cal }}</h1>
    <input v-model="input">
    <div class="">
      <div class="">
        <button @click="discount = 0.05">5%</button>
        <button @click="discount = 0.1">10%</button>
        <button @click="discount = 0.15">15%</button>
      </div>
      <div class="">
        <button @click="discount = 0.2">20%</button>
        <button @click="discount = 0.3">30%</button>
        <button @click="discount = 0.4">40%</button>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      input: 0,
      discount: 0
    }
  },
  computed: {
    cal () {
      return this.input - this.input * this.discount
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
button {
  background: #FFCCFF;
  border-radius: 3px;
  width: 5%;
}
</style>
