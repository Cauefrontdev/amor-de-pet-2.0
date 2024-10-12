<template>

 <div class="container">
 
  <div class="box">
    <img class="logo" :src="require('@/assets/img/logo-amor-de-pet.png')" alt="Dog Home">
    <h1>Encontre seu pet perdido</h1>
    <p>Encontre seu pet de forma <b>rápida e eficiente</b>. Anuncie <b>gratuitamente</b> e tenha acesso ao Painel de Busca!</p>
    <div class="buttons">
      <button class="btn">Cadastrar Pet</button>
      <button class="btn1">Encontrar Pet</button>
    </div>
    <div class="buttons">
      <button class="btn2"> <img class="google" :src="require('@/assets/img/google-logo.png')" alt="google-logo"> Entrar com Google</button>
    </div>
  </div>
  <img class="pet-float img" :src="require('@/assets/img/dog-home.png')" alt="Dog Home">
  <img class="vetor " :src="require('@/assets/img/vetor1.png')" alt="Dog Home">
  <img class="vetor1" :src="require('@/assets/img/vetor2.png')" alt="Dog Home">
  <img class="vetor2" :src="require('@/assets/img/vetor1.png')" alt="Dog Home">
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
  position: relative;
  width: 100vw;
  background: linear-gradient(to top, #ffb602, #f9c543 );
  height: 100vh;
}

.pet-float {
  max-width: 340px;
  position: absolute;
  right: 0;
  bottom: 0;
}

.vetor {
  max-width: 12vw;
  position: absolute;
  left: -2rem;
  top: -3rem;
}

.vetor1 {
  max-width: 20vw;
  position: absolute;
  transform: rotate(25deg);
  left: 10rem;
  bottom: 5rem;
}

.vetor2 {
  max-width: 15vw;
  position: absolute;
  transform: rotate(-55deg);
  right: 5rem;
  top: 5rem;
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

img {
  filter: opacity(0.9);
}

@media (max-width: 1000px) {

  .container {
    height: 80vh;
  }
  .img {
    display: none;
  }

  .vetor {
  max-width: 25vw;
  position: absolute;
  left: -8%;
  transform: rotate(50deg);
  top: -1rem;
}

.vetor1 {
  max-width: 40vw;
  position: absolute;
  transform: rotate(25deg);
  left: 0rem;
  bottom: -5rem;
}

.vetor2 {
  max-width: 15vw;
  position: absolute;
  transform: rotate(-55deg);
  right: 0rem;
  top:  8rem;
}


}


</style>
