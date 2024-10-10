<template>
 <div class="container">
  <div class="box">
    <img class="logo" :src="require('@/assets/logo-amor-de-pet.png')" alt="Dog Home">
    <h1>Encontre seu pet perdido</h1>
    <p>Encontre seu pet de forma <b>rápida e eficiente</b>. Anuncie <b>gratuitamente</b> e tenha acesso ao Painel de Busca!</p>
    <div class="buttons">
      <button class="btn">Cadastrar Pet</button>
      <button class="btn1">Encontrar Pet</button>
    </div>
    <div class="buttons">
      <button class="btn2"> <img class="google" :src="require('@/assets/google-logo.png')" alt="google-logo"> Entrar com Google</button>
    </div>
  </div>
  <img class="pet-float" :src="require('@/assets/dog-home.png')" alt="Dog Home">
 </div>
</template>

<script>
export default {
  name: 'HomeComponent',
  props: {
    msg: String
  }
}
</script>


<style scoped>
.container {
  width: 100vw;
  background-image: linear-gradient(to bottom, #ffb602, #ea9401);
  height: 100vh;
}

.pet-float {
  max-width: 20rem;
  position: absolute;
  bottom: 0px;
  right: 0;
}

.box {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 5%;
  text-align: center;
  color: #fff;

  & b {
    color: #7C05B2;
  }
}

.logo {
  max-width: 250px;
}

.google {
  max-width: 12%;
}

.buttons {
  width: 100%;
  align-items: center;
  justify-content: center;
  display: flex;
  gap: 2.5%;
}

@media (max-width: 844px) {
  .pet-float {
    display: none;
  }
}


</style>
