<template>
  <b-container fluid class="bv-example-row">
    <b-row>
      <b-col
        v-for="product in products"
        :key="product.id"
        :product="product"
      >
        <div>
          <b-card
            :title="product.title"
            :img-src="product.image"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem;"
            class="mb-2"
          >
            <b-card-text class="text-truncate">
              {{ product.description }}
            </b-card-text>

            <b-button href="#" variant="primary">
              {{ product.price }}
            </b-button>
          </b-card>
        </div>
      </b-col>
    </b-row>
  </b-container>
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

<style lang="scss" scoped>

</style>
