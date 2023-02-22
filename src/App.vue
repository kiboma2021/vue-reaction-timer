<template>

<div>
  <h1>{{ heading }}</h1>
  <button @click="startPlaying" :disabled="isPlaying" :class="{deactbtn: isPlaying}" >Play</button>
</div>

<h1 v-if="score">Result is {{ this.score }} ms</h1>

  <div v-if="isPlaying">
    <Block class="modal" :delay="delay" @end="endGame">
      
    </Block>
  </div>

</template>

<script>
import Block from './components/Block.vue'

export default {
  name: 'App',
  components: {Block},

  data() {
    return {
      heading: "Welcome to Reaction Timer Game ...",
      isPlaying: false,
      delay:null,
      score:null,
    }
  },

  methods: {
    startPlaying() {
      this.delay= 2000 + Math.random()*5000
      this.isPlaying = true
      this.score = null
    },
    endGame(myReactionTime){
      this.score= myReactionTime
      this.isPlaying = false
    }

  }
}

</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}

button {
  background-color: greenyellow;
  color: black;
  font-weight: bold;
  border: none;
  border-radius: 10px;
  width: 8rem;
  padding: 1rem;
}

.deactbtn {
  background-color: grey;
}

</style>
