<template>
  <Grid/>
  <PlayerCard
      ref="player1"
      :top="0"
      :left="0"
      :color="players[0].color"
      :is-turn="players[0].isTurn"
      :time-for-turn="players[0].timeForTurn"
      :score="players[0].score"
      :picture-path="'assets/profile/mustache.jpg'"
      @player-tour-ended="startPlayerCardTimer"/>
  <PlayerCard
      ref="player2"
      :top="0"
      :right="0"
      :color="players[1].color"
      :is-turn="players[1].isTurn"
      :time-for-turn="players[1].timeForTurn"
      :score="players[1].score"
      :picture-path="'assets/profile/smile.jpg'"
      @player-tour-ended="startPlayerCardTimer"/>
  <PlayerCard
      ref="player3"
      :bottom="0"
      :right="0"
      :color="players[2].color"
      :is-turn="players[2].isTurn"
      :time-for-turn="players[2].timeForTurn"
      :score="players[2].score"
      :picture-path="'assets/profile/wind.jpg'"
      @player-tour-ended="startPlayerCardTimer"/>
  <PlayerCard
      ref="player4"
      :bottom="0"
      :left="0"
      :color="players[3].color"
      :is-turn="players[3].isTurn"
      :time-for-turn="players[3].timeForTurn"
      :score="players[3].score"
      :picture-path="'assets/profile/wow.jpg'"
      @player-tour-ended="startPlayerCardTimer"/>
</template>

<script>
import Grid from "@/components/Grid";
import PlayerCard from "@/components/PlayerCard";

export default {
  name: 'App',
  components: {
    PlayerCard,
    Grid
  },
  data()
  {
    return {
      players : [
        { player:this.$refs.player1, score: 1000000, timeForTurn: 1000, isTurn: true,  color: '#32B667' },
        { player:this.$refs.player2, score: 1000000, timeForTurn: 2000, isTurn: false, color: '#FF3838' },
        { player:this.$refs.player3, score: 1000000, timeForTurn: 1000, isTurn: false, color: '#38A0FF' },
        { player:this.$refs.player4, score: 1000000, timeForTurn: 2000, isTurn: false, color: '#FF9838' },
      ],
      currentPlayer : 1,
    }
  },
  methods: {
    startPlayerCardTimer()
    {
      this.currentPlayer = this.currentPlayer % 4 + 1;

      // Change de joueur s'il est encore dans le jeu
      if(this.players[this.currentPlayer-1].score > 0)
      {
        this.players[this.currentPlayer-1].player.activeTimer();
        this.players[this.currentPlayer-1].player.startTimer();
      }
      else{
        this.startPlayerCardTimer();
      }
    }
  },
  mounted()
  {
    this.players[0].player = this.$refs.player1;
    this.players[1].player = this.$refs.player2;
    this.players[2].player = this.$refs.player3;
    this.players[3].player = this.$refs.player4;
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
  height: 100vh;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;

  background-color: #A1DDFF;
}
</style>
