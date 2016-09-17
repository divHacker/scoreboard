<template>
  <div id="app">
    <score-board :score-info="scores.home" :update-score="updateHomeScore"></score-board>
    <score-board :score-info="scores.away" :update-score="updateAwayScore"></score-board>
  </div>
</template>

<script>
import ScoreBoard from './components/ScoreBoard'

export default {
  data () {
    return {
      scores: {
        home: {
          score: 0,
          name: 'Home'
        },
        away: {
          score: 0,
          name: 'Away'
        }
      }
    }
  },
  components: {
    ScoreBoard
  },
  methods: {
    updateScore: function (index, point) {
      if (this.scores[index].score > 0 || point !== -1) {
        this.scores[index].score = this.scores[index].score + point
      }
    },
    updateHomeScore: function (point) {
      this.updateScore('home', point)
    },
    updateAwayScore: function (point) {
      this.updateScore('away', point)
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
