<template>
  <div>
    <button @click="primeiro($event), segundo(txt, $event), terceiro()">Ativar múltiplos eventos</button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiplosEventos",
  data() {
    return {
        multiplos_eventos: '',
        txt: 'Outra forma de passar argumento'
    }
  },
  methods: {
    primeiro(e) {
        this.multiplos_eventos = 'Primeiro evento ativado!'
    },
    segundo(txt, e) {
        setTimeout(() => {
            this.multiplos_eventos = txt;
        }, 500);
    },
    terceiro() {
        setTimeout(() => {
            this.multiplos_eventos = ''
        }, 1500)
    }
  }
};
</script>

<style scoped>
div {
  margin: 100px;
}
</style>