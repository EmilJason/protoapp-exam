<script setup>
import NavbarComponent from '@/components/NavbarComponent.vue'
import Appstore from '../assets/badge.app-store.svg'
import Playstore from '../assets/badge.play-store.svg'
</script>

<template>
  <div class="bg-img">
    <NavbarComponent />
    <div class="container jumbotron">
      <h1>Protoapp</h1>
      <p>
        Our landing page works on all devices, so you only have to set it up once, and get beautiful
        results forever.
      </p>
      <button class="btn btn-primary rounded mt-1 mb-3">Get Started</button>

      <hr class="mb-2 mt-2" />
      <div class="flex justify-center">
        <img :src="Appstore" alt="app-store" />
        <img :src="Playstore" alt="play-store" />
      </div>
      <hr class="mb-2 mt-2" />
    </div>
  </div>
</template>

<style lang="scss">
@import url('../assets/styles/main.scss');
.bg-img {
  background-image: url('../assets/bg-leaves.svg'), url('../assets/bg-decals.svg');
  background-repeat: no-repeat;
  background-position:
    top right,
    bottom left;
  min-height: 80vh;

  .jumbotron {
    margin: 12rem 10rem;
    @media screen and (max-width: 480px) {
      margin: 1rem;
    }
    @media screen and (max-width: 820px) {
      margin: 1rem;
    }

    h1 {
      font-size: 5rem;
      font-weight: 300;
      @media screen and (max-width: 480px) {
        font-size: 2.8rem;
      }
    }

    p {
      font-size: 2.5rem;
      font-weight: lighter;
      width: 42%;
      @media screen and (max-width: 480px) {
        font-size: 2.1rem;
        width: 100%;
      }
    }
  }
}
</style>
