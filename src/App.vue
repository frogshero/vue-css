<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <padding-test /> -->
    <!-- <form-test /> -->
    <form-lay-out :changeDataFlg.sync="changeDataFlg"/>
    <el-button @click="changeDataFlg=true">show</el-button>
  </div>
</template>

<script>
import FormLayOut from './components/FormLayOut.vue'
import FormTest from './components/FormTest.vue'
import HelloWorld from './components/HelloWorld.vue'
import PaddingTest from './components/PaddingTest.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    PaddingTest,
    FormTest,
    FormLayOut
  },
  data() {
    return {
      changeDataFlg: false,
    }
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
