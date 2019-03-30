<template> 
  <div id="app">
    <ImageComponent/>
    <HelloWorld/>
    <p v-if="visibleif"> Teste do V-if</p>
    <p v-show="visibleshow"> Teste do V-show </p>
    <h3> Digite Seu texto:
    <input type="text" placeholder="Nome aqui" v-model="msg">
    <button v-on:click="mostre"> Ok </button>
    <button v-on:click="texto_oculto">Mostre o Texto </button>
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
      msg: '',
      visibleif: false,
      visibleshow: false,
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
    texto_oculto: function(){
      this.visibleif = true;
      this.visibleshow = true;
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
