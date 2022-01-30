<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">-->
  <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <CharCreate/>
  <AbilityScores/>
</template>

<script>
import CharCreate from './components/CharCreate.vue'
import AbilityScores from './components/AbilityScores.vue'

export default {
  name: 'App',
  components: {
    CharCreate,
    AbilityScores
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
