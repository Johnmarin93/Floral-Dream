<script setup>
import faq from '@/data/faq.js'
import FAQItem from '@/components/home/faq/FAQItem.vue'
</script>
<template>
  <section class="faq section bg-light">
    <div class="container">
      <h2 class="text-center mb-5">Preguntas Frecuentes</h2>
      <div v-for="item in faq" :key="item.id"><FAQItem :item="item" /></div>
    </div>
  </section>
</template>
