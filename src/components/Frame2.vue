<template>
  <!-- <div class="hello"> -->
  <div style="background-color:#aaa; height:200px;width:350px;float:right;" id="right">
    <h1>You may edit the</h1>
    <h1>User here</h1>
    <p>Edit me!</p>
    <button @click="addAge">Add Age</button>
    <button @click="subAge">Sub Age</button>
  </div>
</template>

<script>
export default {
  name: 'Frame2',
  props: ['age'],
  methods: {
    addAge: function() {
      this.age += 1
      this.$emit('ageAdd', this.age)
    },
    subAge: function() {
       this.age -= 1
       this.$emit('ageSub', this.age)
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#right {
  margin: 35px;
}

</style>
