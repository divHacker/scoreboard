<template>
  <div id="app">
    <hscore :scoreh="scoreh" :plusoneh="plusoneh" :plustwoh="plustwoh" :plusthreeh="plusthreeh" :minusoneh="minusoneh"></hscore>
    <ascore :scorea="scorea" :plusonea="plusonea" :plustwoa="plustwoa" :plusthreea="plusthreea" :minusonea="minusonea"></ascore>
  </div>
</template>

<script>
import Hscore from './components/Hscore'
import Ascore from './components/Ascore'
export default {
  data () {
    return {
      scoreh: 0,
      scorea: 2
    }
  },
  components: {
    Hscore,
    Ascore
  },
  methods: {
    plusoneh: function () {
      this.scoreh = this.scoreh + 1
    },
    plusonea: function () {
      this.scorea = this.scorea + 1
    },
    plustwoh: function () {
      this.scoreh = this.scoreh + 2
    },
    plustwoa: function () {
      this.scorea = this.scorea + 2
    },
    plusthreeh: function () {
      this.scoreh = this.scoreh + 3
    },
    plusthreea: function () {
      this.scorea = this.scorea + 3
    },
    minusoneh: function () {
      if (this.scoreh <= 0) {
        this.scoreh = 0
      } else {
        this.scoreh = this.scoreh - 1
      }
    },
    minusonea: function () {
      if (this.scorea <= 0) {
        this.scorea = 0
      } else {
        this.scorea = this.scorea - 1
      }
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
