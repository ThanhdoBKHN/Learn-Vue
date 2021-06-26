<template>
  <div id="app">
    <h1><b>The Parent Component</b></h1>
    <p1> {{ name }} and {{ age }}</p1>
    <br>
    <button @click="changeName">Change My Name</button>
    <Frame1 :name="name" :age="age" @nameReseted="name = $event"></Frame1>
    <Frame2 :age="age" @ageAdd="age = $event"  @ageSub="age = $event"></Frame2>
    <div style="clear:both">
    </div>
  </div>
</template>

<script>
import Frame1 from './components/Frame1.vue'
import Frame2 from './components/Frame2.vue'

export default {
  data() {
    return  {
      name: 'Do Van Thanh',
      age: 22,
    }
  },
  name: 'App',
  components: {
    Frame1,
    Frame2,
  }, 
  methods: {
    changeName() {
      this.name = "ThanhDV"
    },
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
  background-color: lightblue;
}
</style>
