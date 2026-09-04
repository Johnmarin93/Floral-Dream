<script setup>
import { ref } from 'vue'
const abierto = ref(false)
defineProps({
  item: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <article class="faq-item">
    <div class="faq-header" @click="abierto = !abierto">
      <h4>{{ item.question }}</h4>
      <button><i class="bi" :class="abierto ? 'bi-dash-lg' : 'bi-plus-lg'"></i></button>
    </div>
    <p v-if="abierto" class="faq-answer">
      {{ item.answer }}
    </p>
  </article>
</template>

<style scoped>
.bi {
  font-size: 1.5rem;
  color: var(--primary);
}
.faq-header {
  display: flex;

  justify-content: space-between;

  align-items: center;

  cursor: pointer;
}
.faq-header button {
  border: none;

  background: none;

  font-size: 2rem;

  cursor: pointer;
}
.faq-item {
  border-bottom: 1px solid #e9ecef;
  padding: 20px 0;
}

.faq-answer {
  margin-top: 15px;
  color: #6c757d;
  line-height: 1.8;
}
.faq-header h4 {
  margin: 0;
  font-size: 1.2rem;
  font-weight: 600;
}
</style>
