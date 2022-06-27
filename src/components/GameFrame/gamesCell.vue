<template>
  <div
      class="cell"
      @click="takeValue"
  >
    {{ value }}
  </div>
</template>

<script>
export default {
  name: 'gamesCell',
  props: {
    player1: {
      type: Boolean,
      required: true,
    },
    reset: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      value: '',
    }
  },
  methods: {
    takeValue() {
      this.value = this.player1? 'X' : 'O'
      this.resetValue()
      this.$emit('game-step')
    },
    resetValue() {
  if(this.reset === true){
    return this.value = ''
  }
  return null
}
  },
  computed() {
  }
}
</script>

<style lang="scss">
.cell {
  cursor: pointer;
  background: white;
  justify-content: center;
  align-items: center;
  font-size: 60px;
  font-weight: 600;
  -moz-user-select: -moz-none;
  -o-user-select: none;
  -khtml-user-select: none;
  -webkit-user-select: none;
  user-select: none;

  &:hover {
    background: gainsboro;
  }
}

.red {
  background: red;
}

.blue {
  background: blue;
}
</style>
