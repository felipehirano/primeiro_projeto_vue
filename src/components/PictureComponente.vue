<template>
  <!-- O v-bind pode ser substituído pelo :  -->
  <img :src="avatar" :alt="descricao" />
</template>
<script>
export default {
  name: "PictureComponente",
  data() {
    return {
      avatar: "/images/logo.png",
      descricao: "Felipe Ken",
    };
  },
};
</script>
