<!-- tener varibale e importarlas(siempre usar data) -->
<script>
   export default{
      data: () => ({
         contador: 10,
      }),
   methods: {
         saludar() {
            console.log("hii");
         },
         incrementar(){
            // acceder al albjerto mediante this
            this.contador++;
         },

         restar(){
            // acceder al albjerto mediante this
            this.contador--;
         },

         resetear(){
            // acceder al albjerto mediante this
            this.contador=10;
         }
      },
   };
</script>


<template>
   <div class="container">

   <img src="./assets//logo.svg" alt="logo vue" width="125" height="125">
   <small>
      <h1>Hola desde VUE</h1>

   </small>

   <hr />
   <h2>Contador: {{ contador }}</h2>
   <!-- <button v-on:click="saludar">Alo por consola</button> -->
   <button @click="saludar">Hola por consola</button>

   <button @click="incrementar">+1</button>
   <button @click="restar">-1</button>
   <button @click="resetear">Reset</button>
      
</div>
</template>

<style scoped>

/* importar estilos manera de vue */
/* @import ".assets/base.css"; */

/* scoped solo aplica estilos solo para este archivo */

.container{
   text-align: center;
   /* background-color: #ddd; */
}
 h1{
   font-weight: bolder;
   /* color:red */
 }


 small{
   color:999;
 }


 h2{
   font-size: 2.5rem;;
 }


 button{
   cursor: pointer;
   font-size: 1.5rem;
   margin : 0px 6px ;
 }
</style>