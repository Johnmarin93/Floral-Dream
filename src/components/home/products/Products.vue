<script setup>
import products from '@/data/products.js'
import ProductCard from '@/components/home/products/ProductCard.vue'
import BaseSectionTitle from '@/components/common/BaseSectionTitle.vue'
</script>

<template>
  <section id="products-section" class="products section">
    <div class="container">
      <BaseSectionTitle title="Productos destacados" />
      <div class="row">
        <div class="col-md-3" v-for="product in products" :key="product.id">
          <ProductCard :product="product" />
        </div>
      </div>
    </div>
  </section>
</template>
