<template>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Projetos</a></li>
    <li><a href="#">Contatos</a></li>
    <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>
  </ul>
</template>

<script>
export default {
  name: "HeaderComponente",
  props: ["esta_logado"],
};
</script>

<!--
A prop scoped acompanhada da tag style ganha nas regras de seletores.
Ele adiciona uma tag [data-] no começo da classe mostrando que é exclusivo do componente.
-->
<style scoped>
ul {
  list-style: none;
  display: flex;
  background: #999;
}
li {
  margin-right: 10px;
}
a {
  color: #ddd;
  text-decoration: none;
  transition: 0.5s;
}

a:hover {
  color: turquoise;
}
</style>
