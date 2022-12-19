<template>
  <TheHeader v-if="showHeader" />
  <div v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>
  <br>
  <br>
  <br>
  <div v-if="accessLevel === 'admin'">Usuário: Admin</div>
  <div v-else-if="accessLevel === 'marketing'">Usuário: Marketing</div>
  <div v-else>Usuário: Normal</div>
  <br>
  <br>
  <br>
  <div>
    <div v-for="(obj, index) in todos" 
         v-bind:key="obj.id"
         class="todos-item">
        {{ index }}  {{ obj.title }}
    </div>
  </div>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TheHeader from './components/TheHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TheHeader
  },

  data() {
    return {
      showHeader: true,
      firstName: 'Jhon',
      lastName: 'Snow',
      showName: false,
      accessLevel: 'admin',

      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
    }
  }
}
</script>

<style>
.todos-item {
    background: blueviolet;
    color: #fff;
    margin: 0 0 3px 0;
    padding: 3px 6px;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

}
</style>
