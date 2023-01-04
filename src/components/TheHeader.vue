<template>
  <header class="header">Header</header>
</template>

<script>

export default {
  // componente foi montado
  
  mounted(){
    console.log('mounted')
    window.addEventListener('resize', this.resize)
  },   

  //antes do componente ser desmontado
  beforeUnmount() {
    // destruir as libs
    // Eventos
    // listeners
    console.log("beforeUnmount");
    window.removeEventListener('resize', this.resize);
  },

  // componente desmontado</h5>
  unmounted() {
    console.log("unmounted");
  },

  methods: {
    resize($evt){
        console.log($evt)
    }
  }
};
</script>

<style>
.header {
  background-color: blueviolet;
  color: #fff;
}
</style>