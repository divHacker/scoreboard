<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <modscore :scorea="scorea" :plusonea="plusonea" :plustwoa="plustwoa" :plusthreea="plusthreea" :minusonea="minusonea"></modscore>
  </div>
</template>

<script>
import Modscore from './Modscorea'
export default {
  props: ['scorea', 'plusonea', 'plustwoa', 'plusthreea', 'minusonea'],
  data () {
    return {
      msg: 'Away'
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
