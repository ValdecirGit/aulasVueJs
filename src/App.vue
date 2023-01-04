<template>
  <div>
    {{ user.first_name }} {{ user.last_name }} <br />
    computed properties <br />
    Propriedades Computadas
    <br /><br />

    <button @click="OnClick">captura instancia do componente</button>
    <br />
    <br />
    <br />
    <br />
    <br />
    <button @click="OnClickUser">acessa propriedades do usuario</button>

    <br />
    <br />
    <br />
    {{ fullName }}
    <br />
    <br />
    <br />
    <h2>Todos em aberto</h2>
    <div v-for="todo in uncompletedTodos" 
        :key="todo.id">
      {{ todo.title }}
    </div>
    <h2>Todos Completas</h2>
    <div v-for="todo in completedTodos" 
        :key="todo.id">
      {{ todo.title }}
    </div>
    <h2>Todos</h2>
    <div v-for="todo in todos" 
        :key="todo.id">
        <input type="checkbox"
          v-model="todo.completed">
      {{ todo.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      user: {
        first_name: "Valdecir",
        last_name: "Ribeiro de Melo",
      },

      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
      ],
    };
  },

  components: {},

  computed: {
    fullName() {
      return `${this.user.first_name} ${this.user.last_name}`;
    },

    uncompletedTodos() {
      // retorna valores do array somente que forem diferentes de completed
      return this.todos.filter(todo => !todo.completed);
    },
    completedTodos() {
      // retorna valores do array somente que forem diferentes de completed
      return this.todos.filter(todo => todo.completed);
    },

  },

  methods: {
    OnClick($evt) {
      console.log(this, $evt);
    },
    OnClickUser($evt) {
      console.log(this.user, $evt);
    },
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
