<template>
   <span>Ability Scores</span>
    <br/>
    <input type="radio" id="abilitygen_3d6" value="3d6" v-model="abilitygentype">
    <label for="abilitygen_3d6">3d6</label>
    <input type="radio" id="abilitygen_4d6" value="4d6" v-model="abilitygentype">
    <label for="abilitygen_4d6">4d6 drop lowest</label>
    <input type="radio" id="abilitygen_point_buy" value="point_buy" v-model="abilitygentype">
    <label for="abilitygen_point_buy">Point Buy</label>
    <input type="radio" id="abilitygen_random" value="random" v-model="abilitygentype">
    <label for="abilitygen_random">Random</label>
    <br/>
    <button @click="generateAbilityScores(); generateAbilityScore()">Generate Ability Scores</button>
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
        alert("Ability scores here");
    }
  }
};
</script>