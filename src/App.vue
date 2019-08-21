<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ItemPost :check-show="currentClick" @currentClick="clickParent($event)"/>
  </div>
</template>

<script>
import ItemPost from '../components/ItemPost'
export default {
  name: 'app',
  components: {
    ItemPost
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      currentClick: true
    }
  },
  methods: {
    clickParent(clickChild) {
      this.currentClick = clickChild
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
