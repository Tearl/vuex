<template>
  <div id="app">
    <h3>welcome to your vuex-demo</h3>
    <input type="button" value="增加" @click="increment">
    <input type="button" value="减少" @click="decrement">
    <input type="button" value="偶数才能点击" @click="clickOdd">
    <input type="button" value="点击异步增加" @click="clicknysc">
    <div>现在数字为: {{count}}, 它是个 {{getOdd}}</div>
    <div>111222</div>
  </div>
</template>

<script>
import {mapGetters, mapActions} from 'vuex'

  export default{
    computed: mapGetters([
      'count',
      'getOdd'
    ]),
    methods: mapActions([
      'increment',
      'decrement',
      'clickOdd',
      'clicknysc'
    ])
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

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
