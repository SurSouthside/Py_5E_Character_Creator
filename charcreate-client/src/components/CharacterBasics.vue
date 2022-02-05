<template>
    <!--Step 1 start-->
    <label for="charcreate_name">Name:</label>
    <input type="text" id="charcreate_name" v-model="inputValue"/>
    <br/>
    <label for="charcreate_race">Race:</label>
    <select v-model="race" id="charcreate_race">
        <option>Dwarf</option>
        <option>Elf</option>
    </select>
    <br/>
    <br/>
    <!--Step 1 end-->
</template>

<script>
export default {
  name: 'CharacterBasics'
};
</script>