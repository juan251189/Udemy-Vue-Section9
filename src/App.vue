<template>
  <div id="app">
    <app-quote>
      <h2 slot="title">{{quoteTitle}}</h2>
      <span slot="subtitle">Some Subtitle</span>
      <p slot="content">A wonderful quote</p>
      <button @click="quoteTitle='A wonderful Quote'">change quote</button>
    </app-quote>
  </div>
</template>

<script>

import Quote from './components/Quote.vue'
export default {
  name: 'App',
  data(){
    return{
    quoteTitle:'Erase the word dont'
}  },
  components: {
    appQuote:Quote
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
