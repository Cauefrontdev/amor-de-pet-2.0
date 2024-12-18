<template>
    <footer class="footer">
      
        <div class="selo-box">
            <div class="selo"><img class="img" :src="require('@/assets/img/boleto.png')" alt="boleto-icon"></div>
            <div class="selo"><img class="img" :src="require('@/assets/img/visa-svgrepo-com.svg')" alt="visa-icon"></div>
            <div class="selo"><img :src="require('@/assets/img/mc-icon.png')" alt="mc-icon"></div>
            <div class="selo"><img class="img pp" :src="require('@/assets/img/paypal-140-svgrepo-com.svg')" alt="pp-icon"></div>
        </div>
        <img class="selo-2" :src="require('@/assets/img/selo.png')" alt="selo-de-segurança">
        <nav>
            <a href="">Feedback</a>
            <a href="">Contato</a>
            <a href="">Parcerias</a>
        </nav>
        <p>Tem uma ong? Seja nosso parceiro!</p>
        <nav>
            <p>&copy; <b>Amor de pet</b> todos direitos reservados</p>
        </nav>
        <p>Desenvolvido por:</p>
        <img class="logo img" src="https://i.imgur.com/WSq33AA.png" alt="">
    </footer>
</template>
   
   <script>
   export default {
     name: 'FooterComponent',
     props: {
       msg: String
     }
   }
   </script>
   
   
   <style scoped>

   a {
    color: #fff;
   }

   .pp {
    max-width: 20px !important;
   }

   .selo-2 {
    max-width: 180px;
   }

   nav {
    justify-content: center;
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    text-align: center;
   }

   .selo-box {
    display: flex;
    gap: 15px;
   }

   .selo {
    width: 40px;
    height: 40px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #ffb602;

    & img {
        max-width: 30px;
    }
   }
   
   .footer {
    padding-top: 50px;
    padding-bottom: 130px;
    gap: 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-top: 2px solid #7C05B2;
    background-color: #7C05B2;
    color: white;
   }

   .img {
    filter: brightness(0) invert(1);
   }

   @media (max-width: 844px) {
    nav {
        flex-direction: column;
    }
   }
   
   
   </style>
   