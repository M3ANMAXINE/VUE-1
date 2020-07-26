<template>
  <div>
    


      
    <input type="text" v-model="valor" class="form-control">
    <button class="btn btn-primary" v-on:click="crearTarea()">Crear</button>

    <H2>TAREAS</H2>

    <ul v-for="(tarea,index) in lista" :key="index"> 
        <li > {{ index }} {{' ' + tarea }}     <button class="btn btn-primary" v-on:click="eliminar(index)">Eliminar</button>
  </li>        
    </ul>




  </div>
</template>

<script>
export default {

  name: "tareas",
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
            
    eliminar () {

      this.lista.splice(this.index,1);
     
    }
}};


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
