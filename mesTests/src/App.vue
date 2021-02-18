<template>
  <div>
    Message: {{ message }}
    <br>
    <button @click="compter"> J'ai été cliqué {{ counter }} fois. </button>
    <br>
    <p v-if="seen">Fantôme: {{ phantome }}</p>
    <br>
    <button @click="display"> {{ appardi }} </button>
    <br>
    <input type="text" v-model="inversion">
    <p>résultat: {{ inverser }}</p>
    <li v-for="item in groceryList" :key="item.id">{{item.id+1}}. {{ item.text }}</li>
    <br>
    <input v-model="ecrit">
    <p>{{ yeux }}</p>

  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
// import HelloWorld from './components/HelloWorld.vue'

export default defineComponent({
  name: 'App',
  components: {
    // HelloWorld
  },

  data(){
    return {
      message: 'Je suis un message.',
      counter: 0,
      seen: true,
      phantome: 'Je peux disparaitre.',
      appardi: 'disparition',
      inversion: '',
      groceryList: [
        { id: 0, text: 'Légumes' },
        { id: 1, text: 'Fruits' },
        { id: 2, text: 'Riz' }
      ],
      ecrit: '',
      yeux: 'Ecris un truc, je t\'observe.'
    }
  },

  methods: {
    display(){
      if (this.seen){
        this.seen = false
        this.appardi = 'apparition!'
      }
      else{
        this.seen = true
        this.appardi = 'disparition!'
      }
    },

    compter(){
      this.counter ++
    }
  },

  computed: {
    inverser: function(){
     return this.inversion.split('').reverse().join('')
    }
  },

  // watch: {
  //   observer: function(){
  //     return this.yeux = 'oooh tu écris!'
  //   }
  // }


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