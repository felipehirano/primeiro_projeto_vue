<template>
  <HeaderComponente />
  <PrimeiroComponente />
  <LifeCycleComponente />
  <PessoaComponente />
</template>

<script>
import HeaderComponente from "./components/HeaderComponente.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycleComponente from "./components/LifeCycleComponente.vue";
import PessoaComponente from "./components/PessoaComponente.vue";

export default {
  name: "App",
  components: {
    HeaderComponente,
    PrimeiroComponente,
    LifeCycleComponente,
    PessoaComponente,
  },
};
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}

a {
  color: red;
}
</style>
