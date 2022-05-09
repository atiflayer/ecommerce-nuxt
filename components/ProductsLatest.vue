/* eslint-disable vue/multi-word-component-names */
<template>
  <div class="container">
    <h4 class="header">
      Latest Products
    </h4>
    <p class="snippet">
      Latest Products displayed here.
    </p>
    <div
      v-for="product in products"
      :key="product.id"
      :product="product"
      class="cards-container"
    >
      <b-card
        :title="product.title"
        img-src="https://picsum.photos/600/300/?image=25"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          {{ product.title }}...
        </b-card-text>

        <b-button href="#" variant="primary">
          Go somewhere
        </b-button>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      products: []
    }
  },
  async fetch () {
    const productList = await fetch('https://fakestoreapi.com/products').then(res => res.json())
    const listReverse = productList.reverse()
    this.products = listReverse.slice(0, 5)
  }
}
</script>

<style scoped>

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

    .product-card {
        margin-top: 1.5rem;
        height: 4rem;
        display: flex;
    }
    .text-container {
        margin-left: 2rem
    }
</style>
