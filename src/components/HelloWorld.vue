<template>
  <div v-bind:style={background:color}>
    <h3>{{ catMessage }}</h3>
    <div>
      <button v-on:click="incrementCounter">Increment the cuteness meter</button>
    </div>
    <div :class="{yell : shouldYell}">{{catName + '\'s'}} cuteness meter is at {{clickCount}} </div>
    <a v-bind:href="vueLink"> here's a link to the vue documentation </a>
  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    // props passed in from parent component
    catName: String,
    subMsg: String,
    vueLink: String,
  },
  data: function () {
    return {
      // initial data values
      clickCount: 0,
      shouldYell: false,
      color: 'aqua'
    }
  },
  methods: {
    incrementCounter: function () {
        this.clickCount += 1
        if(this.clickCount >= 10){
          this.shouldYell = true
        }
        this.color == 'red' ? this.color = 'aqua' : this.color = 'red'
    }
  }, 
  computed: {
    catMessage() {
      return this.catName + ' ' + this.subMsg
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
.background {
  background-color:aqua
}
.yell {
  font-size: 25px;
  font-weight: bolder;
}
</style>
