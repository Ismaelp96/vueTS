<template>
  <div class="contador-body">
    <h1>Contador</h1>
    <h2>{{ valor }}</h2>
    <button @click="setValor(-1)">Diminuir</button>
    <button @click="setValor(1)">Adicionar</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    valorInicial: {
      type: Number,
    },
  },
  data() {
    return {
      valor: this.valorInicial || 0,
    }
  },
  methods: {
    setValor(delta: number) {
      this.valor += delta
    },
  },
})
</script>

<style>
.contador-body h1 {
  margin-bottom: 2.4rem;
}
.contador-body h2 {
  margin-bottom: 2.4rem;
}
button {
  border: 1px solid transparent;
  background-color: #444;
  padding: 0 1.6rem;
  display: inline-flex;
  line-height: 30px;
  border-radius: 6px;
  color: white;
  transition: all 0.3s ease-in-out;
  cursor: pointer;
}
button:not(:first-child) {
  margin-left: 10px;
}
button:hover {
  background-color: transparent;
  color: #444;
  border-color: #444;
}
</style>
