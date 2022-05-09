<template>
  <div class="card">
    <img :src="product.image" alt="" class="image">
    <h5 class="header">
      {{ product.title }}
    </h5>
    <p class="snippet">
      Product ID : {{ product.id }}
    </p>
    <p class="snippet">
      Rating : {{ product.rating.rate }}
    </p>
    <p class="snippet">
      Price : {{ product.price }}
    </p>
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
    /* p {
        color: grey
    } */

    /* img {
        width: 4rem;
        height: 4rem;
        border-radius: 100%;
    } */

    .container {
        margin-top: 2rem;
    }
    /* .header {
        font-weight: 700;
        font-size: 1.5rem;
    } */
    .snippet {
        color: grey;
        margin-bottom: 0.5rem;
    }

    .card {
        width: 31.5%;
        height: 25rem;
        border: none;
        overflow: hidden;
        padding: 0;
        cursor: pointer;
    }
    .image {
        height: 55%;
        border-radius: 0.5rem;
    }
    .header {
        font-size: 1.15rem;
        margin-top: 0.4rem;
        color: black;
    }
    .header:hover {
      color: black;
      text-decoration: none;
    }
    /* .snippet {
        color: grey
    } */

</style>
