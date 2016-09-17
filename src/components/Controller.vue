<template>
  <div class="hello">
    <button @click="updateScore(1)">+1</button>
    <button @click="updateScore(2)">+2</button>
    <button @click="updateScore(3)">+3</button>
    <button :disabled="!score" @click="updateScore(-1)">-1</button>
  </div>
</template>

<script>
export default {
  props: ['score', 'updateScore'],
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>
