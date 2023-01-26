<template>
  <div class="grid">
    <Character :x="cases[10].x" :y="cases[10].y"/>
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
        { id: 0, x: 0, y: 0 },
        { id: 1, x: 32, y: 12 },
        { id: 2, x: 64, y: 24 },
        { id: 3, x: 96, y: 36 },
        { id: 4, x: 128, y: 48 },
        { id: 5, x: 160, y: 60 },
        { id: 6, x: 192, y: 72 },
        { id: 7, x: 224, y: 84 },
        { id: 8, x: 256, y: 96 },
        { id: 9, x: 288, y: 108 },
        { id: 10, x: 320, y: 120 },
        { id: 11, x: 0, y: 0 },
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
  width: 100%;

  position: relative;

  display: flex;

  background-color: blue;
}
</style>
