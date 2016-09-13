<template>
  <div class="hello">
    <p><font size="8">{{ scorea }}</font></p>
    <button @click="plusonea()">+1</button>
    <button @click="plustwoa()">+2</button>
    <button @click="plusthreea()">+3</button>
    <button @click="minusonea()">-1</button>
  </div>
</template>

<script>
export default {
  props: ['scorea', 'plusonea', 'plustwoa', 'plusthreea', 'minusonea'],
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
