/* eslint-disable vue/multi-word-component-names */
<template>
  <div class="container">
    <h4 class="header">
      Men's Clothing
    </h4>
    <p class="snippet">
      Men's Clothing are displayed below!
    </p>
    <div v-if="products" class="cards-container">
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
    const productList = await fetch('https://fakestoreapi.com/products').then(res => res.json())
    this.products = productList.filter(product => product.category === "men's clothing")
    // const listReverse = productList.reverse()
    // console.log(productList[0].rating.rate)

    // for (const x in productList) {
    //   // console.log(productList[x].rating.rate)
    //   if (productList[x].rating.rate >= 4.0) {
    //     console.log(x)
    //   }
    // }

    // console.log(popular)
    // console.log(productList)

    // for (let i = 0; i <= listReverse.length; i++) {
    // console.log(i)
    // if (listReverse[0] > 10) { console.log(i) }
    // }

    // if (productList.id > 10) {
    // this.products = listReverse.slice(0, 5)
    // } else {
    // this.products = 0
    // }

    // console.log(listReverse)
    // console.log(this.products)
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

</style>
