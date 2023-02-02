<template>
  <div class="grid">

    <div class="gridImage">

    </div>


    <!-- Ecart entre les cases de déplacement du joueur
      52px => 35px
      30px => 20px
    -->

    <!-- Petit -->
    <!--
    <div class="caseForCharacter" style="left: 300px; top: 349px;">

    </div>

    <div class="caseForCharacter" style="left: 265px; top: 329px;">

    </div>

    <div class="caseForCharacter" style="left: 230px; top: 309px;">

    </div>

    <div class="caseForCharacter" style="left: 195px; top: 289px;">

    </div>

    <div class="caseForCharacter" style="left: 160px; top: 269px;">

    </div>

    <div class="caseForCharacter" style="left: 125px; top: 249px;">

    </div>

    <div class="caseForCharacter" style="left: 90px; top: 229px;">

    </div>

    <div class="caseForCharacter" style="left: 55px; top: 209px;">

    </div>
    -->
    <!-- ---- -->

    <!-- Grand -->
    <div class="caseForCharacter" style="left: 450px; top: 523px;">

    </div>

    <div class="caseForCharacter" style="left: 398px; top: 493px;">

    </div>

    <div class="caseForCharacter" style="left: 346px; top: 463px;">

    </div>

    <div class="caseForCharacter" style="left: 294px; top: 433px;">

    </div>

    <div class="caseForCharacter" style="left: 242px; top: 403px;">

    </div>

    <div class="caseForCharacter" style="left: 190px; top: 373px;">

    </div>

    <div class="caseForCharacter" style="left: 138px; top: 343px;">

    </div>
    <!-- ---- -->



    <!--
    <div class="caseContainer" style="bottom: 55px; left: 350px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 80px; left: 305px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 105px; left: 260px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 130px; left: 215px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 155px; left: 170px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 180px; left: 125px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 205px; left: 80px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>


    <div class="caseContainer" style="bottom: 55px; left: 350px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 80px; left: 305px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 105px; left: 260px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 130px; left: 215px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 155px; left: 170px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 180px; left: 125px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>

    <div class="caseContainer" style="bottom: 205px; left: 80px;">
      <div class="priceContainer">
        <div class="forCharacterPosition">

        </div>
      </div>
    </div>
    -->

    <Character :x="cases[0].x" :y="cases[0].y-22"/>
  </div>
</template>

<script>
import Character from "@/components/Character";

export default {
  name: "grid-component",
  components: {
    Character
  },
  data(){
    return{
      position: {
        x: 0,
        y: 0
      },
      cases: [
        { id: 0, y: 523, x: 450 },
        { id: 1, y: 493, x: 398 },
        { id: 2, y: 463, x: 346 },
        { id: 3, y: 433, x: 294 },
        { id: 4, y: 403, x: 242 },
        { id: 5, y: 373, x: 190 },
        { id: 6, y: 343, x: 138 },
        { id: 7, y: 224, x: 84 },
        { id: 8, y: 256, x: 96 },
        { id: 9, y: 288, x: 108 },
        { id: 10, x: 320, y: 120 },
        { id: 11, x: 138, y: 343 },
        { id: 12, x: 0, y: 0 },
        { id: 13, x: 0, y: 0 },
        { id: 14, x: 0, y: 0 },
        { id: 15, x: 0, y: 0 },
        { id: 16, x: 0, y: 0 },
        { id: 17, x: 0, y: 0 },
        { id: 18, x: 0, y: 0 },
        { id: 19, x: 0, y: 0 },
        { id: 20, x: 0, y: 0 },
        { id: 21, x: 0, y: 0 },
        { id: 22, x: 0, y: 0 },
        { id: 23, x: 0, y: 0 },
        { id: 24, x: 0, y: 0 },
        { id: 25, x: 0, y: 0 },
        { id: 26, x: 0, y: 0 },
        { id: 27, x: 0, y: 0 },
        { id: 28, x: 0, y: 0 },
        { id: 29, x: 0, y: 0 },
        { id: 30, x: 0, y: 0 },
        { id: 31, x: 0, y: 0 },
      ],
    }
  }
}
</script>

<style scoped>
.grid {
  height: 608px;
  width: 1061px;

  position: relative;

  display: flex;
  justify-content: center;

  background-color: blue;
}

.gridImage{
  width: 608px;
  height: 100%;

  background-image: url("../assets/grid.png");
  background-size: contain;
  background-repeat: no-repeat;

  transform: matrix(0.87, 0.5, -0.87, 0.5, 0, 0);
}

@media(max-width: 1630px)
{
  .grid{
    height: calc(608px*2/3);/*500px;*/
    width: calc(1061px*2/3);/*800px;*/
  }

  .gridImage{
    width: calc(608px*2/3);
  }


}

.caseForCharacter{
  width: 13px;
  height: 13px;

  position: absolute;

  transform: matrix(0.87, 0.5, -0.87, 0.5, 0, 0);

  background-color: yellow;
}

/*
.caseContainer{
  position: absolute;

  width: 50px;
  height: 75px;

  transform: matrix(0.87, 0.5, -0.87, 0.5, 0, 0);

  background-color: #BFAD97;
}

.priceContainer{
  position: absolute;

  bottom: 0;

  width: 100%;
  height: calc(100%/3);

  background-color: white;
}

.forCharacterPosition{
  width: 10px;
  height: 4px;

  position: absolute;

  left: 29px;
  bottom: 25px;

  background-color: black;
}
*/

</style>
