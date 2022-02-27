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
    <button v-if="abilityGenType !== 'point_buy'" @click="generateAbilityScores(); generateAbilityScore()">Generate Ability Scores</button>
    <br/>
    <div v-if="abilityGenType === 'point_buy'">
     <PointBuy></PointBuy>
    </div>
    <br/>
    <!--TODO: Disable 'Generate Ability Scores' button when point_buy radio selected?-->
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

import PointBuy from './PointBuy.vue'

export default {
  name: 'AbilityScores',
  components: {
    PointBuy
  },
  data(){
    return {
        diceMin: 1,
        diceMax: 7, //Account for off-by-one
        randomMin: 1,
        randomMax: 21, //Account for off-by-one
        pointBuyLimit: 27,
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
        this.strScore = 0;
        this.dexScore = 0;
        this.conScore = 0;
        this.intScore = 0;
        this.wisScore = 0;
        this.chaScore = 0;

        var strRoll = 0;
        var dexRoll = 0;
        var conRoll = 0;
        var intRoll = 0;
        var wisRoll = 0;
        var chaRoll = 0;

        var minRoll = 0;
        var minRollIndex = 0;

        var strScoreArray = [];
        var dexScoreArray = [];
        var conScoreArray = [];
        var intScoreArray = [];
        var wisScoreArray = [];
        var chaScoreArray = [];

        switch(this.abilityGenType) {
         case '3d6':
          //alert("3d6");

          //STR
          for(let i = 0; i < 3; i++) {
           strRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           //alert("Dice roll: " + strRoll);
           this.strScore = this.strScore + strRoll;
           //alert("Strength score: " + this.strScore);
          }

          //DEX
          for(let i = 0; i < 3; i++) {
           dexRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           //alert("Dice roll: " + dexRoll);
           this.dexScore = this.dexScore + dexRoll;
           //alert("Dexterity score: " + this.dexScore);
          }

          //CON
          for(let i = 0; i < 3; i++) {
           conRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           //alert("Dice roll: " + conRoll);
           this.conScore = this.conScore + conRoll;
           //alert("Constitution score: " + this.conScore);
          }

          //INT
          for(let i = 0; i < 3; i++) {
           intRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           //alert("Dice roll: " + intRoll);
           this.intScore = this.intScore + intRoll;
           //alert("Intelligence score: " + this.intScore);
          }

          //WIS
          for(let i = 0; i < 3; i++) {
           wisRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           //alert("Dice roll: " + wisRoll);
           this.wisScore = this.wisScore + wisRoll;
           //alert("Wisdom score: " + this.wisScore);
          }

          //CHA
          for(let i = 0; i < 3; i++) {
           chaRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
           //alert("Dice roll: " + chaRoll);
           this.chaScore = this.chaScore + chaRoll;
           //alert("Charisma score: " + this.chaScore);
          }                        
          break;
         case '4d6':
          //alert("4d6");

          //STR
          for(let i = 0; i < 4; i++) {
            strRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
            //alert("Dice roll: " + strRoll);
            strScoreArray.push(strRoll);
            //alert("Strength score: " + strScoreArray.reduce(function (previousValue, currentValue) {
             //return previousValue + currentValue }, 0));
           }
           minRoll = Math.min.apply(null,strScoreArray)
           //alert("Lowest roll: " + minRoll);
           minRollIndex = strScoreArray.indexOf(minRoll);
           //alert("Lowest roll index: " + minRollIndex);
           strScoreArray.splice(minRollIndex, 1);
           this.strScore = strScoreArray.reduce((partialSum, a) => partialSum + a, 0);
           //alert("Strength score: " + this.strScore);

          //DEX
          for(let i = 0; i < 4; i++) {
            dexRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
            //alert("Dice roll: " + dexRoll);
            dexScoreArray.push(dexRoll);
            //alert("Dexterity score: " + dexScoreArray.reduce(function (previousValue, currentValue) {
             //return previousValue + currentValue }, 0));
           }
           minRoll = Math.min.apply(null,dexScoreArray)
           //alert("Lowest roll: " + minRoll);
           minRollIndex = dexScoreArray.indexOf(minRoll);
           //alert("Lowest roll index: " + minRollIndex);
           dexScoreArray.splice(minRollIndex, 1);
           this.dexScore = dexScoreArray.reduce((partialSum, a) => partialSum + a, 0);
           //alert("Dexterity score: " + this.dexScore);
           
          //CON
          for(let i = 0; i < 4; i++) {
            conRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
            //alert("Dice roll: " + conRoll);
            conScoreArray.push(conRoll);
            //alert("Constitution score: " + conScoreArray.reduce(function (previousValue, currentValue) {
             //return previousValue + currentValue }, 0));
           }
           minRoll = Math.min.apply(null,conScoreArray)
           //alert("Lowest roll: " + minRoll);
           minRollIndex = conScoreArray.indexOf(minRoll);
           //alert("Lowest roll index: " + minRollIndex);
           conScoreArray.splice(minRollIndex, 1);
           this.conScore = conScoreArray.reduce((partialSum, a) => partialSum + a, 0);
           //alert("Constitution score: " + this.conScore);
           
          //INT
          for(let i = 0; i < 4; i++) {
            intRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
            //alert("Dice roll: " + intRoll);
            intScoreArray.push(intRoll);
            //alert("Intelligence score: " + intScoreArray.reduce(function (previousValue, currentValue) {
             //return previousValue + currentValue }, 0));
           }
           minRoll = Math.min.apply(null,intScoreArray)
           //alert("Lowest roll: " + minRoll);
           minRollIndex = intScoreArray.indexOf(minRoll);
           //alert("Lowest roll index: " + minRollIndex);
           intScoreArray.splice(minRollIndex, 1);
           this.intScore = intScoreArray.reduce((partialSum, a) => partialSum + a, 0);
           //alert("Intelligence score: " + this.intScore);
           
           
          //WIS
          for(let i = 0; i < 4; i++) {
            wisRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
            //alert("Dice roll: " + wisRoll);
            wisScoreArray.push(wisRoll);
            //alert("Wisdom score: " + wisScoreArray.reduce(function (previousValue, currentValue) {
             //return previousValue + currentValue }, 0));
           }
           minRoll = Math.min.apply(null,wisScoreArray)
           //alert("Lowest roll: " + minRoll);
           minRollIndex = wisScoreArray.indexOf(minRoll);
           //alert("Lowest roll index: " + minRollIndex);
           wisScoreArray.splice(minRollIndex, 1);
           this.wisScore = wisScoreArray.reduce((partialSum, a) => partialSum + a, 0);
           //alert("Wisdom score: " + this.wisScore);

          //CHA
          for(let i = 0; i < 4; i++) {
            chaRoll = Math.floor(Math.random() * (this.diceMax - this.diceMin) + this.diceMin);
            //alert("Dice roll: " + chaRoll);
            chaScoreArray.push(chaRoll);
            //alert("Charisma score: " + chaScoreArray.reduce(function (previousValue, currentValue) {
             //return previousValue + currentValue }, 0));
           }
           minRoll = Math.min.apply(null,chaScoreArray)
           //alert("Lowest roll: " + minRoll);
           minRollIndex = chaScoreArray.indexOf(minRoll);
           //alert("Lowest roll index: " + minRollIndex);
           chaScoreArray.splice(minRollIndex, 1);
           this.chaScore = chaScoreArray.reduce((partialSum, a) => partialSum + a, 0);
           //alert("Charisma score: " + this.chaScore);

          break;
         case 'point_buy':
          alert("point_buy");
          this.strScore = 8;
          this.dexScore = 8;
          this.conScore = 8;
          this.intScore = 8;
          this.wisScore = 8;
          this.chaScore = 8;
          break;
         case 'random':
          //alert("random");
          this.strScore = Math.floor(Math.random() * (this.randomMax - this.randomMin) + this.randomMin);
          this.dexScore = Math.floor(Math.random() * (this.randomMax - this.randomMin) + this.randomMin);
          this.conScore = Math.floor(Math.random() * (this.randomMax - this.randomMin) + this.randomMin);
          this.intScore = Math.floor(Math.random() * (this.randomMax - this.randomMin) + this.randomMin);
          this.wisScore = Math.floor(Math.random() * (this.randomMax - this.randomMin) + this.randomMin);
          this.chaScore = Math.floor(Math.random() * (this.randomMax - this.randomMin) + this.randomMin);
          break;
         default:
          alert('No method selected');
          break;
        }
    }
  }
};
</script>