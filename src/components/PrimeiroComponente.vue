<template>
  <h1>Olá vue!</h1>
  <p>Meu nome é : {{ nome }} e eu sou {{ profissao }}</p>
</template>

<script>
export default {
  name: "PrimeiroComponente",
  data() {
    return {
      nome: "Felipe",
      profissao: "Programador",
    };
  },
};
</script>
