<template>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades.</p>
  <p>Utilizo as seguintes tecnologias no back-end:</p>
  <ul>
    <!-- Utilizando o bind no for para parar de dar o erro de keys obrigatórias. -->
    <li v-for:="technology in backend_technologies">{{ technology }}</li>
  </ul>
  <p>Utilizo as seguintes tecnologias no back-end:</p>
  <ul>
    <!-- Utilizando o bind como key para mostrar a outra forma de retirar o erro das keys obrigatórias -->
    <li v-for="technology in frontend_technologies" :key="technology.id">
      {{ technology.language }}
    </li>
  </ul>
  <div>
    <button @click="showEmail">{{ texto_botao }}</button>
  </div>
  <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  <!-- Para atributos html, é necessário usar o v-bind para linkar o atributo dinâmico. -->
  <p>
    Para acessar meu portfólio <a v-bind:href="meu_link">basta clicar aqui</a>
  </p>
  <PictureComponente />
</template>

<script>
import PictureComponente from "./PictureComponente.vue";

export default {
  name: "InfoComponente",
  components: { PictureComponente },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      email: "fkenhirano4@gmail.com",
      meu_link: "https://google.com",
      texto_botao: "Mostrar e-mail",
      backend_technologies: ["Java", "Python", "PHP"],
      frontend_technologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "Javascript" },
      ],
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.texto_botao = "Mostrar e-mail";
      } else {
        this.texto_botao = "Esconder e-mail";
      }
    },
  },
};
</script>
