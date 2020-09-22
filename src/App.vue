<template>
  <div id="app">
    <app-quote>
      <h2 slot="title">{{quoteTitle}}</h2>

      <p slot="content">A wonderful quote</p>
      <button @click="quoteTitle='A wonderful Quote'">change quote</button>
    </app-quote>

    <hr>
    <div class="components-list">

        <h1>Dynamic components</h1>
        <button @click="selectedComponent='appHappy'">Happyness</button>
        <button @click="selectedComponent='appEarth'">Earth</button>
        <button>Spiritual</button>
        <button>Motivation</button>
        <component :is="selectedComponent">
      </component >

    </div>

  </div>
</template>

<script>

import Quote from './components/Quote.vue';
import Happy from './components/Happy.vue';
import Earth from './components/Earth.vue';
export default {
  name: 'App',
  data(){
    return{
    quoteTitle:'Erase the word dont',
    selectedComponent:'appHappy'
}  },
  components: {
    appQuote:Quote,
    appHappy:Happy,
    appEarth:Earth
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
.components-list button{
  margin: 0 10px;
}
</style>
