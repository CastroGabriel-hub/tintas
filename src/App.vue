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
      let litersNeeded = area / 6;
      let latasNeeded = Math.round(litersNeeded / 18);
      latasNeeded === 0 ? latasNeeded = 1 : null;
      let latasPrice = latasNeeded * 80;
      
      this.message = `Você precisa comprar ${latasNeeded} latas de tinta, que custarão R$ ${latasPrice}`;
    },

    calcGaloes(area){
      let litersNeeded = area / 6;
      let galoesNeeded = Math.round(litersNeeded / 3.6);
      galoesNeeded === 0 ? galoesNeeded = 1 : null;
      let galoesPrice = galoesNeeded * 25;

      this.message = `Você precisa comprar ${galoesNeeded} galões de tinta, que custarão R$ ${galoesPrice}`;
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
