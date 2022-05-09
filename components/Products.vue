<template>
  <div class="container">
    <h3 class="header">
      Latest Products
    </h3>
    <div v-if="products">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :product="product"
      />
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
    this.products = await fetch('https://fakestoreapi.com/products?sort=desc').then(res => res.json())
  }
}
</script>

<style scoped>

    .container {
        margin-top: 2rem;
    }
    .header {
        font-weight: 300;
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
