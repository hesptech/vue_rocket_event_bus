<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Test v-bind:header.sync="header"/>
    <Test2 v-bind:header.sync="header"/>
  </div>
</template>

<script>
import Test from './components/Test.vue'
import Test2 from './components/Test2.vue'
export default {
  name: 'app',
  components: {
    Test,
    Test2
  },
  props: {
    headerTxt: {
      type: String,
      default: 'initial header'
    }
  },
  data (){
    return {
      header: this.headerTxt
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
