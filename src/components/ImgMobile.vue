<template>

    <div class="container">
     <img class="pet-float img" :src="require('@/assets/img/dog-home.png')" alt="Dog Home">
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
    display: none;
   }
   
   .pet-float {
     max-width: 240px;
     right: 0;
     bottom: 0;
   }
   
 
   
   img {
     filter: opacity(0.9);
     display: none;
   }
   
   @media (max-width: 1000px) {
   
     .img {
       display: block;
     }

     .container {
        display: flex;
        position: relative;
        align-items: center;
        justify-content: right;
        width: 100vw;
        background: linear-gradient(to top, #ffb602);
        height: auto;
        margin-top: -70px;
     }
   }
   
   
   </style>
   