<template>
  <!-- O v-bind pode ser substituído pelo :  -->
  <img :src="avatar" :alt="descricao" />
  <!-- Aqui está o exemplo de como utilizar o emit para enviar/escutar eventos de um componente filho -->
  <MudarImagemComponente @mudar-imagem="trocarImagem" />
</template>
<script>
import MudarImagemComponente from "./MudarImagemComponente.vue";
export default {
  name: "PictureComponente",
  components: { MudarImagemComponente },
  data() {
    return {
      avatar: "/images/logo.png",
      descricao: "Felipe Ken",
    };
  },
  methods: {
    trocarImagem() {
      this.avatar = "/images/logo-collapsed.png";
    },
  },
};
</script>
