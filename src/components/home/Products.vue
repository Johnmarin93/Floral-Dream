<script setup>
import products from '@/data/products.js'
import ProductCard from './ProductCard.vue'
</script>

<template>
  <section class="products">
    <div class="container">
      <h2 class="text-center mb-5">Productos destacados</h2>
      <div class="row">
        <div class="col-md-4" v-for="product in products" :key="product.id">
          <ProductCard :product="product" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.products {
  padding: 100px 0;
}
</style>
