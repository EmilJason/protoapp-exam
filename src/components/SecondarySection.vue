<script setup>
import BadgeLaravel from '../assets/badge.laravel-mix.svg'
import BadgeHowToRead from '../assets/badge.how-to-read-code.svg'

const data = [
  {
    title: 'Automation',
    subtitle: 'Roll out',
    image: BadgeLaravel,
    spanTitle: 'Automatic Prototyping',
    description:
      'Webpack is the most powerful and flexible asset compilation tool available today. With that power, however, comes a certain level of complexity.'
  },
  {
    title: 'Simplicity',
    subtitle: 'Sip Coffee',
    image: BadgeHowToRead,
    spanTitle: 'Complexity Simplified',
    description:
      'I know too many backend developers who are stifled by one glaring phobia: CSS. How do you construct a layout when nothing lines up?'
  }
]
</script>

<template>
  <div class="bg-secondary">
    <div class="section-two">
      <h3>Last Call to Action</h3>
      <p>Another section content goes here.</p>
      <div class="card-list justify-center m-top">
        <div class="card rounded" v-for="item in data" :key="item.title">
          <div class="image-with-title">
            <img :src="item.image" alt="" />
            <h5 class="rounded-5">{{ item.title }}</h5>
          </div>
          <div class="content">
            <span>{{ item.subtitle }}</span>
            <h4>{{ item.spanTitle }}</h4>
            <p>
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.bg-secondary {
  background-image: url('../assets/bg-decals3.svg');
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: contain;
  padding-top: 7rem;
  padding-bottom: 7rem;
  min-height: 100vh;
  .section-two {
    text-align: center;
    h3 {
      font-size: 3rem;
      font-weight: bold;
    }
    p {
      font-size: 1.5rem;
    }

    .card-list {
      display: flex;
      align-items: center;
      margin: 5rem;
      @media screen and (max-width: 821px) {
        flex-direction: column !important;
        margin: 1rem !important;
        padding: 0;
      }
      @media screen and (max-width: 981px) {
        flex-direction: column !important;
        margin: 3rem;
        padding: 0;
      }
      @media screen and (max-width: 1371px) {
        margin: 10rem;
        padding: 0;
      }
    }
    .card {
      display: flex;
      flex-direction: row;
      margin-top: 7rem;
      gap: 3rem;
      align-items: center;
      background-color: var(--bg-color-card-1);
      padding: 3rem;
      max-width: 30%;

      @media screen and (max-width: 821px) {
        max-width: 90%;
        margin: 1rem 0 !important;
      }
      @media screen and (max-width: 981px) {
        flex-direction: column !important;
        max-width: 40%;
        margin: 1rem 0;
      }

      &:nth-child(2) {
        background-color: var(--bg-color-card-2);
      }

      .image-with-title {
        display: flex;
        flex-direction: column;
        gap: 1rem;

        h5 {
          text-transform: uppercase;
          font-size: 0.7rem;
          color: white;
          background-color: #bdbdbd81;
          padding: 0.2rem 0.1rem;
        }
      }
      .content {
        text-align: left;
        color: white;
        span {
          text-transform: uppercase;
          font-size: 0.8rem;
        }
        h4 {
          font-size: 2.1rem;
          font-weight: bold;
          margin-bottom: 2rem;
          width: 50%;
        }
        p {
          font-size: 1.1rem;
        }
      }
    }
  }
}
</style>
