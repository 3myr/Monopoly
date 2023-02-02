<template>
  <div class="character" :style="{ left: position.x + 'px', top: position.y + 'px' }"></div>
</template>

<script>
export default {
  name: "character-component",
    props: {
      x: {
        type: Number,
        default : 0
      },
      y: {
        type: Number,
        default : 0
      }
    },
    data() {
      return {
        position: {
          x: this.x,
          y: this.y,
        },
        xShift: 52,
        yShift: 30,
      };
    },
    mounted() {
      document.addEventListener("keydown", (event) => {
        if (event.keyCode === 37) {
          // fleche gauche
          this.position.x -= this.xShift; // 32
          this.position.y += this.yShift; // 12
        } else if (event.keyCode === 38) {
          // fleche haut
          this.position.x -= this.xShift;
          this.position.y -= this.yShift;
        } else if (event.keyCode === 39) {
          // fleche droite
          this.position.x += this.xShift;
          this.position.y -= this.yShift;
        } else if (event.keyCode === 40) {
          // fleche bas
          this.position.x += this.xShift;
          this.position.y += this.yShift;
        }
      });
    }
}
</script>

<style scoped>
.character {
  width: 32px;
  height: 32px;
  position: absolute;
  background-color: red;
}
</style>
