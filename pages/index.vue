<template>
  <div>
    <Nav />
    <ProductGrid />
    <ProductsLatest />
    <ProductsPopular />
    <ProductsLowest />
    <ProductsMen />
    <ProductsWomen />
    <ProductsJewellery />
    <ProductsElectronics />
    <!-- <div class="container">
      <h4 class="header">
        Latest Products
      </h4>
      <p class="snippet">
        Latest Products displayed here.
      </p>
      <div v-if="products" class="cards-container">
        <ProductCard
          v-for="product in products"
          :key="product.id"
          :product="product"
        />
      </div>
      <div v-if="products1" class="cards-container">
        <ProductCard
          v-for="product in products1"
          :key="product.id"
          :product="product"
        />
      </div>
    </div> -->
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
  // data () {
  //   return {
  //     products: [],
  //     products1: []
  //   }
  // },
  // async fetch () {
  //   const productList = await fetch('https://fakestoreapi.com/products').then(res => res.json())
  //   const listReverse = productList.reverse()
  //   this.products = listReverse.slice(0, 5)
  //   this.products1 = productList.filter(product => product.rating.rate >= 4)
  // }
}
</script>

<style scoped>

    /* .container {
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
        flex: nowrap;
    } */

</style>
