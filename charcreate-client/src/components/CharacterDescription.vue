<template>
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
        <option>Acolyte</option>
        <option>Charlatan</option>
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
</template>

<script>
export default {
  name: 'CharacterDescription'
};
</script>