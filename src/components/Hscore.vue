<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <modscore :scoreh="scoreh" :plusoneh="plusoneh" :plustwoh="plustwoh" :plusthreeh="plusthreeh" :minusoneh="minusoneh"></modscore>
  </div>
</template>

<script>
import Modscore from './Modscoreh'
export default {
  props: ['scoreh', 'plusoneh', 'plustwoh', 'plusthreeh', 'minusoneh'],
  data () {
    return {
      msg: 'Home'
    }
  },
  components: {
    Modscore
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>
