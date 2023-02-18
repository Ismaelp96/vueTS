<template>
  <div id="app">
    <contador-body :valorInicial="10" />
    <contador-classe :valorInicialClass="100" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import ContadorBody from '@/components/ContadorBody.vue'
import ContadorClasse from '@/components/ContadorClasse.vue'
@Component({
  components: {
    ContadorBody,
    ContadorClasse,
  },
})
export default class App extends Vue {}
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
html {
  font-size: 62.5%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 100vh;
  font-size: 1.6rem;
}
</style>
