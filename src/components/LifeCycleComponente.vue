<template>
  <h1>Meu nome é : {{ nome }}</h1>
</template>

<script>
export default {
  name: "LifeCycleComponente",
  data() {
    return {
      nome: "Ainda não sei",
    };
  },
  // Hooks
  created() {
    setTimeout(() => {
      this.nome = "Felipe";
    }, 2000);
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Ken";
    }, 4000);
  },
};
</script>
