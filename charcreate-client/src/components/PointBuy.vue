<template>
    The basic rules of point buy are as follows
    <li>
        <ul>Each ability score begins at 8, and can go no lower than 8</ul>
        <ul>Any ability score above 8 costs a certain number of points to increase</ul>
        <ul>You have 27 points with which to increase your ability scores</ul>
        <ul>The maximum ability score before applying racial bonuses is 15</ul>
    </li>
    Use the following table to assist in point buy calculations
    <table>
        <thead colspan="2"></thead>
        <tbody>
            <tr>
                <td>Ability Score</td>
                <td>Point Cost</td>
            </tr>
            <tr>
                <td>8</td>
                <td>0</td>
            </tr>
            <tr>
                <td>9</td>
                <td>1</td>
            </tr>
            <tr>
                <td>10</td>
                <td>2</td>
            </tr>
            <tr>
                <td>11</td>
                <td>3</td>
            </tr>
            <tr>
                <td>12</td>
                <td>4</td>
            </tr>
            <tr>
                <td>13</td>
                <td>5</td>
            </tr>
            <tr>
                <td>14</td>
                <td>7</td>
            </tr>
            <tr>
                <td>15</td>
                <td>9</td>
            </tr>
        </tbody>
    </table>
    <label for="pointbuy_bank">Available Points:</label>
    <input type="text" id="pointbuy_bank" readonly="readonly" v-model="pointBuyAvailable"/>
</template>


<script>
export default {
  name: 'PointBuy',
  data(){
    return {
        pointBuyMin: 0,
        pointBuyMax: 27,
        pointBuyAvailable: 27,
        abilityScoreMin: 8,
        abilityScoreMax: 15
    }
  },
}
</script>

<style>

</style>