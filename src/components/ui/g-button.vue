<template>
  <button class="btn">{{ value }}</button>
</template>

<script>
export default {
  name: 'g-button',
  props: {
    value: {
      type: String,
      default: ''
    }
  },
  data() {
    return {}
  }
}
</script>

<style scoped lang="scss">
.btn {
  cursor: pointer;
  padding: 0;
  border-radius: 10px;
  height: 34px;
  font-size: 18px;
  color: white;
  background: blue;
  width: 100px;

  &:hover {
    font-size: 20px;
    background: teal;
  }
}
</style>
