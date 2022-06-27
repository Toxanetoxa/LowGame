<template>
  <div id="app" class="app">
    <section class="container">
      <div class="container-head"></div>
      <div class="container-body">
        <game-frame/>
      </div>
      <div class="container-footer">
        <g-button :value="'reset'"/>
      </div>
    </section>
  </div>
</template>

<script>
import GameFrame from "@/components/GameFrame/gameFrame";
import GButton from "@/components/ui/g-button";
export default {
  name: 'App',
  components: {
    GButton,
    GameFrame
  }
}
</script>

<style lang="scss">
@import "./assets/css/app";

.app {
  display: flex;
  align-items: center;
  width: 100%;
  height: 100vh;
  background: $color_main_white;

  .container {
    position: relative;
    width: 80%;
    margin: 0 auto;
    height: 80%;
    background: $color_bg_game_frame;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    gap: 10px;

    &-head,
    &-footer {
      height: 10%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    &-body {
      height: calc(80% - 20px);
      display: flex;
      justify-content: center;
      align-items: center;
    }


    &-head,
    &-body,
    &-footer {
      border-bottom: 1px solid $color-main_white;
    }
  }
}
</style>
