<template>
  <!-- Exemplo de como cada componente é independente. Ao clicar no botão ativar, 
  verá que apenas no que foi clicado será mostrado a mensagem de botão ativo. -->
  <ReutilizacaoComponente />
  <h1>Olá vue!</h1>
  <ReutilizacaoComponente />
  <p>Meu nome é : {{ nome }} e eu sou {{ profissao }}</p>
  <MultiplosEventosComponente />
  <ReutilizacaoComponente />
  <ReutilizacaoComponente />
  <ReutilizacaoComponente />
</template>

<script>
import MultiplosEventosComponente from "./MultiplosEventosComponente";
import ReutilizacaoComponente from "./ReutilizacaoComponente";
export default {
  name: "PrimeiroComponente",
  components: { MultiplosEventosComponente, ReutilizacaoComponente },
  data() {
    return {
      nome: "Felipe",
      profissao: "Programador",
    };
  },
};
</script>
