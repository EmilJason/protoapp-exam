<script setup>
import ProductSearch from '../assets/product-search.svg'
import ProductSmartphone from '../assets/product-smartphone.svg'
import ProductWork from '../assets/product-work.svg'

const data = [
  {
    title: 'Discover',
    image: ProductSearch,
    description:
      'Get information on using these guidelines whenever you are using therefore they have the same style and quality.'
  },
  {
    title: 'Augmented',
    image: ProductSmartphone,
    description:
      'Word salad often arouses curiosity due to its seemingly intelligent and tasteful play on words.'
  },
  {
    title: 'Endless Possibilities',
    image: ProductWork,
    description: `Management Systems shouldn't be a bore. Run out of words? here some lorem ipsum: Lorem ipsum dolor sit amet.`
  }
]
</script>

<template>
  <div class="container about">
    <div class="center mb-3">
      <h2>Meet Protoapp</h2>
      <p>
        The app lorem ipsum is common placeholder text used to demonstrate the graphic elements of a
        document or visual presentation.
      </p>
    </div>

    <div class="about-lists">
      <div class="flex item" v-for="item in data" :key="item.title">
        <img :src="item.image" alt="" />
        <div class="card">
          <h4>{{ item.title }}</h4>
          <p>{{ item.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import url('../assets/styles/main.scss');

.center {
  text-align: center;

  h2 {
    font-size: 4rem;
  }

  p {
    font-size: 2rem;
    font-weight: lighter;
    width: 60vw;
    margin: auto;
  }
}

.about {
  margin-top: 1rem;
}

.about-lists {
  margin: auto;
  max-width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.item {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  @media screen and (max-width: 1024px) {
    flex-direction: column;
  }
  &:nth-child(odd) {
    flex-direction: row-reverse;

    @media screen and (max-width: 1024px) {
      flex-direction: column;
    }
  }
  &:nth-child(odd) .card h4,
  &:nth-child(odd) .card p {
    text-align: right;
  }

  img {
    width: 20rem;
    min-height: 20rem;
  }
  .card {
    display: flex;
    flex-direction: column;
    margin: 1rem;

    h4 {
      font-size: 2rem;
      font-weight: bold;
    }

    p {
      font-size: 1.5rem;
      font-weight: lighter;
      width: 100%;
    }
  }
}
</style>
