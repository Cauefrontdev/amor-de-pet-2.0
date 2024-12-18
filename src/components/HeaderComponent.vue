<template>
    <div class="container-sm">
      <header class="header">
        <nav class="nav">
          <img src="logo.jpg" alt="" class="logo">
          <button class="hamburger"></button>
          <ul class="nav-list">
            <li><a href="#">Cadastrar pet</a></li>
            <li><a href="#">Encontrar pet</a></li>
            <li><a href="#">Adoção</a></li>
            <li><a href="#">Ajudar</a></li>
            <li><a href="" class="btn">Entrar <i class="fa-solid fa-arrow-right"></i></a></li>
          </ul>
        </nav>
      </header>
    </div>
  </template>
  
  <script>
  export default {
    name: "HeaderComponent",
    mounted() {
      const hamburger = document.querySelector(".hamburger");
      const nav = document.querySelector(".nav");
  
      hamburger.addEventListener("click", () => {
        nav.classList.toggle("active");
      });
    },
  };
  </script>
  
  <style scoped>
  * {
    margin: 0;
    padding: 0;
  }
  
  a {

    text-decoration: none;
  }
  
  .header {
    padding-inline: 16px;
  }
  
  .nav {
    max-width: 100%;
    height: 15vh;
    margin-inline: auto;
    display: flex;
    justify-content: space-between;
    align-items: end;
  }
  
  .logo {
    max-width: 150px;
  }
  
  .nav-list {
    align-items: center;
    display: flex;
    gap: 32px;
    list-style: none;
  }
  
  .nav-list a {
    font-size: 1.1rem;
    color: #8C52FF;
    transition: 400ms;
  }

  .nav-list a:hover {
    font-weight: bold;
  }
  
  

  
  .hamburger {
    z-index: 1000;
    display: none;
    border: none;
    background: none;
    border-top: 3px solid #8C52FF;
    cursor: pointer;
  }
  
  .hamburger::after,
  .hamburger::before {
    z-index: 1000;
    content: " ";
    display: block;
    width: 30px;
    height: 3px;
    background: #8C52FF;
    margin-top: 5px;
    position: relative;
    transition: 400ms;
  }
  
  @media (max-width: 844px) {
    .hamburger {
      display: block;
    }

    .nav {
    height: 12vh;
    align-items: center;
  }
  
    .nav-list {
      z-index: 999;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: #fff;
      clip-path: circle(100px at 90% -15%);
      transition: 1s ease-out;
  
      flex-direction: column;
      justify-content: space-around;
      align-items: center;
      gap: 0;
  
      pointer-events: none;
    }
  
    .nav-list a {
      font-size: 24px;
      opacity: 0;
    }
  
    .nav-list li:nth-child(1) a {
      transition: 0.5s 0.2s;
    }
  
    .nav-list li:nth-child(2) a {
      transition: 0.5s 0.4s;
    }
  
    .nav-list li:nth-child(3) a {
      transition: 0.5s 0.6s;
    }
  
    .nav.active .nav-list {
      clip-path: circle(1500px at 90% -15%);
      pointer-events: all;
    }
  
    .nav.active .nav-list a {
      opacity: 1;
    }
  
    .nav.active .hamburger {
      position: fixed;
      top: 26px;
      right: 16px;
      border-top-color: transparent;
    }
  
    .nav.active .hamburger::before {
      transform: rotate(135deg);
    }
  
    .nav.active .hamburger::after {
      transform: rotate(-135deg);
      top: -7px;
    }
  }
  </style>
  