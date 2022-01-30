<template>
   <span>Ability Scores</span><button @click="generateAbilityScores(); generateAbilityScore()">Generate Ability Scores</button>
    <br/>
    <label for="charcreate_str">Strength:</label>
    <input type="text" id="charcreate_str"/>
    <label for="charcreate_dex">Dexterity:</label>
    <input type="text" id="charcreate_dex"/>
    <label for="charcreate_con">Constitution:</label>
    <input type="text" id="charcreate_con"/>
    <label for="charcreate_int">Intelligence:</label>
    <input type="text" id="charcreate_int"/>
    <label for="charcreate_wis">Wisdom:</label>
    <input type="text" id="charcreate_wis"/>
    <label for="charcreate_cha">Charisma:</label>
    <input type="text" id="charcreate_cha"/>
    <br/>
    <br/>
</template>

<script>
export default {
  name: 'AbilityScores',
  data(){
    return {
        strScore: "",
        dexScore: "",
        conScore: "",
        intScore: "",
        wisScore: "",
        chaScore: "",
    }
  },
  methods:{
    generateAbilityScores() {
        alert(this.inputValue);
        console.log(this.inputValue);
    }
  }
};
</script>