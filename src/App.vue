<template>
  <label for="area">Informe a área a ser pintada: </label>
  <input type="text" name="area" v-model="area">

  <button @click="calcLatas(area)">Apenas latas de 18L</button>
  <button @click="calcGaloes(area)">Apenas Galões de 3.6L</button>

  <p>{{ message }}</p>
</template>

<script>

export default {
  name: 'App',

  data() {
    return {
      area : 0,
      message : "",
    }
    
  },

  methods : {
    calcLatas(area){
      
    },

    calcGaloes(area){

    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
