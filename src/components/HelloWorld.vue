<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>{{ subMsg }}</h3>
    <a v-bind:href="vueLink"> here's a link to documentation </a>
    <div>
      <button v-on:click="incrementCounter">Test on click handler</button>
    </div>
    <div>Test button clicks {{clickCount}} </div>
  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    subMsg: String,
    vueLink: String,
  },
  data: function () {
    return {
      clickCount: 0,
    }
  },
  methods: {
    incrementCounter: function () {
        this.clickCount += 1
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
