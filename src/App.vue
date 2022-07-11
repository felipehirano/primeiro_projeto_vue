<template>
  <PrimeiroComponente />
  <LifeCycleComponente />
  <PessoaComponente />
</template>

<script>
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycleComponente from "./components/LifeCycleComponente.vue";
import PessoaComponente from "./components/PessoaComponente.vue";

export default {
  name: "App",
  components: {
    PrimeiroComponente,
    LifeCycleComponente,
    PessoaComponente,
  },
};
</script>
