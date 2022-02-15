<template>
   <span>Ability Scores</span>
    <br/>
    <input type="radio" id="abilitygen_3d6" value="3d6" name="abilityGenType" v-model="abilityGenType">
    <label for="abilitygen_3d6">3d6</label>
    <input type="radio" id="abilitygen_4d6" value="4d6" name="abilityGenType" v-model="abilityGenType">
    <label for="abilitygen_4d6">4d6 drop lowest</label>
    <input type="radio" id="abilitygen_point_buy" value="point_buy" name="abilityGenType" v-model="abilityGenType">
    <label for="abilitygen_point_buy">Point Buy</label>
    <input type="radio" id="abilitygen_random" value="random" name="abilityGenType" v-model="abilityGenType">
    <label for="abilitygen_random">Random</label>
    <br/>
    <button @click="generateAbilityScores(); generateAbilityScore()">Generate Ability Scores</button>
    <br/>
    <label for="charcreate_str">Strength:</label>
    <input type="text" id="charcreate_str" v-model="strScore"/>
    <label for="charcreate_dex">Dexterity:</label>
    <input type="text" id="charcreate_dex" v-model="dexScore"/>
    <label for="charcreate_con">Constitution:</label>
    <input type="text" id="charcreate_con" v-model="conScore"/>
    <label for="charcreate_int">Intelligence:</label>
    <input type="text" id="charcreate_int" v-model="intScore"/>
    <label for="charcreate_wis">Wisdom:</label>
    <input type="text" id="charcreate_wis" v-model="wisScore"/>
    <label for="charcreate_cha">Charisma:</label>
    <input type="text" id="charcreate_cha" v-model="chaScore"/>
    <br/>
    <br/>
</template>

<script>
export default {
  name: 'AbilityScores',
  data(){
    return {
        diceMin: 1,
        diceMax: 7, //Account for off-by-one
        abilityGenType: "",
        strScore: 0,
        dexScore: 0,
        conScore: 0,
        intScore: 0,
        wisScore: 0,
        chaScore: 0,
    }
  },
  methods:{
    generateAbilityScores() {
        //alert(this.abilityGenType);
        switch(this.abilityGenType) {
         case '3d6':
          //alert("3d6");
          for(let i = 0; i < 3; i++) {
           var strRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           alert("Dice roll: " + strRoll);
           this.strScore = this.strScore + strRoll;
           alert("Strength score: " + this.strScore);
          }
          //alert(this.strScore);
          break;
         case '4d6':
          alert("4d6");
          break;
         case 'point_buy':
          alert("point_buy");
          break;
         case 'random':
          alert("4d6");
          break;
         default:
          alert('No method selected');
          break;
        }
    }
  }
};
</script>