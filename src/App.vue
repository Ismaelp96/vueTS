<template>
  <div id="app">
    <contador-body :valorInicial="10" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import ContadorBody from '@/components/ContadorBody.vue'
@Component({
  components: {
    ContadorBody,
  },
})
export default class App extends Vue {}
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
