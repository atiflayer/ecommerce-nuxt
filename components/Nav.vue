<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark padding">
    <NuxtLink class="navbar-brand" to="/">Ecommerce</NuxtLink>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse ml-auto" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
            <li class="nav-item active">
                <NuxtLink to="/products" class="nav-link">Home <span class="sr-only">(current)</span></NuxtLink>
            </li>
            <li class="nav-item active">
                <NuxtLink to="/my-items" class="nav-link">Product List <span class="sr-only">(current)</span></NuxtLink>
            </li>
        </ul>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
    .padding {
        padding: 1.5rem;
        background-color: black
    }
    .nav-left {
        margin-left: auto;
    }

</style>
