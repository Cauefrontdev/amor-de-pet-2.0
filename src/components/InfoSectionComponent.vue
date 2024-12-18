<template>

    <body>
        <div class="container-sm">
          <div class="hero">
            <div class="img-box">
              <img class="pet" src="vetor1.png" alt="">
             
            </div>
            <div class="text-box">
              <h1 class="title2">Alcance milhares em minutos!</h1>
              <p>Ative uma campanha de impacto nas redes sociais e aumente as chances de reencontro na região.</p>
              <h3 class="g">03 pet(s) encontrados na região</h3>
              <div class="btn-box">
                <a href="" class="btn">Ajude a aumentar esse número <i class="fa-solid fa-arrow-right"></i></a>
              </div>
              <a href=""><img src="perfil.png" alt="" class="perfil"></a>
            </div>
        
        
        
          </div>
        </div>
    </body>
     
    </template>
    
    <script>
    export default {
      name: 'InfoSectionComponent',
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
      justify-content: center;
      padding-top: 50px !important;
      padding-bottom: 50px !important;
      height: 90vh;
    }
    
    h1, p {
      color: #fff;
    }

    body {
        background-color: #8C52FF;
    }
    
    .hero {
    width: 100%;
      position: relative;
      align-items: center;
      display: flex;
      justify-content: space-between;
      gap: 15rem;
      height: 100%;
    }
    
    .g {
        color: #00BF77;
        font-weight: bold;
    }
    .text-box {
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
      height: 25rem;
      position: absolute;
      right: -27.1%;
      bottom: 0;
    }

    .perfil {
        max-width: 250px;
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
        justify-content: center;
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
        display: none;
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
        height: 25rem !important;
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
    