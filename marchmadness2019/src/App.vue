<template>
  <div id="app">
    <appBaseHeader></appBaseHeader>
    <appBracket></appBracket>
    
  </div>
</template>

<script>
import BaseHeader from './components/header.vue';
import Bracket from './components/bracket.vue';

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      header:'',
      shown: false,
    }
  },
  methods:{
    change: function() {
      this.shown = !this.shown;
      if(this.shown){
        this.header = "HEADER";
      }
      else{
        this.header = "";
      }
      
    }
  },
  components: {
    appBaseHeader: BaseHeader,
    appBracket: Bracket,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
  width: 1070px;
  padding-top: 10px;
  margin: 0 auto;
  }
</style>
