<template>
  <div>
    <button @click.once="onClick">
      Enviar
    </button>
  </div>
  <br>
  <br>
  <div @mouseover="onMouseOver"
       @mouseout="onMouseOut">
    MouseOver e MouseOut
  </div>

  <br>
  <br>

  <form action="https:/google.com"
        @submit.prevent="onSubmit">

        <input type="text"
         @keyup.enter="onKeyUp">

         
     <button type="submit">
          Executar
     </button>
  </form>  

  <br>
  <br>

  
</template>

<script>

export default {
  name: 'App',

  data() {
    return {

    }
  },

  methods: {
    onClick($evt) {
      console.log('clicou no botao', $evt);
    },

    onMouseOver($evt){
      console.log('passou mouse em cima', $evt);
    },

    onMouseOut($evt){
      console.log('tirou mouse de cima', $evt);
    },
    
    onSubmit($evt) {
      console.log('Submit', $evt);
    },

    onKeyUp($evt){
      console.log('onKeyUp', $evt);
    }
    

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;

}
</style>
