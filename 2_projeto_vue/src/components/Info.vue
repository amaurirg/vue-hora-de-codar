<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando como {{ cargo }} no momento</p>
    <p v-else>Estou em busca de novas oportunidades.</p>
    <p>Utilizo as seguintes tecnologias para backend:</p>
    <ul>
      <li
        v-for="(technology, index) in backend_technologies"
        v-bind:key="index"
      >
        {{ technology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para frontend:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para {{ email }}</p>
    <p class="teste">
      Para acessar meu portfólio
      <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture.vue";

export default {
  name: "Info",
  data() {
    return {
      mostrar_email: false,
      meu_link: "https://google.com",
      textoBotao: "Mostrar email",
      backend_technologies: ["Python", "JavaScript", "PHP"],
      frontend_technologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "CSS" },
        { id: 3, language: "VueJS" },
      ],
    };
  },
  components: { Picture },
  props: {
    email: String,
    esta_trabalhando: Boolean,
    cargo: String,
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textoBotao = "Mostrar email";
      } else {
        this.textoBotao = "Esconder email";
      }
    },
  },
};
</script>