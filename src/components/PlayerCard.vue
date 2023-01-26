<template>
  <div class="card" :style="{ left : x + 'px', top: y + 'px'}"></div>
</template>

<script>
export default {
  name: "player-card",
  props: {
    x: {
      type: Number
    },
    y: {
      type: Number
    }
  }
}
</script>

<style scoped>
.card{
  width: 300px;
  height: 100px;

  position: absolute;

  background-color: green;
}
</style>
