<template>
    <div class="signup-container">
      <!-- Container da Esquerda -->
      <div class="left-container">
        <h1>Registro de Pet Perdido</h1>
        <div class="puppy">
          <img src="https://i.imgur.com/FotMRrh.png" alt="Imagem do Pet">
        </div>
      </div>
  
      <!-- Container da Direita -->
      <div class="right-container">
        <header>
          <h1>Ajude a encontrar o seu pet!</h1>
          <p>Para cadastrar um <b>pet perdido</b>, preencha os dados com <b>nome, raça, último local visto</b> e informações de <b>contato</b>. Assim, aumentamos as chances de <b>encontrá-lo rapidamente</b></p>
          <div class="set">
            <div class="input-group">
              <label for="pets-name">Nome do Pet</label>
              <input v-model="petData.name" id="pets-name" type="text" placeholder="Nome do pet">
            </div>
            <div class="input-group pets-photo">
              <div class="pp">
                  <button id="pets-upload" @click="uploadPhoto">
                    <i class="fas fa-camera-retro"></i>
                  </button>
                  <label for="pets-upload">Envie uma foto</label>
              </div>
            </div>
          </div>
  
          <div class="set">
            <div class="input-group">
              <label for="pets-breed">Raça</label>
              <input v-model="petData.breed" id="pets-breed" type="text" placeholder="Raça do pet">
            </div>
            <div class="input-group">
              <label for="pets-location">Último Local Visto</label>
              <input v-model="petData.location" id="pets-location" type="text" placeholder="Ex: Rua A, Bairro B">
            </div>
          </div>
  
          <div class="set">
            <div class="input-group">
              <label for="pet-gender">Gênero</label>
              <div class="radio-container">
                <input v-model="petData.gender" id="pet-gender-female" name="pet-gender" type="radio" value="Fêmea">
                <label for="pet-gender-female">Fêmea</label>
                <input v-model="petData.gender" id="pet-gender-male" name="pet-gender" type="radio" value="Macho">
                <label for="pet-gender-male">Macho</label>
              </div>
            </div>
            <div class="input-group">
              <label for="pets-contact">Informações de Contato</label>
              <input v-model="petData.contact" id="pets-contact" type="text" placeholder="Telefone ou e-mail">
            </div>
          </div>
  
          <div class="set">
            <div class="input-group">
              <label for="pets-features">Características Especiais</label>
              <input v-model="petData.features" id="pets-features" type="text" placeholder="Ex: Coleira vermelha, cicatriz">
            </div>
            <div class="input-group">
              <label for="pets-color">Cor do Pet</label>
              <input v-model="petData.color" id="pets-color" type="text" placeholder="Ex: Preto, Branco">
            </div>
          </div>
        </header>
        
        <footer>
          <button @click="submitForm" class="btn">Cadastrar Pet</button>
        </footer>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        petData: {
          name: '',
          breed: '',
          location: '',
          gender: 'Fêmea',
          contact: '',
          features: '',
          color: ''
        }
      };
    },
    methods: {
      // Função de upload de foto
      uploadPhoto() {
        // Aqui você pode adicionar a lógica de upload no Firebase Storage no futuro
        alert("Funcionalidade de upload de foto será adicionada em breve!");
      },
      
      // Função de envio de formulário
      async submitForm() {
        try {
          // Esta função será configurada para enviar dados ao Firebase
          console.log("Dados do Pet:", this.petData);
          alert("Formulário enviado com sucesso! Integração com o Firebase em breve.");
          
          // Limpar o formulário após envio
          this.resetForm();
        } catch (error) {
          console.error("Erro ao enviar o formulário:", error);
          alert("Erro ao enviar o formulário, tente novamente.");
        }
      },
  
      // Função para limpar o formulário após o envio
      resetForm() {
        this.petData = {
          name: '',
          breed: '',
          location: '',
          gender: 'Fêmea',
          contact: '',
          features: '',
          color: ''
        };
      }
    }
  };
  </script>
  
  <style scoped>
      @import url('https://fonts.googleapis.com/css?family=Montserrat:400,600&display=swap');
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  .pp {
    display: flex;
    gap: 10px;
    align-items: center;
  }

  body {
    align-items: center;
    display: grid;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    font-weight: 400;
    height: 100vh;
    justify-items: center;
  }

  .signup-container {
    display: flex;
    max-width: 900px;
    border-radius: 30px;
    overflow: hidden;
  }

  .left-container {
    width: 300px;
    background-image: linear-gradient(to bottom, #bb83fb, #7C05B2);
    padding: 40px 0;
    text-align: center;
    position: relative;
  }

  .left-container h1 {
    color: #ffffff;
    font-size: 24px;
  }

  .left-container img {
    position: absolute;
    bottom: 0;
    left: 0;
    max-width: 100%;
  }

  .right-container {
    flex: 1;
    color: #ffffff;
    background: #7C05B2;
    display: flex;
    flex-direction: column;
    padding: 20px;

    & p {
        font-size: 12px;
        margin-bottom: 20px;
    }
  }

  .right-container h1 {
    font-size: 28px;
    font-weight: 900;
    margin-bottom: 20px;
  }

  .set {
    display: flex;
    gap: 20px;
    margin: 10px 0;
    flex-wrap: wrap;
  }

  .input-group {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 5px;
  }

  .input-group label {
    color: #ffffff;
    font-weight: 500;
  }

  .input-group input {
    height: 38px;
    border: none;
    border-radius: 30px;
    padding: 12px 25px;
  }

  .pets-photo button {
    background-color: #ffffff;
    border: none;
    border-radius: 50%;
    height: 38px;
    width: 38px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .pets-photo button i {
    color: #7C05B2;
    font-size: 16px;
  }

  .radio-container {
    display: flex;
    gap: 10px;
    align-items: center;
  }

  .radio-container input[type="radio"] {
    display: none;
  }

  .radio-container label {
    color: #ffffff;
    cursor: pointer;
    padding: 8px 12px;
    border-radius: 15px;
    background: #ffffff00;
    transition: background 0.3s;
  }

  .radio-container input[type="radio"]:checked + label {
    background: #00000025;
  }

  footer {
    margin-top: auto;
    display: flex;
    justify-content: center;
  }

  .btn {
   
    padding: 12px 25px;
 
  }

  .btn1:hover {
    background-color: #f5f5f5;
  }

  
  @media (max-width: 844px) {

    .pets-photo {
        display: flex;
    }

    .signup-container {
      flex-direction: column;
      max-width: 100%;
      border-radius: 0;
    }

    .left-container {
      display: none;
    }

    .right-container {
      width: 100%;
      background-color: #7b05b200;
      border-radius: 0;

      & h1, p {
        text-align: center;
      }

      & b {
        color: #7C05B2;
      }
    }

    .set {
      flex-direction: column;
    }
  }
  </style>
  