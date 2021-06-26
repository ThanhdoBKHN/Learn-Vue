<template>
  <div style="background-color:#eee; height:200px;width:350px;float:left;" id="left">
    <h1>Information User Details</h1>
    <p>List Details: </p>
    <p>My Name: {{ name }} </p>
    <p>My Age: {{ age }}</p>
    <button @click="resetName">ResetName</button>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    age: Number,
  },
  name: 'Frame1',
  methods: {
    resetName: function () {
      this.name = 'Do Van Thanh'
      this.$emit('nameReseted', this.name)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#left {
  margin: 35px;
}

</style>

