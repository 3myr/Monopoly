<template>
  <Grid/>
  <PlayerCard :x="0" :y="0"/>
  <PlayerCard :x="1000" :y="0"/>
  <PlayerCard :x="0" :y="800"/>
  <PlayerCard :x="1000" :y="800"/>
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
