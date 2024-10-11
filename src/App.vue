<template>
  <div class="carousel-wrapper" @touchstart="startTouch" @touchend="endTouch">
    <div class="carousel" :style="{ transform: `translateX(-${currentPage * 100}vw)` }">
      <!-- Seções do carrossel -->
      <section id="home"><HomeComponent/></section>
      <section id="register">Cadastro de Pet Perdido</section>
      <section id="feed">Feed de Pets Perdidos</section>
      <section id="adoption">Adoção</section>
      <section id="profile">Perfil</section>
      <section id="about">Sobre Nós</section>
      <section id="donation">Doação</section>
    </div>
  </div>
  <div class="nav-box">
      <nav class="nav">
        <ul>
          <li ><a href="#home"><i class="fas fa-home"></i></a></li>
          <li><a href="#register"><i class="fas fa-paw"></i></a></li>
          <li><a href="#feed"><i class="fas fa-search"></i></a></li>
          <li><a href="#adoption"><i class="fas fa-heart"></i></a></li>
          <li><a href="#profile"><i class="fas fa-user"></i></a></li>
          <li><a href="#about"><i class="fas fa-info-circle"></i></a></li>
          <li><a href="#donation"><i class="fas fa-donate"></i></a></li>
        </ul>
      </nav>
    </div>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue';

export default {
  name: 'App',
  components: {
    HomeComponent,
  },
};
</script>

