<template>
  <div class="contador-class">
    <h1>Contador com Classe</h1>
    <h2>{{ valor }}</h2>
    <h3>{{ getParOuImpar() }}</h3>
    <h3>{{ parOuImpar }}</h3>
    <button @click="setValor(-5)">Diminuir</button>
    <button @click="setValor(5)">Adicionar</button>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'

@Component
export default class ContadorClasse extends Vue {
  @Prop(Number) private readonly valorInicialClass?: number
  private valor: number = this.valorInicialClass || 0

  public setValor(delta: number) {
    this.valor += delta
  }
  public getParOuImpar(): string {
    return this.valor % 2 === 0 ? 'Par' : 'Impar'
  }
  public get parOuImpar(): string {
    return this.valor % 2 === 0 ? 'Par' : 'Impar'
  }
}
</script>

<style>
.contador-class h1 {
  margin-bottom: 2.4rem;
}
.contador-class h2 {
  margin-bottom: 2.4rem;
}
.contador-class h3 {
  margin-bottom: 2.4rem;
}
</style>
