<template>
  <div class="hello">
    <h1 v-bind:title="msg" v-if = "seen">Hover over me</h1>
    <h5>{{ name }}</h5>
    <button v-on:click="reverseMessage">Reverse name</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'You loaded this page on ' + new Date().toLocaleString(),
      seen: true,
      name: 'Betty Mariam Johny'
    }
  },
  methods: {
    reverseMessage: function () {
      this.name = this.name.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello
{
  background: #902378;
}
h1, h2 {
  font-weight: normal;
  color: aqua;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
