<template>
  <div class="hello">
    <h1>{{ scoreInfo.name }}</h1>
    <h1>{{ scoreInfo.score }}</h1>
    <controller :score="scoreInfo.score" :update-score="updateScore"></controller>
  </div>
</template>

<script>
import Controller from './Controller'
export default {
  props: ['scoreInfo', 'updateScore'],
  data () {
    return {
    }
  },
  components: {
    Controller
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
.hello {
  float: left;
  margin: 30px;
}
</style>
