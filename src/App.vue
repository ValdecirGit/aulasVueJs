<template>
  <div>
    <h1>Elemento Raiz do DOM</h1>
    {{name}}
  <div>
    <h2>Cliclo de Vida (life cycle)</h2>
    <h3>Criação</h3> 
    <h5>Prepara o componente, faz ajax, inicializa variáveis. Não tem acesso ao template (DOM)</h5> 
    <h3>Montagem</h3> 
    <h5>Quando vc precisa inicializar uma lib externa (ex: new Lib()) e ela precisa de acesso ao template (DOM)
        Tem Acesso ao template (DOM)
    </h5> 
    <h3>Atualização</h3> 
    <h5>Usado para debug. Tudo o que acontece no Vue</h5> 
    <h3>Desmonstagem</h3> 
    <h5>Desmonsta o componente. Remove tudo o que for necessário para liberar memória.
        Ex. Lib->destroy()
    </h5> 
    <h3>Hooks</h3> 
    <h4>Usando para interagir em todas estas fases.</h4>
    <h5>beforeCreate(){} --> antes do componente ser criado</h5>
    <h5>created(){} ---> componente foi criado</h5>
    <h5>beforeMount(){} --->antes do componente ser montado</h5>
    <h5>mounted(){} --->componente foi montado</h5>
    <h5>beforeUnmount(){} --->antes do componente ser desmontado</h5>
    <h5>unmounted(){} --->componente desmontado</h5>
  
    <br />
    <br />
  </div>
</div>
</template>

<script>

export default {
  name: "App",

  data() {
    return {
      name: "Valdecir RML"
    }
  },

  //antes do componente ser criado
  beforeCreate(){
    console.log('beforeCreate');
    console.log('estado:', this.name);
    console.log('DOM:', this.$el);
  },

  //componente foi criado
  created(){
    console.log('created');
    console.log('estado:', this.name);
    console.log('DOM:', this.$el);
  },

  //antes do componente ser montado
  beforeMount(){
    console.log('beforeMount');
    console.log('estado:', this.name);
    console.log('DOM:', this.$el);
  },
  // componente foi montado
  mounted(){
    console.log('mounted');
    console.log('estado:', this.name);
    console.log('DOM:', this.$el);
  },
  //antes do componente ser desmontado
  beforeUnmount(){
    console.log('beforeUnmount');
  },

  // componente desmontado</h5>
  unmounted(){
    console.log('unmounted');
  },


  components: {
    

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
