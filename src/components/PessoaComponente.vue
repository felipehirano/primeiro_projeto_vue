<template>
  <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
  <InfoComponente />
  <FormComponente />
</template>
<script>
import FormComponente from "./FormComponente.vue";
import InfoComponente from "./InfoComponente.vue";
export default {
  components: { InfoComponente, FormComponente },
  name: "PessoaComponente",
  data() {
    return {
      nome: "Felipe",
    };
  },
};
</script>
