<template>
  <div id="app">
    <img alt="cat photo" src="./assets/lewie.jpg" />
    <HelloWorld 
      msg="Trying out a Vue app" 
      subMsg="adding a prop"
      v-bind:vueLink="vueLink"
    />
    <!-- <a v-bind:href="vueLink" > here is a link to vue </a> -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data: function () {
    return {
      vueLink: "https://vuejs.org/v2/guide/index.html"
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

img {
  height: 200px;
}
</style>
