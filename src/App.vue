<template>
  <div class="carousel-wrapper" @touchstart="startTouch" @touchend="endTouch">
    <div class="carousel" :style="{ transform: `translateX(-${currentPage * 100}vw)` }">
      <!-- Seções do carrossel -->
      <section id="home"><HomeComponent /></section>
      <section id="register">Cadastro de Pet Perdido</section>
      <section id="feed">Feed de Pets Perdidos</section>
      <section id="adoption">Adoção</section>
      <section id="profile">Perfil</section>
      <section id="about">Sobre Nós</section>
      <section id="donation">Doação</section>
    </div>

    <!-- Barra de Navegação -->
    <div class="nav-box">
      <nav class="nav">
        <ul>
          <li @click="goToPage(0)"><a href="#home"><i class="fas fa-home"></i></a></li>
          <li @click="goToPage(1)"><a href="#register"><i class="fas fa-paw"></i></a></li>
          <li @click="goToPage(2)"><a href="#feed"><i class="fas fa-search"></i></a></li>
          <li @click="goToPage(3)"><a href="#adoption"><i class="fas fa-heart"></i></a></li>
          <li @click="goToPage(4)"><a href="#profile"><i class="fas fa-user"></i></a></li>
          <li @click="goToPage(5)"><a href="#about"><i class="fas fa-info-circle"></i></a></li>
          <li @click="goToPage(6)"><a href="#donation"><i class="fas fa-donate"></i></a></li>
        </ul>
      </nav>
    </div>

    <!-- Indicadores (bolinhas) -->
    <div class="indicators">
      <span v-for="(indicator, index) in 7" :key="index"
        :class="{'active': currentPage === index}"
        @click="goToPage(index)"
        @mouseover="hoveredIndex = index"
        @mouseleave="hoveredIndex = null"
        :style="{ opacity: hoveredIndex === index ? 0.6 : 1 }">
      </span>
    </div>
  </div>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue';

export default {
  name: 'App',
  components: {
    HomeComponent,
  },
  data() {
    return {
      currentPage: 0, // Página atual do carrossel
      startX: 0, // Coordenada inicial do toque para mobile
      endX: 0, // Coordenada final do toque para mobile
      isSwiping: false, // Para controle do swipe
    };
  },
  methods: {
    goToPage(page) {
      this.currentPage = page; // Atualiza a página atual ao clicar nos ícones ou bolinhas
    },
    startTouch(e) {
      this.startX = e.touches[0].clientX; // Captura a posição inicial do toque
      this.isSwiping = true;
    },
    endTouch(e) {
      this.endX = e.changedTouches[0].clientX; // Captura a posição final do toque
      const diff = this.startX - this.endX;

      if (this.isSwiping) {
        // Lógica para passar apenas uma página por vez
        if (diff > 50 && this.currentPage < 6) {
          this.currentPage++;
        } else if (diff < -50 && this.currentPage > 0) {
          this.currentPage--;
        }
        this.isSwiping = false;
      }
    },
  },
};
</script>

<style>
/* Mantendo seu estilo original */

@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Shrikhand&display=swap');

* {
  margin: 0;
  padding: 0;
}

h1 {
  font-family: 'Montserrat', sans-serif;
  font-size: 3rem;
  font-weight: 900;
}

p {
  font-family: 'Montserrat', sans-serif;
  max-width: 500px;
  font-size: 1rem;
}

button {
  font-weight: 300;
  padding: 15px 28px;
  border-radius: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1), 0 4px 8px rgba(0, 0, 0, 0.05);
  transition: 400ms;
}

button:hover {
  filter: brightness(0.7);
}

.btn {
  border: 3px solid #fff;
  background: #7C05B2;
  color: #fff;
}

.btn1 {
  border: 3px solid #7C05B2;
  background: #fff;
  color: #7C05B2;
}

.btn2 {
  padding: 15px 8px;
  gap: 8px;
  border: 3px solid #fff;
  background: #fff;
  color: #868686;
  outline: none;
}

.nav-box {
  width: 100%;
  height: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 90vh;
}

.nav {
  padding: 15px 28px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1), 0 4px 8px rgba(0, 0, 0, 0.05);
  border-radius: 30px;
  background-color: #fff;
}

ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

ul li a i {
  font-size: 20px;
  color: #7C05B2;
}

/* Estilo do carrossel */
.carousel-wrapper {
  position: relative;
  overflow: hidden;
}

.carousel {
  display: flex;
  transition: transform 0.5s ease-in-out;
  width: 700%; /* Cada seção ocupa 100% da tela */
}

section {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  background-image: linear-gradient(to bottom, #ffb602, #ea9401);
}

/* Estilo para o indicador (bolinhas) */
.indicators {
  position: fixed;
  bottom: 1%;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 25px;
}

.indicators span {
  display: block;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background-color: transparent;
  border: 2px solid #fff;
  cursor: pointer;
  transition: opacity 0.3s ease, transform 0.3s ease;
}

.indicators span.active {
  background-color: #7C05B2;
}

.indicators span:hover {
  transform: scale(1.2); /* Efeito de aumento ao passar o mouse */
}
</style>
