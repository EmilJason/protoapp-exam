<script setup>
import Appstore from '../assets/badge.app-store.svg'
import Playstore from '../assets/badge.play-store.svg'
</script>
<template>
  <div class="bg-section">
    <div class="section-one">
      <h3>Deep dive. Ready?</h3>
      <p>So are we. You're. Not. Word filler.</p>
      <div class="flex justify-center m-top">
        <img :src="Appstore" alt="app-store" />
        <img :src="Playstore" alt="play-store" />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import url('../assets/styles/main.scss');
.bg-section {
  background: url('../assets/bg-decals2.svg') top right no-repeat;
  padding-top: 10vh;
}
.section-one {
  text-align: center;
  min-height: 60vh;
  background: #2248e2;
  mix-blend-mode: screen;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 0.7rem;
  h3 {
    color: white;
    font-size: 3rem;
    font-weight: bold;
  }
  p {
    color: white;
    font-size: 1.7rem;
    font-weight: lighter;
  }

  .m-top {
    margin-top: 4rem;
  }
}
</style>
