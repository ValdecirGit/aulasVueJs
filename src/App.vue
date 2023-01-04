<template>
  <div>
    <h1>Personalizar componente usando Slot</h1>

    <TheHeader>
      <template v-slot:title> Home </template>
      <template v-slot:description> <p>Descrição</p> </template>

      Content do header - menu ....

    </TheHeader>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",

  components: {
    TheHeader,
  },

  data() {
    return {};
  },
  beforeUpdate() {},
  updated() {},
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  beforeUnmount() {},
  unmounted() {},

  watch: {},

  computed: {},

  methods: {},
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
