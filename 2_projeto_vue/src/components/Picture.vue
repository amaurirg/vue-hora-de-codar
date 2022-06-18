<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="trocarImagem" />
  </div>
</template>

<script>
import MudarImagem from "./MudarImagem.vue";

export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Amauri Rossetti Giovani",
    };
  },
  components: { MudarImagem },
  methods: {
    trocarImagem() {
      this.avatar = './img/avatar2.png'
    },
  },
};
</script>