<!--Steps based on 5th Edition Player Handbook character creation-->

<template>
  <div>
    <p>Character Creator</p>
    <!--Step 1 start-->
    <label for="charcreate_name">Name:</label>
    <input type="text" id="charcreate_name"/>
    <br/>
    <label for="charcreate_race">Race:</label>
    <select id="charcreate_race"/>
    <br/>
    <br/>
    <!--Step 1 end-->
    <!--Step 2 start-->
    <label for="charcreate_class">Class:</label>
    <select id="charcreate_class"/>
    <br/>
    <label for="charcreate_level">Level:</label>
    <select id="charcreate_level"/>
    <br/>
    <br/>
    <!--Step 2 end-->
    <!--Step 3 start-->
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
    <!--Step 3 end-->
    <!--Step 4 start-->
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