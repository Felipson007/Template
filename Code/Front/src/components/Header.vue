<template>
    <header class="header">
      <div class="logo-container">
        <img :src="logoSrc" alt="Logo da Empresa" class="logo">
        <span class="company-name">{{ companyName }}</span>
      </div>
      <div class="button-container">
        <button @click="onButtonClick1" class="button">{{ button1Text }}</button>
        <button @click="onButtonClick2" class="button">{{ button2Text }}</button>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    props: {
      logoSrc: {
        type: String,
        required: true,
      },
      companyName: {
        type: String,
        required: true,
      },
      button1Text: {
        type: String,
        required: true,
      },
      button2Text: {
        type: String,
        required: true,
      },
    },
    methods: {
      onButtonClick1() {
        // Ação ao clicar no botão 1
        console.log("Botão 1 clicado");
      },
      onButtonClick2() {
        // Ação ao clicar no botão 2
        console.log("Botão 2 clicado");
      }
    }
  }
  </script>
  
  <style>
  /* Estilo do Header */
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 7rem;
    top: 0;
    position: fixed;
    width: 100%;
    left: 0;
    background-color: #f5f5f5;
}
  
  /* Estilo para o container do logo e nome da empresa */
  .logo-container {
    display: flex;
    align-items: center;
  }
  
  /* Estilo da logo */
  .logo {
    width: 50px;
    height: auto;
    margin-right: 10px;
  }
  
  /* Estilo do nome da empresa */
  .company-name {
    font-size: 18px;
    font-weight: bold;
  }
  
  /* Estilo para o container dos botões */
  .button-container {
    display: flex;
    gap: 10px;
  }
  
  /* Estilo para os botões */
  .button {
    padding: 8px 12px;
    background-color: #007BFF;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .button:hover {
    background-color: #0056b3;
  }
  </style>
  