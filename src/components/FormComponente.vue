<template>
  <form action="" @submit="enviarFormulario($event)">
    <div>
      <InputTextComponente />
    </div>
    <div>
      <InputTextComponente />
    </div>
    <div>
      <SubmitComponente />
    </div>
  </form>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
  <p>Conteúdo</p>
</template>
<script>
import InputTextComponente from "./form/InputTextComponente.vue";
import SubmitComponente from "./form/SubmitComponente.vue";

export default {
  name: "FormComponente",
  components: {
    InputTextComponente,
    SubmitComponente,
  },
  methods: {
    enviarFormulario(e) {
      // O evento default do formulário é enviar as informações para o servidor para o processamento da informação, recarregando a página em seguida.
      // Porém, não é isso o que queremos aqui. Queremos que os dados sejam trabalhados antes de enviar para o processamento no servidor.
      // O e.preventDefault vai evitar que esse comportamento padrão dele ocorra, tornando possível trabalharmos os dados utilizando esse método.
      e.preventDefault();
      console.log("Enviar formulário");
    },
  },
};
</script>

<style scoped>
p {
  margin: 50px;
}
</style>
