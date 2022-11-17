<template>
  <div>
    <Header :esta_logado="true"/>
    <PrimeiroComponente/>
    <p class="paragrafo-pai">Minha string é: {{teste}}</p>
    <LifeCycle/>
    <Pessoa/>
  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Header
  },
  data() {
    return {
      teste: 'testando'
    }
  }
}
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;
  }
</style>