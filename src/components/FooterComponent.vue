<script setup>
import { ref } from 'vue'
import Logo from '../assets/logo1.svg'
const currentYear = ref(new Date().getFullYear())
</script>

<template>
  <div class="bg-footer-color">
    <div class="container bg-footer-color">
      <div class="flex">
        <img :src="Logo" alt="" />
        <div class="footer-content">
          <h4>Protoapp</h4>
          <h5>Camp One Inc, LLC</h5>
          <p>
            Que Ad Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo, quisquam.
            Repellat neque velit, explicabo ipsa itaque a, ea id magnam debitis praesentium aut?
            Eligendi culpa quam voluptate necessitatibus itaque nisi minima natus impedit inventore
            ea. Eos dignissimos nemo nostrum adipisci?
          </p>
        </div>
      </div>
      <span> &copy; {{ currentYear }} Protoapp. All rights preserved.</span>
    </div>
  </div>
</template>

<style lang="scss">
.bg-footer-color {
  padding-top: 3rem;
  padding-bottom: 3rem;
  .flex {
    gap: 2rem;
    margin-bottom: 1.1rem;
    img {
      width: 4rem;
      height: 4rem;
      align-self: flex-start;
    }
    .footer-content {
      display: flex;
      flex-direction: column;
      color: white;
      h4 {
        font-size: 1.3rem;
      }
      h5 {
        font-size: 1.5rem;
        font-weight: normal;
      }
      p {
        width: 45%;
        font-weight: lighter;
        line-height: 1.7rem;
        @media screen and (max-width: 821px) {
          width: 90%;
        }
      }
    }
  }
  span {
    color: white;
    font-weight: lighter;
    font-size: 0.8rem;
    margin-top: 30rem;
  }
}
</style>
