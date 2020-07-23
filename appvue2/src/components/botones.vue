<template>


<div>

    <h1>{{val}}</h1>

      <ul>
          <li v-for="(numero,index) in numeros" :key="index"> 
     <button class="btn btn-primary" @click="add(numero.text)">{{numero.bot}}</button>

          </li>
      </ul>


                       
</div>
</template>

<script>
export default {
  name: 'boton',
 data() {
     return{
         numeros:[{bot:"3s",text:"00:03 min/seg "}, {bot:"1m",text: "01:00 min/seg"}, {bot:"5m",text: "05:00 min/seg"}, {bot:"10m",text: "10:00 min/seg"}, {bot:"30m",text: "30:00 min/seg"},{bot:"clear",text:""}],
         val: "",
         
         
     }
 },
 methods: {
     add(text) {
     this.val = text 
 }
    

  }};

</script>

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
button{
    padding-left: 5px;
}
</style>
