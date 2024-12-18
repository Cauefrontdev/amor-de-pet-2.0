<template>

    <div class="container-sm">
      <div class="hero">
        <div class="text-box">
          <h1 class="title">Seus dados estão seguros com a gente.</h1>
          <p>Nosso site conecta pessoas da sua região para compartilhar informações em tempo real, aumentando as chances de localizar o seu pet perdido de forma muito mais rápida e eficiente.</p>
          <div class="btn-box">
            <a href="" class="btn">Perdi meu pet <i class="fa-solid fa-arrow-right"></i></a>
            <a href="" class="btn1">Achei um pet <i class="fa-solid fa-arrow-right"></i></a>
          </div>
        </div>
        <div class="card-box">
          <div class="card1">
            <i class="fa-solid fa-lock"></i>
            <h4>Site seguro e protegido.</h4>
          </div>
          <div class="card1">
            <i class="fa-solid fa-clock"></i>
            <h4>Tudo em tempo real.</h4>
          </div>
          <div class="card1">
            <i class="fa-solid fa-users"></i>
            <h4>Comunidade nas redes sociais</h4>
          </div>
        </div>
        
        
      </div>
    </div>
     
    </template>
    
    <script>
    export default {
      name: 'CardsComponent',
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
      height: 90vh;
    
      
    }
    
    h1, p {
      color: #8C52FF;
    }
    
    .hero {
        padding-top: 50px;
        padding-bottom: 50px;
    width: 100%;
      position: relative;
      align-items: center;
      display: flex;
      justify-content: space-between;
      gap: 15rem;
      height: 100%;
    }

   

    .card-box {
        display: flex;
    width:  40rem;
    flex-wrap: wrap;
    gap: 4rem;
    height: auto;
}

.text-box {
      display: flex;
      flex-direction: column;
      gap: 26px;
    }


    .card1 {
      position: relative;
        display: flex;
        width: 15rem;
        height: 15rem;
        align-items: center;
        color: #fff;
        font-weight: bold;
        justify-content: center !important; 
        background-color: #8C52FF;
        border-radius: 60px;

        & h4 {
            font-size: 20px !important;
            max-width: 150px;
        }

        & i {
          position: absolute;
          font-size: 84px;
          top: -40px;
          color: #FFB602;
        }
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
        padding-bottom: 200px;
      }

      .card-box {
        padding-top: 50px;
        width: auto;
      }


      .card-box {
        flex-direction: column;
        flex-wrap: nowrap;
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
        height: 20rem;
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
    