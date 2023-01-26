<template>
  <div class="playerCardContainer" :style="cardStyle">
    <!-- Header -->
    <div class="headerContainer" :style="headerStyle">
      <div class="headerNameContainer" :style="headerNameStyle">
        <p class="headerName">
          EmyLePur
        </p>
      </div>
    </div>

    <!-- Content Game -->
    <div class="infoContainer" :style="infoStyle">
      <div class="cashContainer" :style="cashStyle">
        <div class="cash">
          <p class="cashText">1 825 000</p>
          <div class="cashIcon">

          </div>
        </div>

        <!-- Temps restant pour le joueur, caché par défaut -->
        <div class="time">

        </div>
      </div>
    </div>

    <!-- Photo -->
    <div>
      <div class="pictureContainer" :style="pictureStyle">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "player-card",
  props: {
    left: {
      type: Number
    },
    right: {
      type: Number
    }
    ,
    top: {
      type: Number
    },
    bottom: {
      type: Number
    },
    color: {
      type: String
    }
  },
  data() {
    return {
      headerHeight: 38,
      pictureMargin: 4,
      headerNameMargin: 14, /* TODO A Modifier */
    }
  },
  computed: {
    cardStyle() {
      return {
        left: this.left !== null ? this.left + 'px' : '',
        right: this.right !== null ? this.right + 'px' : '',
        top: this.top !== null ? this.top + 'px' : '',
        bottom: this.bottom !== null ? this.bottom + 'px' : '',
      }
    },
    pictureStyle() {
      return {
        left: this.left !== null ? (this.left + this.pictureMargin) + 'px' : '',
        right: this.right !== null ? (this.right + this.pictureMargin) + 'px' : '',
        top: this.bottom !== null ? this.bottom + 'px' : '',
        bottom: this.top !== null ? this.top + 'px' : '',
      }
    },
    headerStyle() {
      let borderRadiusCalculated = '';
      if (typeof this.top !== 'undefined' && typeof this.left !== 'undefined') {
        borderRadiusCalculated = "0 5px 5px 0";
      } else {
        if (typeof this.top !== 'undefined' && typeof this.right !== 'undefined') {
          borderRadiusCalculated = "5px 0 0 5px";
        } else {
          if (typeof this.bottom !== 'undefined' && typeof this.right !== 'undefined') {
            borderRadiusCalculated = "5px 0 0 5px";
          } else {
            if (typeof this.bottom !== 'undefined' && typeof this.left !== 'undefined') {
              borderRadiusCalculated = "0 5px 5px 0";
            }
          }
        }
      }
      return {
        top: this.top !== null ? this.top + 'px' : '',
        bottom: this.bottom !== null ? this.bottom + 'px' : '',
        height: this.headerHeight + 'px',
        backgroundColor: this.color,
        borderRadius: borderRadiusCalculated,
      }
    },
    infoStyle() {
      let borderRadiusCalculated = '';
      let borderStrokeCalculated = '';
      if (typeof this.top !== 'undefined' && typeof this.left !== 'undefined') {
        borderRadiusCalculated = "0 0 10px 0";
        borderStrokeCalculated = "0 3px 3px 0";
      } else {
        if (typeof this.top !== 'undefined' && typeof this.right !== 'undefined') {
          borderRadiusCalculated = "0 0 0 10px";
          borderStrokeCalculated = "0 0 3px 3px";
        } else {
          if (typeof this.bottom !== 'undefined' && typeof this.right !== 'undefined') {
            borderRadiusCalculated = "10px 0 0 0";
            borderStrokeCalculated = "3px 0 0 3px";
          } else {
            if (typeof this.bottom !== 'undefined' && typeof this.left !== 'undefined') {
              borderRadiusCalculated = "0 10px 0 0";
              borderStrokeCalculated = "3px 3px 0 0";
            }
          }
        }
      }

      return {
        top: this.top !== null ? (this.top + this.headerHeight) + 'px' : '',
        bottom: this.bottom !== null ? (this.bottom + this.headerHeight) + 'px' : '',
        left: this.left !== null ? this.left + 'px' : '',
        right: this.right !== null ? this.right + 'px' : '',
        borderRadius: borderRadiusCalculated,
        borderStyle: "solid ",
        borderWidth: borderStrokeCalculated,
        borderColor: this.color,
      }
    },
    cashStyle()
    {
      return {
        left: this.right !== null ? this.right + 'px' : '',
        right: this.left !== null ? this.left + 'px' : '',
      }
    },
    headerNameStyle() {
      return {
        left: this.right !== null ? (this.right + this.headerNameMargin) + 'px' : '',
        right: this.left !== null ? (this.left + this.headerNameMargin) + 'px' : '',
      }
    }
  }
}
</script>

<style scoped>
/* Container */
.playerCardContainer {
  width: 280px; /* Largeur par défaut */
  height: 104px; /* Hauteur par défaut */

  position: absolute;

  display: flex;
  flex-direction: column;
}

.playerCardContainer * {
  margin-block-start: 0;
  margin-block-end: 0;
}

/*        */

/* Header */
.headerContainer {
  width: 100%;
  height: 38px; /* Hauteur par défaut */

  position: absolute;

  background-color: #32B667; /* Couleur par défault */
}

.headerNameContainer{
  width: 62%; /* TODO A Modifier */
  height: 100%;

  position: absolute;

  display: flex;
  justify-content: center;
  align-items: center;

  #background-color: yellow;
}

.headerContainer .headerName {

  text-overflow: ellipsis;
  font-family: "Arial Black";
  font-size: 24px;

  color: white;
  font-weight: bold;
  text-transform: uppercase;

  #background-color: blue;
}

/*        */

/* Info   */
.infoContainer {
  width: 95%;
  height: 57px; /* Hauteur par défaut */

  position: absolute;

  background-color: #FFF2E5;
}

.cashContainer{
  height: 90%; /* TODO A revoir ? */
  width: 65%; /* TODO A Modifier par widthInfoContainer - pictureMargin + widthPicture*/

  position: absolute;

  display: flex;
  flex-direction: column;

  justify-content: center;
  align-items: center;
  gap: 5px;

  #background-color: yellow;
}

.cash{
  display: flex;
  flex-direction: row;

  justify-content: center;
  align-items: center;
}

.cashText{
  font-size: 20px;
}

/* TODO Revoir la disposition du billet */
.cashIcon{
  height: 20px;
  width: 20px;

  background-color: white;
  margin-left: 5px;
}

.time{
  width: 90%;
  height: 5px;

  background-color: red;
}
/*        */

/* Picture */
.pictureContainer {
  width: 90px;
  height: 90px; /* Hauteur par défaut */

  border-radius: 10px;

  position: absolute;

  background-color: white;
}

/*         */
</style>
