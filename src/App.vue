<template>
  <Grid/>
  <PlayerCard :top="0" :left="0" :color="'#32B667'"/>
  <PlayerCard :top="0" :right="0" :color="'#FF3838'"/>
  <PlayerCard :bottom="0" :left="0" :color="'#FF9838'"/>
  <PlayerCard :bottom="0" :right="0" :color="'#38A0FF'"/>
</template>

<script>
import Grid from "@/components/Grid";
import PlayerCard from "@/components/PlayerCard";

export default {
  name: 'App',
  components: {
    PlayerCard,
    Grid
  }
}
</script>

<style>
body {
  margin: 0;

  overflow: hidden;
}

#app{
  width: 100%;
  height: 100%;

  position: relative;
}
</style>
