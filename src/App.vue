<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <h6>{{test}}</h6>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'
export default {
  name: 'App',
  setup() {
    let test = ref(0);
    test.value = 222;
    return {
      test
    }
  },
  created() {
    console.log(this.$)
  },
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
