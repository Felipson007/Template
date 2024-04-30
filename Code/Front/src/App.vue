<template>
  <div class="landing-page">
    <!-- Cabeçalho -->
    <header class="header">
      <h1>{{ title }}</h1>
      <p>{{ subtitle }}</p>
    </header>
    
    <!-- Conteúdo Principal -->
    <main class="content">
      <img :src="imageSrc" alt="Imagem Representativa" />
      <p>{{ description }}</p>
      
      <!-- Testemunhos (exemplo de dados em uma lista) -->
      <section v-if="testimonials.length > 0">
        <h2>Testemunhos</h2>
        <ul>
          <li v-for="testimonial in testimonials" :key="testimonial.id">
            <p>{{ testimonial.text }}</p>
            <strong>{{ testimonial.name }}</strong>
          </li>
        </ul>
      </section>

      <!-- Formulário de Conversão -->
      <section>
        <h2>Preencha o formulário</h2>
        <form @submit.prevent="handleSubmit">
          <label for="name">Nome:</label>
          <input type="text" id="name" v-model="form.name" required />

          <label for="email">Email:</label>
          <input type="email" id="email" v-model="form.email" required />

          <!-- Adicione campos adicionais, se necessário -->

          <button type="submit">Enviar</button>
        </form>
      </section>
    </main>
    
    <!-- Rodapé -->
    <footer class="footer">
      <p>&copy; 2024 Minha Empresa. Todos os direitos reservados.</p>
      <a href="#">Política de Privacidade</a> | <a href="#">Termos de Uso</a>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Título Principal da Landing Page",
      subtitle: "Subtítulo ou descrição breve",
      imageSrc: "url-da-imagem.jpg",
      description: "Descrição detalhada do produto ou serviço que você está oferecendo.",
      testimonials: [
        { id: 1, text: "Testemunho 1", name: "Cliente 1" },
        { id: 2, text: "Testemunho 2", name: "Cliente 2" }
      ],
      form: {
        name: "",
        email: "",
      },
    };
  },
  methods: {
    handleSubmit() {
      // Lógica para lidar com o envio do formulário
      console.log("Formulário enviado:", this.form);
      // Resetar o formulário após o envio
      this.form.name = "";
      this.form.email = "";
    },
  },
};
</script>

<style scoped>
/* Adicione estilos aqui para personalizar a landing page */
.landing-page {

}
.header {
  display: flex;
  position: fixed;
  top: 0;
  background-color: black;
  width: 100%;
  align-items: center;
  flex-direction: row;
  left: 0;
}
.content {
  /* Estilos para o conteúdo principal */
}
.footer {
  /* Estilos para o rodapé */
}
</style>
