<template>
  <!--<img alt="Vue logo" src="./assets/logo.png">-->
  <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
  <CharacterBasics/>
  <CharacterClass/>
  <AbilityScores/>
  <CharacterDescription/>
</template>

<script>
import CharacterBasics from './components/CharacterBasics.vue'
import CharacterClass from './components/CharacterClass.vue'
import AbilityScores from './components/AbilityScores.vue'
import CharacterDescription from './components/CharacterDescription.vue'

export default {
  name: 'App',
  components: {
    CharacterBasics,
    CharacterClass,
    AbilityScores,
    CharacterDescription
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
