<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" v-model="message">
    <button v-on:click="$emit('myEvent')">CheckEmit</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },

  data(){
    return{
      message: "Hello Message"  
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
