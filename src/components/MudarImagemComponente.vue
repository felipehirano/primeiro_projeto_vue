<template>
  <div>
    <!-- Dispara um emit mudarImagem para o componente que quiser escutá-lo -->
    <button @click="$emit('mudarImagem')">Trocar imagem de perfil</button>
  </div>
</template>
<script>
export default {
  name: "MudarImagemComponente",
  //   É necessário declarar os emits que o component irá disparar
  emits: ["mudarImagem"],
};
</script>
