<template>
  <div>
    <Header
      :logoSrc="logoPath"
      :companyName="companyName"
      :button1Text="button1Text"
      :button2Text="button2Text"
    />
    <!-- Conteúdo adicional -->
  </div>
</template>

<script>
import Header from './components/Header.vue';
import logo from './assets/logo.jpg';
export default {
  components: {
    Header,
  },
  data() {
    return {
      logoPath: logo, // Substitua pelo caminho do logo
      companyName: 'Growth',
      button1Text: 'Botão 1',
      button2Text: 'Botão 2',
    };
  },
};
</script>
