<template>
  <div>
    <button
      @click="
        primeiro(textoPrimeiro, $event),
          segundo(textoSegundo, $event),
          terceiro($event)
      "
    >
      Ativar múltipols eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>
<script>
export default {
  name: "MultiplosEventosComponente",
  data() {
    return {
      multiplos_eventos: "",
      textoPrimeiro: "Primeiro evento",
      textoSegundo: "Segundo evento",
    };
  },
  methods: {
    primeiro(texto) {
      this.multiplos_eventos = texto;
    },
    segundo(texto) {
      setTimeout(() => {
        this.multiplos_eventos = texto;
      }, 500);
    },
    terceiro() {
      setTimeout(() => {
        this.multiplos_eventos = "";
      }, 1500);
    },
  },
};
</script>
<style scoped>
div {
  margin: 100px;
}
</style>
