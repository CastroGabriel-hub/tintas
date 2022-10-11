<template>
  <label for="area">Informe a área a ser pintada: </label>
  <input type="text" name="area" v-model="area">
</template>

<script>

export default {
  name: 'App',

  data() {
    return {
      area : 0,
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
