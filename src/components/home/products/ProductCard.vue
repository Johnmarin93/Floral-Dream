<script setup>
defineProps({
  product: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <article class="product-card">
    <img :src="product.image" :alt="product.name" class="product-image" />
    <h3 class="titulo">{{ product.name }}</h3>
    <span v-for="n in product.rating" :key="n"> ⭐ </span>
  </article>
</template>

<style scoped>
.product-card {
  padding: 20px;
  background: white;
  overflow: hidden;
  border-radius: 10px;
  text-align: center;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.product-price {
  font-size: 1.3rem;
  font-family: 'Bodoni Moda', serif;
  font-weight: 700;
  color: var(--primary);
  margin-bottom: 15px;
}

.product-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.product-image {
  width: 100%;
  height: auto;
}
.titulo {
  padding-top: 20px;
}
</style>
