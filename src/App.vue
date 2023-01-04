<template>
  <div>
    <the-header v-if="showHeader"/>
    <h1>Elemento Raiz do DOM</h1>
    {{name}} 
    <br>
    <br>
    <button @click="showHeader = !showHeader">
      Ativar e desativar Header</button>
    <br>
    <br>
    <input v-model="name" type="text" />

</div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';

export default {
  name: "App",

  data() {
    return {
      name: "Valdecir RML",
      showHeader: false
    }
  },


// // mais usado para DEBUG  
// //antes da atualizacao do componente
// beforeUpdate() {
//   console.log('beforeUpdate', this.name);
// },

// // mais usado para DEBUG  
// //Atualizacao do componente
// updated() {
//   console.log('update', this.name);
// },

  // //antes do componente ser criado
  // beforeCreate(){
  //   console.log('beforeCreate');
  //   console.log('estado:', this.name);
  //   console.log('DOM:', this.$el);
  // },

  // //componente foi criado
  // created(){
  //   console.log('created');
  //   console.log('estado:', this.name);
  //   console.log('DOM:', this.$el);
  // },

  // //antes do componente ser montado
  // beforeMount(){
  //   console.log('beforeMount');
  //   console.log('estado:', this.name);
  //   console.log('DOM:', this.$el);
  // },
  // // componente foi montado
  // mounted(){
  //   console.log('mounted');
  //   console.log('estado:', this.name);
  //   console.log('DOM:', this.$el);
  // },
  // //antes do componente ser desmontado
  // beforeUnmount(){
  //   console.log('beforeUnmount');
  // },

  // // componente desmontado</h5>
  // unmounted(){
  //   console.log('unmounted');
  // },

  components: {
    TheHeader
    

  },

  watch: {
    
  },

  computed: {

  },

  methods: {
    
  },
};
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
