<template>
    <div class="app-body">
      <HeaderComponent/>
      <HomeComponent/>
      <div class="bg"><InfoSectionComponent/></div>
      <div class="bg2"><CardsComponent/>
        <img class="dog" src="dog3.png">
      </div>
      <FooterComponent/>
    </div>
</template>

<script>
import HomeComponent from './components/HomeComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import InfoSectionComponent from './components/InfoSectionComponent.vue';
import CardsComponent from './components/CardsComponent.vue';
export default {
  name: 'App',
  components: {
    HomeComponent,
    FooterComponent,
    HeaderComponent,
    InfoSectionComponent,
    CardsComponent,
 },
};
</script>

<style scoped>
  .app-body {
    width: 100%;
    position: relative;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .bg {
    width: 100%;
    height: auto;
    margin-top: 50px;
    background-color: #8C52FF;
  }

  .bg2 {
    position: relative;
    width: 100%;
    height: auto;
    overflow: hidden;
    margin-top: 50px;
    background-color: #fff;
  }

  .dog {
        position: absolute;
        right: -18rem;
        bottom: 0px;
        width: 950px;
    }

    @media (max-width: 992px) {
      .dog {
        width: 750px;
        right: -280px;
      }
    }
    

</style>



