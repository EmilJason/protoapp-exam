<script setup>
import Logo from '../assets/logo1.svg'
</script>
<template>
  <header class="navbar">
    <div class="container flex">
      <img :src="Logo" alt="" />
      <h1 class="brand-name"><header>Protoapp</header></h1>

      <nav class="nav-links ml-1">
        <li>
          <a href="">Home</a>
        </li>
      </nav>
    </div>
  </header>
</template>
<style lang="scss"></style>
