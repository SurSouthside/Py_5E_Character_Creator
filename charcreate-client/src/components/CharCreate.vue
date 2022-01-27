<!--Steps based on 5th Edition Player Handbook character creation-->

<template>
  <div>
    <p>Character Creator</p>
    <!--Step 1 start-->
    <label for="charcreate_name">Name:</label>
    <input type="text" id="charcreate_name"/>
    <br/>
    <label for="charcreate_race">Race:</label>
    <select v-model="race" id="charcreate_race">
        <option>Dwarf</option>
        <option>Elf</option>
    </select>
    <br/>
    <br/>
    <!--Step 1 end-->
    <!--Step 2 start-->
    <label for="charcreate_class">Class:</label>
   <select v-model="race" id="charcreate_class">
        <option>Barbarian</option>
        <option>Bard</option>
    </select>
    <br/>
    <label for="charcreate_level">Level:</label>
    <select id="charcreate_level"/>
    <label for="charcreate_hp">Hit Points:</label>
    <input type="text" id="charcreate_hp"/>
    <br/>
    <label for="charcreate_proficiency">Proficiency Bonus:</label>
    <input type="text" id="charcreate_proficiency"/>
    <br/>
    <br/>
    <!--Step 2 end-->
    <!--Step 3 start-->
    <span>Ability Scores</span>
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
    <!--Step 3 end-->
    <!--Step 4 start-->
    <span>Alignment</span>
    <br/>
    <label for="charcreate_align_lg">Lawful Good:</label>
    <input type="radio" id="charcreate_align_lg" name="alignment" value="'lg">
    <label for="charcreate_align_ng">Neutral Good:</label>
    <input type="radio" id="charcreate_align_ng" name="alignment" value="'ng">
    <label for="charcreate_align_cg">Chaotic Good:</label>
    <input type="radio" id="charcreate_align_cg" name="alignment" value="'cg">
    <br/>
    <label for="charcreate_align_ln">Lawful Neutral:</label>
    <input type="radio" id="charcreate_align_ln" name="alignment" value="'ln">
    <label for="charcreate_align_tn">True Neutral:</label>
    <input type="radio" id="charcreate_align_tn" name="alignment" value="'tn">
    <label for="charcreate_align_cn">Chaotic Neutral:</label>
    <input type="radio" id="charcreate_align_cn" name="alignment" value="cn">
    <br/>
    <label for="charcreate_align_le">Lawful Evil:</label>
    <input type="radio" id="charcreate_align_le" name="alignment" value="'le">
    <label for="charcreate_align_ne">Neutral Evil:</label>
    <input type="radio" id="charcreate_align_ne" name="alignment" value="ne">
    <label for="charcreate_align_ce">Chaotic Evil:</label>
    <input type="radio" id="charcreate_align_ce" name="alignment" value="ce">
    <br/>
    <label for="charcreate_background">Background:</label>
    <select v-model="background" id="charcreate_background">
        <option>Barbarian</option>
        <option>Bard</option>
    </select>
    <br/>
    <label for="charcreate_ideals">Ideals:</label>
    <textarea v-model="ideals" id="charcreate_ideals"></textarea>
    <br/>
    <label for="charcreate_bonds">Bonds:</label>
    <textarea v-model="bonds" id="charcreate_bonds"></textarea>
    <br/>
    <label for="charcreate_flaws">Flaws:</label>
    <textarea v-model="flaws" id="charcreate_flaws"></textarea>
    <br/>
    <br/>
    <!--Step 4 end-->
    <!--Step 5 start-->
    <!--Step 5 end-->
    <!--Step 6 start-->
    <!--Step 6 end-->
  </div>
</template>

<script>
export default {
  name: 'CharCreate'
}
</script>