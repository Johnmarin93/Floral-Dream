<script setup>
import testimonials from '@/data/testimonials.js'
import TestimonialCard from './TestimonialCard.vue'
</script>

<template>
  <section class="testimonials">
    <div class="container">
      <h2 class="text-center mb-5">Testimonios de clientes</h2>
      <div class="row">
        <div class="col-md-4" v-for="testimonial in testimonials" :key="testimonial.id">
          <TestimonialCard :testimonial="testimonial" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.testimonials {
  padding: 100px 0;
}
</style>
