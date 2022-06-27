<template>
  <div class="game">
    <games-cell
        class="game-cell"
        v-for="x in 9"
        @game-step="detectedPlayer"
        :player1="players1"
        :reset="reset"
    />
  </div>
</template>

<script>
import GamesCell from "@/components/GameFrame/gamesCell";
import GButton from "@/components/ui/g-button";
export default {
  name: 'gameFrame',
  components: {GButton, GamesCell},
  data() {
    return {
      players1: true,
      reset: false,
    }
  },
  methods: {
    detectedPlayer() {
      this.players1 = !this.players1
      console.log(this.players1)
    },
    resetGame() {

    }
  }
}
</script>

<style scoped lang="scss">
.game {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
  width: 80%;
  height: 80%;
  border-radius: 10px;
  overflow: hidden;

  &-cell {
    display: flex;
    border-radius: 10px;
    border: 1px solid black;
   }
}

</style>
