<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <padding-test />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import PaddingTest from './components/PaddingTest.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    PaddingTest
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* 默认居中 */
  /* text-align: center;   */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
