<script setup>
import BaseButton from '@/components/common/BaseButton.vue'
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
    <h3>{{ product.name }}</h3>
    <p class="product-price">{{ product.price }}</p>
    <span v-for="n in product.rating" :key="n"> ⭐ </span>
    <div class="mt-3">
      <BaseButton variant="primary"> Agregar al carrito </BaseButton>
    </div>
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
  border-radius: 10px;
  margin-bottom: 15px;
}
</style>
