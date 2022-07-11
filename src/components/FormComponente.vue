<template>
  <form action="">
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
};
</script>
