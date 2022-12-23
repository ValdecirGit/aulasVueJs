<template>
  <div>
    <div>
      One-way data binding <br>
      Two-way data binding <br>
      v-model -->> formulários <br><br>
    </div>

    <div>
      <label>Nome:</label><br>
      <input type="text" v-model="name">
      <br>
      {{ name }}
    </div>
    <br>
    <br>
    <div>
      <select v-model="sports">
        <option value="">Escolha</option>
        <option value="futebol">Futebol</option>
        <option value="basquete">Basquete</option>
        <option value="voleibol">Voleibol</option>
      </select>
      <br>
      <br>
      {{ sports }}
    </div>
    <br>
    <br>
    <div>
      <label>NewsLetter</label>
      <input v-model="newsletter" type="radio" value="Sim">
      Sim 
      <input v-model="newsletter" type="radio" value="Nao">
      Nao
      <br>
      <br>
      {{ newsletter }}
    </div>
    <br>
    <br>
    <input v-model="contract" 
         type="checkbox" value="Nao">
      Aceita nossos termos ...
      <br>
      <br>
      {{ contract }}
    <br>
    <br>
    <div>
      <label>Marque as cores que vc gosta</label>
      <br>
      <input v-model="colors" type="checkbox" value="azul">
      azul 
      <input v-model="colors" type="checkbox" value="amarelo">
      amarelo
      
      <br>
      {{ colors }}
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',

  data() {
    return {
      name: 'jhos nosw',
      sports: '',
      newsletter: 'Nao',
      contract: true,
      colors: []
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
