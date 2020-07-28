<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

       
    <H2>TAREAS</H2>

    <input type="text" v-model="valor" class="form-control">
    <button class="btn btn-primary" v-on:click="crearTarea()">Crear</button>

    <tareas :lista="lista"    @id="eliminarx" />
  </div>
</template>

<script>
import tareas from './components/tarefas.vue'

export default {
  name: 'App',
  components: {
    tareas,
  },
  data() {
    return {
      lista: [],
      valor: "",
         };
   },
    methods: {
    crearTarea() {
      if(this.valor !=="")  
    this.lista.push(this.valor);
    this.valor = "";
    },
            
    eliminarx(index) {

      this.lista.splice(index, 1);
     
    }
   }}



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
</style>
