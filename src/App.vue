<template>

<div>
  <h1>{{ heading }}</h1>
  <button @click="toggleModal">Play</button>
</div>

  <div v-if="showModal">
    <Block class="modal" @close="toggleModal" >
      
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
      showModal: false
    }
  },

  methods: {
    toggleModal() {
      this.showModal = !this.showModal
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

</style>
