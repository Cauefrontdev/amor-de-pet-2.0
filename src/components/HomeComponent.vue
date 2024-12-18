<template>

<div class="container-sm">
  <div class="hero">
    <div class="text-box">
      <h1 class="title">Reunindo patas e corações de quem tanto amamos</h1>
      <p>Conectamos famílias e seus pets. Cadastre animais perdidos, publique achados ou descubra um novo amigo para adotar. Juntos, podemos transformar vidas!</p>
      <div class="btn-box">
        <a href="" class="btn">Perdi meu pet <i class="fa-solid fa-arrow-right"></i></a>
        <a href="" class="btn1">Achei um pet <i class="fa-solid fa-arrow-right"></i></a>
      </div>
    </div>
    <div class="img-box">
      <img class="pet" src="dog.png" alt="">
      <img src="vetor.png" alt="" class="vetor">
    </div>
    
    
  </div>
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

.container-sm {
  position: relative;
  display: flex;
  align-items: center;
  height: 80vh;
}

h1, p {
  color: #8C52FF;
}

.hero {
  position: relative;
  align-items: center;
  display: flex;
  gap: 15rem;
  height: 100%;
}

.text-box {
  padding-top: 26px;
  height: 100%;
  align-items: top;
  display: flex;
  flex-direction: column;
  gap: 26px;
}

.btn-box {
  display: flex;
  gap: 16px;
}

.pet{
  height: 25rem;
}

.vetor {
  height: 30rem;
  position: absolute;
  right: -27.1%;
  bottom: 0;
}

@media (max-width: 1200px) {
  .hero {
    gap: 10rem;
  }

  .vetor {
    right: -20%;
  }
}

@media (max-width: 992px) {
  .hero {
    flex-direction: column;
    gap: 3rem;
    text-align: left;
  }

  .text-box {
    align-items: left;
  }

  h1 {
    font-size: 2.4rem !important;
    max-width: 280px;
  }

  p {
    font-size: 1rem !important;
  }

  .btn-box {
    flex-direction: column;
    gap: 12px;
  }

  .pet {
    margin-top: 25px;
    margin-bottom:25px;
    height: 25rem;
  }

  .vetor {
    display: none;
  }
}

@media (max-width: 768px) {
  .container-sm {
    height: auto;
    padding: 1rem;
  }

  .hero {
    gap: 2rem;
  }

  h1 {
    font-size: 1.8rem;
  }

  p {
    font-size: 1rem;
  }

  .pet {
    height: 15rem;
  }

  .vetor {
    height: 20rem;
    right: -5%;
  }
}

@media (max-width: 576px) {
  .text-box {
    gap: 16px;
  }

  h1 {
    font-size: 1.5rem;
  }

  p {
    font-size: 0.9rem;
  }

  .btn {
    font-size: 0.9rem;
  }

  .btn1 {
    font-size: 0.9rem;
  }

  .pet {
    height: 12rem;
  }

  .vetor {
    height: 15rem;
    right: 0;
  }
}

</style>
