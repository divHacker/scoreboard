<template>
  <div class="hello">
    <p><font size="8">{{ scoreh }}</font></p>
    <button @click="plusoneh()">+1</button>
    <button @click="plustwoh()">+2</button>
    <button @click="plusthreeh()">+3</button>
    <button @click="minusoneh()">-1</button>
  </div>
</template>

<script>
export default {
  props: ['scoreh', 'plusoneh', 'plustwoh', 'plusthreeh', 'minusoneh'],
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
