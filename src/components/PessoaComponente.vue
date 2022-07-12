<template>
  <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
  <InfoComponente :email="email" :esta_trabalhando="false" />
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
      email: "fkenhirano4@gmail.com",
    };
  },
};
</script>
