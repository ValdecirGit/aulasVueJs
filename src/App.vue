<template>
  <TheHeader v-if="showHeader" />

  <h1 v-bind:class="classVar">
    Valdecir testando classe  style com v-bind
  </h1>
  <h2 v-bind:class="{'title2': true, 'title-home': isHome}">
    VUE 3
  </h2>

  <p v-bind:class="pClass">
    orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
  </p>

  <p v-bind:style="styleClass">

    orem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
  </p>

  
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
        <img  v-if="obj.imagemSrc"
              v-bind:src="obj.imagemSrc" />
    </div>
  </div>

  
  <img v-bind:src="imagemSrc" v-bind:alt="imgAlt" />

  <img alt="Vue logo" src="./assets/logo.png"/> 
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
      pClass: ['text', 'text-home'] ,
      styleClass: {color: 'green', backgroundColor: 'black', 'font-size': '30px'},
      isHome: true,
      classVar: 'title',
      imgAlt: 'foto de Jhon SNow',
      imagemSrc: 'https://via.placeholder.com/150',
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
          "completed": false,
          "imagemSrc": 'https://via.placeholder.com/150'
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imagemSrc": 'https://via.placeholder.com/150'
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

.text-home {
  color:blue;
}
.text {
  size: 80;
}
.title {
  size: 20;
  color:blue;
}

.title2 {
  size: 20;
  color:red;
}

.title-home {
  size: 50;
  color:chartreuse
}
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
