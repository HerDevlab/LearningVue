<template>
  
  <div>
      <h2>Exo 1 - Calculatrice</h2>
      <input type="number" v-model="num1">
      <br><br>
      <input type="text" v-model="signe">
      <br><br>
      <input type="number" v-model="num2">
      <br><br>
      <calcul :num1="num1" :num2="num2" :signe="signe"> </calcul> 
      <!-- si tu mets num1 tout cours, il pensera que c'est une var static, alors que la, il s'att a du js -->
      
      <h2>Exo 2 - Convertir</h2>
      <input type="number" v-model="km" id="km">
      <br><br>
      <input type="number" v-model="m" id="m">
      <br><br>
      <input type="number" v-model="cm" id="cm">
      <br><br>
      <input type="number" v-model="mm" id="mm">
      <br><br>      
  </div>


</template>

<script lang="ts">
import { defineComponent } from 'vue'
import calcul from './components/Calcul.vue'
import conversion from './components/Mesure.vue'

export default defineComponent({

  name: 'App',
  components: {
    calcul,
    conversion
  },

  data() {
    return{
      num1: 0,
      num2: 0,
      signe: ''
    }
  }

})
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