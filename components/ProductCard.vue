<template>
  <div class="container">
    <div class="cards-container">
      <img :src="product.image" alt="">
    </div>
    <div class="header text-container">
      <h3>{{ product.title }}</h3>
      <p class="snippet">
        {{ product.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['product']
}
</script>

<style scoped>
    .product-card {
        margin-top: 1.5rem;
        height: 4rem;
        display: flex;
    }
    .text-container {
        margin-left: 2rem
    }
    p {
        color: grey
    }

    img {
        width: 4rem;
        height: 4rem;
        border-radius: 100%;
    }

    .container {
        margin-top: 2rem;
    }
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }

</style>
