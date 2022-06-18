<template>
  <div>
    <Reutilizacao />
    <h1>Olá Vue</h1>
    <p>Meu nome é {{ nome }}</p>
    <Reutilizacao />
    <Reutilizacao />

    <MultiplosEventos />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue";
import Reutilizacao from "./Reutilizacao.vue";
export default {
  name: "PrimeiroComponente",
  data() {
    return {
      nome: "Amauri",
    };
  },
  components: {
    MultiplosEventos,
    Reutilizacao
  },
};
</script>