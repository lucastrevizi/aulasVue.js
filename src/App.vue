<template> 
  <div id="app">
    <ImageComponent/>
    <HelloWorld/>
    <h3> Digite Seu texto: 
    <input type="text" placeholder="Nome aqui" v-model="msg">
    <button v-on:click="mostre"> Ok </button>
    </h3>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import ImageComponent from './components/ImageComponent'
import LabelEdit from 'label-edit'

export default {
  name: 'App',
  data () {
    return {
      msg,
    }
  },
  components: {
    LabelEdit,
    HelloWorld,
    ImageComponent
  },
  methods: {
    mostre: function(){
      alert(`Você escreveu: ${this.msg}`);
    },
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
  margin-top: 60px;
}
</style>
