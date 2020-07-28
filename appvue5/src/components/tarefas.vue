<template>
  <div>
    


   


    <ul v-for="(tarea,index) in lista" :key="index"> 

        <li > {{ index }} {{' ' + tarea }}     <button class="btn btn-primary" v-on:click="eliminar(index)">Eliminar</button></li>        
    </ul>




  </div>
</template>

<script>
export default {

  name: "tareas",
  
         props: {

          lista: Array,    
         },
         methods: {

           eliminar(index){
             console.log(index)

             this.$emit('id', index);

           }
         }
  
};


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
