<template>
  <div>
    <BaseAlert 
      :variant="variant"
    >
      {{ text }}
    </BaseAlert>
  </div>
</template>

<script>
import BaseAlert from "./components/BaseAlert.vue";

export default {
  name: "App",

  components: {
    BaseAlert,
  },

  data() {
    return {
      variant: "danger",
      text: "Seu formulário foi enviado",
    };
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
