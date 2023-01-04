<template>
  <div>
    <h2>Observadores</h2>
    <br />
    <br />
    Name:
    <input v-model="name" type="text"/>
    <br />
    {{name}}
    <br />
    <br />
    Nome:
    <input v-model="user.first_name" type="text"/>
    <br />
    <br />
    Sobre:
    <input v-model="user.last_name" type="text"/>
    <br />
    {{user.first_name}} {{user.last_name}}
    <br />
    <select v-model="pageCount">
      <option value="5">5</option>
      <option value="10">10</option>
      <option value="15">15</option>
    </select>
    <br />
    {{pageCount}}
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      name: '',
      pageCount: '5',
      user: {
        first_name: '',
        last_name: '',
      }
    }
  },

  components: {

  },

  watch: {
    name(vlr){
      // só executa rotina que valor tiver 3 ou mais caracteres
      if (vlr.length >= 3) {
      this.saveUserName();
      }
    },
        pageCount(){
      this.changePage();  
    },

    /* funçãoooooooooooooooooo
    user(){
     console.log('usuario alterado')
    } */

    // objetoooooooooooooooo
    user: {
       handler(){
        console.log('usuario alterado disparo handler')
       },
       deep: true
    }
  },

  computed: {

  },

  methods: {
    saveUserName(){
      console.log('ajax saveUserName');
      console.log(this.name);
    },
    changePage(){
      console.log('ajax changePage');
      console.log(this.pageCount);
    }
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
