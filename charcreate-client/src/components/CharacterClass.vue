<template>
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
</template>

<script>
export default {
  name: 'CharacterClass'
};
</script>